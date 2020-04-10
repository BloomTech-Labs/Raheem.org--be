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

emails
officers
reports
stories

#### DOCUMENTS IN COLLECTIONS

##### EMAILS

---

{
  id: UUID
  emails: STRING
}


##### OFFICERS

---

{
  id: UUID,
  departmentPolicies: STRING,
  officerBadgeID: STRING,
  officerrFName: STRING
  officerLName: STRING
  officerGender: STRING
  officerOutcomes: STRING
  officerPoliceDepartment: STRING
  officerRace: STRING
  officer_id: STRING
}

##### REPORTS

---

{
  id: UUID,
  dob: STRING,
  gender: STRING,
  incidentDate: STRING,
  race: STRING,
  rating: NUMBER,
  selfIdentify: STRING,
  tags: [],
  time: STRING,
  first_name: STRING,
  last_name: STRING
}

##### STORIES

---

{
  id: UUID,
  reportRef: REFERENCES REPORTS COLLECTION UUID,
  storyBody: STRING
}


## 2️⃣ Actions

See organization routes

## 3️⃣ Environment Variables

Environment Variables configurations can only be set in the Firebase Cloud Functions when the database is deployed and hosted live. We currently have the database in TEST because we plan to hand it off to the stakeholder.

See [Raheem Frontend Documentation]--https://github.com/Lambda-School-Labs/raheem.org--fe/blob/master/README.md
