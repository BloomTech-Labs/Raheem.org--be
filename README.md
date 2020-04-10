# API Documentation -- Raheem Backend

#### 1️⃣ Backend deployed via [Google Firebase](https://console.firebase.google.com/project/raheem-b6ed6/overview) <br><br>

## 1️⃣ Getting started

To get the server running locally: We integrated Firebase directly into the React application.

### Backend framework goes here

🚫 Why did we choose this framework?

-    Point One - The stakeholder specifically requested ths framework.
-    Point Two - We recommended alternatives for more complex and larger databases, but they were deemed unnecessary.
-    Point Three - The project is small enough that it didn't require a deeply complex backend.

## 2️⃣ Endpoints

Firebase hosts its data in a series of "collections" that house the documents containing the information returned to the server. Here are the typical CRUD operations using Firebase. We are using an example collection called colName

#### Organization Routes

| Method | Endpoint                | Access Control | Description                                  |
| ------ | ----------------------- | -------------- | -------------------------------------------- |
| GET    | firebase.firestore().collection("colName").get() | owners     | Return all the records in the collection colName |
| ADD    | firebase.firestore().collection("colName").add({content, content, content}) | owners     | Add a record to the collection colName |
| PUT    | firebase.firestore().collection("colName").doc(id).update()  | owners         | Modify a specific record by id in the collection.             |
| DELETE | firebase.firestore().collection("colName").doc(id).delete()  | owners         | Delete a record by id in the collection.                      |


# Data Model

Cloud Firestore is a NoSQL, document-oriented database. Unlike a SQL database, there are no tables or rows. Instead, you store data in documents, which are organized into collections. Each document contains a set of key-value pairs.

#### 2️⃣ COLLECTIONS

emails<br>
officers<br>
reports<br>
stories<br>

#### DOCUMENTS IN COLLECTIONS
<br>
##### EMAIL

---

```
{
  id: UUID,
  emails: STRING
}
```

##### OFFICERS

---

```
{
  id: UUID,
  departmentPolicies: STRING,
  officerBadgeID: STRING,
  officerGender: STRING,
  officerFName: STRING,
  officerLName: STRING,
  officerOutcomes: STRING,
  officerPoliceDepartment: STRING,
  officerRace: STRING,
  officer_id: STRING
  
}
```
##### REPORTS

---

```
{
  id: UUID,
  dob: STRING,
  gender: STRING,
  incidentDate: STRING,
  race: STRING,
  rating: NUMBER,
  selfIdentify: STRING,
  tags: [],
  time: STRING
}
```

##### STORIES

---

```
{
  id: UUID
  reportref: REFERENCES REPORTS COLLECTION UUID,
  storyBody: STRING
}
```

## 2️⃣ Actions

See Organization Routes. No further actions needed to submit forms in the Frontend

## 3️⃣ Environment Variables

Environment Variables can only be configured for Firebase Cloud Functions when the backend database is deployed live. We currently have it in test mode to hand it off to the stakeholders, so they can deploy it.

### Attribution

These contribution guidelines have been adapted from [this good-Contributing.md-template](https://gist.github.com/PurpleBooth/b24679402957c63ec426).

## Documentation

See [Raheem Frontend Documentation](https://github.com/Lambda-School-Labs/raheem.org--fe/blob/master/raheem/README.md) for details on the frontend of our project.

