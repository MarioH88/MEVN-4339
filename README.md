# project-cis_4339_project_38
project-cis_4339_project_38 created by GitHub Classroom


<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#introduction">Introduction</li>
        <li><a href="#goals">Goals</li>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>

    
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About The Project

CIS-4339-Project_38 Group presenting: Web Application for Restoring Justice

### Team Members:

Vincent Vu, Mario Hayden, & Christopher Ayala

### Introduction:

We will be creating web application based on Restoring Justice's request. 

### Goals:

*  Implementation of Intake form (Viewable and editable with history of edits to track)
*  A page that allows a case manager to track referrals
*  Summary Report

### Built With

*  MongoDB (mongodb://localhost:27017/RestoringJusticeDB)
*  VueJS
*  Node


<!-- GETTING STARTED -->
## Getting Started
* Visual Studio Code (or your preference)
* MongoDB 
* Install dependencies (see below)



### Prerequisites
 Dependencies
 * express (npm install express)
 * mongoose (npm install express)
 * morgan (npm install morgan
 * uuid (npm install uuid)

<!-- STARTING UP PROJECT FOR SPRINT 2 -->


<!-- Conclusion -->
### Test Results from Postman
![image](https://user-images.githubusercontent.com/55208797/136436812-fb987b67-9af8-47ed-bec1-68fe5f981ea3.png)
create general info with /creategeninfo


![image](https://user-images.githubusercontent.com/55208797/136436989-b6ae3d27-bc44-41d8-9454-9763806dcbd5.png)
result of /get on generalinfo

![image](https://user-images.githubusercontent.com/55208797/136443822-3c9d1e38-d4dd-44c8-8b77-0b0ba6152972.png)
result of /updategenInfo put request

![image](https://user-images.githubusercontent.com/55208797/136444002-0e70321f-87d6-424a-a4d3-775a70c73fe2.png)
verify that PUT request works

![image](https://user-images.githubusercontent.com/55208797/136465773-beedd30c-3848-4306-97a9-21c0b4ea4eb8.png)
result of /delete on general info

<!-- STARTING UP SPRINT 2-->
## SPRINT 2 INSTRUCTIONS
Step 1: Clone Github Repository

Step 2: Starting up Backend (Back-end)
- Open a new terminal
- type 'cd Back-end' to change to the backend directory
- type 'npm install' to get all the dependecies for the backend server
- type 'node index.js' to connect and run the backend server

Step 3: Starting up Frontend (Front-end)
- Open a new terminal just as in step 2.
- type 'cd Front-end' to change to the frontend directory
- type 'npm install' to get all the dependecies for the frontend
- type 'npm run serve' to connect and run the fronend application
- Follow the link and the application will display for use

Referral Form Business Logic
Frontend:

Created a new page for the referrals which consists of the ff:
●	INDEX/LANDING
○	This page contains the list of referrals added in the system.
○	Functions:
■	UPDATE
●	Upon clicking this button, the user will be redirected to the update page of that specific referral.
■	DELETE
●	Upon clicking this button, the user/admin will ask by the system if he/she is sure of deleting that referral. If yes, the system will call an API to delete that row, if not, the system will do nothing and close the prompt.
■	VIEW LOGS
●	Upon clicking this button, the user will be redirected to the logs page of that specific referral.

●	CREATE
○	In this page, the user will fill-up the form for adding a referral.
○	The form consists of:
■	Social service (Required)
●	If the user chose Other, a new field will be shown to input a specific social service that is not on the list.
■	Case Manager
●	First name (Required)
●	Middle name (Optional)
●	Last name (Required)
■	Short Notes (Required)
■	Date (Required)
■	Time (Required)
■	Is the client referred? (Required)
●	If Yes, a new field will be shown to input the Case Number who referred the client.
■	Is Underlying need addressed?
●	Not at All
●	Partially
●	Fully
○	After filling-up the form, an API call is used to store the data.

●	UPDATE
○	In this page, an API is used to retrieve the previous value of the specific referral. The user can update the form
○	The form consists of:
■	Social service (Required)
●	If the user chose Other, a new field will be shown to input a specific social service that is not on the list.
■	Case Manager
●	First name (Required)
●	Middle name (Optional)
●	Last name (Required)
■	Short Notes (Required)
■	Date (Required)
■	Time (Required)
■	Is the client referred? (Required)
●	If Yes, a new field will be shown to input the Case Number who referred the client.
■	Is Underlying need addressed?
●	Not at All
●	Partially
●	Fully
○	After filling-up the form, an API call is used to store the updated data together with the update logs of the referral.

●	VIEW LOGS
○	In this page, an API is used to call all the update logs happened on that referral
○	Table consists of:
■	ID of the referral
■	Timestamp

Backend:

Created new files and code for the referral module which is the ff:
●	Added an API endpoint for the CRUD of referral
●	This was connected to a Controller
○	INDEX
■	List of all referrals
■	The deleted referrals will not be shown but still on the database
○	CREATE
■	Storing of newly added data
○	SHOW
■	Fetching of specific referral
○	UPDATE
■	Updating of retrieve data from the database
■	Storing of update logs
○	DELETE
■	Delete a referral
■	Deleting the referral will not remove permanently. It will just have a status of DELETED = true
○	LOGS
■	List of update logs for that specific referral
●	Added a new Model
○	REFERRAL
■	This model is for the referral
■	The model consists of:
●	SocialService
●	LastName
●	FirstName
●	MiddleName
●	ShortNotes
●	Date
●	Time
●	IsReferred
●	CaseNumber
●	Addressed
●	Deleted (Soft deletes)
●	Other
○	REFERRAL LOGS
■	This model is for the referral logs
■	The model consists of:
●	ReferralId
●	Time


Referral Form Flowchart

![image](https://user-images.githubusercontent.com/72152763/141410738-31930879-2b53-419f-8c75-856582c7bebe.png)


We will also be demonstrating everything in our Microsoft Stream video on how to run the application.

**Update** App running but sometimes it have a random disconnection from database due to referrals page (possibly a bug), but in the end it works.

