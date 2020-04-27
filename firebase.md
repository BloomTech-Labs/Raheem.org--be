# FireBase Docs

## Initial Setup (Complete for Raheem)

- Login and create a new project at Firebase.google.com
- Setup DataBase
  - Start in testing mode and add security rules when pushing project to production.
  - Select the cloud firestore location (Note: This cannot be changed later).
- Get firestore access info.
  - Goto General settings for the project and add a html </> app.
  - Register app with a app name.
  - Copy and paste the firebase SDK into a notepad or other word document - this will be used in the next few steps.
  - Add a .env file to app files. (For security make sure you have a gitingor file and .env is being ignored.)
  - Insert this into the .env:
  ```
  REACT_APP_FIREBASE_APIKEY=
  REACT_APP_FIREBASE_AUTHDOMAIN=
  REACT_APP_FIREBASE_DATABASEURL=
  REACT_APP_FIREBASE_PROJECTID=
  REACT_APP_FIREBASE_STORAGEBUCKET=
  REACT_APP_FIREBASE_MESSAGINGSENDERID=
  REACT_APP_FIREBASE_APPID=
  REACT_APP_FIREBASE_MEASUREMENTID=
  ```
  - Using the SKD fill in the appropriate into.
- Add firebase dependencies to your react app.
  - Add Firebase: ``` npm i firebase ``` or ``` yarn add firebase ```
  - Add Firebase Tools: ``` npm i firebase-tools ``` or ``` yarn add firebase-tools ```
  - Add Firebase testing: ``` npm i firebase-jest-mock ``` or ``` yarn add firebase-jest=mock ``` (only if you plan on doing testing)
- Setup firebase/firestore hook
  - create firebase.js file. (Optional: add a cofig folder to app.)
  - Place this in file:
  ```js
  import firebase from 'firebase/app';
  import 'firebase/firestore';


  var firebaseConfig = {
    apiKey: process.env.REACT_APP_FIREBASE_APIKEY,
    authDomain: process.env.REACT_APP_FIREBASE_AUTHDOMAIN,
    databaseURL: process.env.REACT_APP_FIREBASE_DATABASEURL,
    projectId: "",
    storageBucket: process.env.REACT_APP_FIREBASE_STORAGEBUCKET,
    messagingSenderId: process.env.REACT_APP_FIREBASE_MESSAGINGSENDERID,
    appId: process.env.REACT_APP_FIREBASE_APPID,
    measurementId: process.env.REACT_APP_FIREBASE_MEASUREMENTID
  };
  
  // Initialize Firebase -- prevent "firebase has already been called" error with the 'if' statement
  if (!firebase.apps.length) {
    firebase.initializeApp(firebaseConfig)
  }

  export default firebase;
  ``` 
  - Add your project id to projectId
<br></br>
<br></br>
<br></br>
## Using the firebase hook

note: The hook is primarly used with forms and the onSubmit.
note: before you can add, update, remove any data from the firestore a collection needs to be added to the forestore.

- adding a collection to fireStore
  -- Collections are like tables in SQL databases.
  - Login to your firebase console.
  - Open Database tab
  - Press 'Start collection'
  - Give your collection a name.
  - You must have at lease one Document in any given collection at setup.
    - Dont wory about the Document id this is auto generated.
    - Add as many fields as you need for the data you want to save.
      - Give the field a Name, Type and a value.
    - Note: Documents are like rows and fields are like columns

Once you have all the collections you need for your apps database, head back over to your code.


Note: Make sure to import your firebase.js file to each component that will be talking to your database.
```js 
import firebase from './firebase.js';
```
### Adding data:

```js
firebase
  .firestore()
  .collection(`collection-name`)
  .add(
    {
      //data to add to collection
      //exe.
      name: 'Trevor Smith',
      DOB: '10/10/1950'
    }
  )
  .then(
    //this is anything you want to happen after a successful add
  )
```
### update data:

```js
firebase
  .firestore()
  .collection(`collection-name`)
  .doc(docId)
  .update(
    {
      //data to add to collection
      //exe.
      name: 'Trevor Smith',
      DOB: '10/10/1950'
    }
  )
  .then(
    //this is anything you want to happen after a successful update
  )
```

### delete data:

```js
firebase
  .firestore()
  .collection(`collection-name`)
  .doc(docId)
  .delete()
  .then(
    //this is anything you want to happen after a successful removal
  )
```
