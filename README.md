🚫 The numbers 1️⃣ through 3️⃣ next to each item represent the week that part of the docs needs to be comepleted by.  Make sure to delete the numbers by the end of Labs.

🚫 Each student has a required minimum number of meaningful PRs each week per the rubric.  Contributing to docs does NOT count as a PR to meet your weekly requirements.

# API Documentation

#### 1️⃣ Backend deployed via Google Firebase: https://console.firebase.google.com/project/raheem-b6ed6/overview) <br>

## 1️⃣ Getting started

To get the server running locally: We integrated Firebase directly into the React application.

### Backend framework goes here

🚫 Why did you choose this framework?

-    Point One - The stakeholder wanted it.
-    Point Two - We recommended alternatives, they did not appeal to the stakeholder.
-    Point Three - The project is small enough that it didn't require a deeply complex backend.
-    Point Four - The stakeholder wanted it.

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

---

emails
officers
reports
stories

#### DOCUMENTS IN COLLECTIONS
##### EMAIL

---

{
  id: UUID
  organization_id: UUID foreign key in ORGANIZATIONS table
  first_name: STRING
  last_name: STRING
  role: STRING [ 'owner', 'supervisor', 'employee' ]
  email: STRING
  phone: STRING
  cal_visit: BOOLEAN
  emp_visit: BOOLEAN
  emailpref: BOOLEAN
  phonepref: BOOLEAN
}


##### OFFICERS

---


{
  id: UUID
  organization_id: UUID foreign key in ORGANIZATIONS table
  first_name: STRING
  last_name: STRING
  role: STRING [ 'owner', 'supervisor', 'employee' ]
  email: STRING
  phone: STRING
  cal_visit: BOOLEAN
  emp_visit: BOOLEAN
  emailpref: BOOLEAN
  phonepref: BOOLEAN
}

##### REPORTS

---


{
  id: UUID
  organization_id: UUID foreign key in ORGANIZATIONS table
  first_name: STRING
  last_name: STRING
  role: STRING [ 'owner', 'supervisor', 'employee' ]
  email: STRING
  phone: STRING
  cal_visit: BOOLEAN
  emp_visit: BOOLEAN
  emailpref: BOOLEAN
  phonepref: BOOLEAN
}


##### STORIES

---

{
  id: UUID
  organization_id: UUID foreign key in ORGANIZATIONS table
  first_name: STRING
  last_name: STRING
  role: STRING [ 'owner', 'supervisor', 'employee' ]
  email: STRING
  phone: STRING
  cal_visit: BOOLEAN
  emp_visit: BOOLEAN
  emailpref: BOOLEAN
  phonepref: BOOLEAN
}



## 2️⃣ Actions

🚫 This is an example, replace this with the actions that pertain to your backend

`getOrgs()` -> Returns all organizations

`getOrg(orgId)` -> Returns a single organization by ID

`addOrg(org)` -> Returns the created org

`updateOrg(orgId)` -> Update an organization by ID

`deleteOrg(orgId)` -> Delete an organization by ID
<br>
<br>
<br>
`getUsers(orgId)` -> if no param all users

`getUser(userId)` -> Returns a single user by user ID

`addUser(user object)` --> Creates a new user and returns that user. Also creates 7 availabilities defaulted to hours of operation for their organization.

`updateUser(userId, changes object)` -> Updates a single user by ID.

`deleteUser(userId)` -> deletes everything dependent on the user

## 3️⃣ Environment Variables


# Attribution

These contribution guidelines have been adapted from [this good-Contributing.md-template](https://gist.github.com/PurpleBooth/b24679402957c63ec426).

## Documentation

See the Raheem Frontend -- https://github.com/Lambda-School-Labs/raheem.org--fe for details on the frontend of our project.

