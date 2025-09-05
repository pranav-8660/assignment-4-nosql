The Scenario:

You are the lead database architect for "Bengaluru Brigade", a new app that connects users with skilled local service providers ("Taskers") for everyday jobs.  

You will design and manage a database named bengaluru_brigade with three core collections:
users: Customers who post jobs.
taskers: The skilled professionals who perform the jobs.
tasks: The individual jobs that are posted, assigned, and completed.
Submission Guidelines:
You will submit a single PDF document. This document must contain clearly labelled screenshots for each task as requested. For the final task, you will write a short paragraph.
Task 1: Schema Design & Data Creation

Your first job is to design the collections and populate them with realistic, Bengaluru-based data.
Design and Create Collections:
Create the users, taskers, and tasks collections.
Populate with Data:
Using insertMany, add at least 4 documents to each collection.
users collection fields: userName, joinDate, city (e.g., "Bengaluru").
taskers collection fields: taskerName, skills (as an array, e.g., ["Plumbing", "Electrician"]), area (e.g., "Jayanagar", "Whitefield"), rating (a number from 1-5), hourlyRate (a number).
tasks collection fields: title (e.g., "Fix Leaky Kitchen Sink"), description (a short sentence), postedBy (the _id of a user from your users collection), assignedTo (the _id of a tasker), category (e.g., "Plumbing"), status ("Open", "Assigned", "Completed"), cost (a number).
(3 Screenshots Required) Provide one screenshot for each collection (users, taskers, tasks) showing the documents you have inserted.
Task 2: Indexing for Performance 
The app needs to be fast. Let us add indexes to speed up common searches.
Tasker Search: Users will frequently search for taskers by their specific skill and the area they work in. Create an efficient compound index on the taskers collection to support this query.
Task Description Search: Users should be able to search for tasks using keywords in the task description. Create a text index on the tasks collection to enable this.
(2 Screenshots Required) Provide a screenshot of the "Indexes" tab in MongoDB Compass for both the taskers and tasks collections, showing the new indexes you created.
Task 3: Practical CRUD Queries 


Now, perform some common operations that the app would need.

  
READ: A user in "Jayanagar" needs a plumber. Write a query to find all available taskers who have "Plumbing" in their skills array and work in the "Jayanagar" area.
UPDATE: A tasker has just finished a job. Find a task with the status "Assigned" and update it. Use $set to change the status to "Completed" and add a new field called completionDate with the current date.
(2 Screenshots Required) Provide a screenshot of the query and its result for both the READ and UPDATE operations. For the UPDATE, show the document after the change.
Task 4: The Aggregation Challenge 

The business team needs some insights. You must write a single aggregation pipeline to answer their complex question.
Business Question: "We want to identify our top-performing taskers. Who are our top 3 highest-rated taskers who have completed at least one task? For each of them, show their name, their average rating, and calculate their total earnings from all completed tasks."

Hints:
You will need to use $lookup to join the taskers and tasks collections.
You will need to $unwind the results of the lookup.
You will need $match to filter for tasks that are "Completed".
You will need $group to calculate the totalEarnings (using $sum) and get the tasker's rating.
You will need $sort and $limit to find the top 3.
(1 Screenshot Required) Provide a screenshot of your complete aggregation pipeline and the final output showing the top 3 taskers.
Task 5: Conceptual Justification (The Architect's Mindset)  
Answer the following question in a short, well-reasoned paragraph.
Question: Explain your schema design choice for the tasks collection. You stored the postedBy and assignedTo fields as _id references. What is the main advantage of this approach? What is the main disadvantage compared to embedding the full user and tasker documents inside the task?
(Written Answer Required) Write your paragraph directly in the PDF document.
Submission Guidelines: You will submit a single PDF document. This document must contain clearly labelled screenshots for each task as requested. For the final task, you will write a short paragraph.
