---
title: "Data Fetching" 
weight: 6
draft: false
---

## fetch_data.py

Within the API folder this file is the main data access entry point which queries the database using a set of rules to give output
based on the response given by the model

#### high_level_questions()

The high_level_questions function takes in three parameters: self, passed_subtopics, and subtopic_id. It returns a list of high-level quiz questions for a given subtopic_id that has been passed.

Inside the function, a list high_level_questions is initialized. A for loop iterates over each passed_subtopic. For each passed_subtopic, SQL queries are used to retrieve the high-level quiz questions of type "create", "evaluate", and "analyze" from the database. The results of each query are appended to the high_level_questions list. Finally, the list is returned.

It is assumed that the models module has been imported and contains a QuizQuestions model class that maps to a database table containing quiz questions, and that the database connection has already been established.


#### failed_subtopic_materials()

The `failed_subtopic_materials` function takes a list of failed subtopics as input and returns a list of relevant notes and materials for each of the failed subtopics. If there are no materials available for a particular subtopic, it returns a message saying that the user has mastered the topic and can choose another topic to study.

The function first initializes an empty list called `failed_subtopic_materials` and then loops through each of the subtopics in the input `failed_subtopics` list. For each subtopic, it queries the database for any notes or materials related to that subtopic using a raw SQL query. The resulting notes are then appended to the `failed_subtopic_materials` list.

After all of the subtopics have been processed, the function checks to see if any materials were actually found by checking the length of the `failed_subtopic_materials` list. If there are no materials, the `action` variable is set to a message indicating that the user has mastered the topic. Otherwise, `action` is set to the `failed_subtopic_materials` list.

Finally, the function returns the `action` variable, which contains either the list of materials or the message about mastering the topic.


#### evaluate_questions()

This format can be used for all other functions that reference retrieval of questions based on the blooms taxonomy from the database.
Replace 'evaluate' with any other question type.

##### Description
This function is responsible for selecting a random "evaluate" type question from the QuizQuestions model based on the current subtopic. 

##### Inputs:
- `mark` - (int) Indicates whether the previous question was answered correctly (1) or incorrectly (0)

##### Outputs:
- Returns a random "evaluate" type question from the QuizQuestions model if there are any available and mark is equal to 1. 
- If there are no "evaluate" type questions available and mark is equal to 1, the function calls the create_questions() function to select a random "create" type question.
- If there are "evaluate" type questions available and mark is equal to 0, the function randomly selects one of the available "evaluate" type questions.
- If there are no "evaluate" type questions available and mark is equal to 0, the function calls the analyze_questions() function to select a random "analyze" type question.
