---
title: "API Endpoints" 
weight: 6
draft: false
pre : "<b>2. </b>"
---

This API endpoint `diagnostic_recommendation` is designed to receive a POST request with user input data and return a recommendation for quiz questions based on the user input.

## API Endpoint

POST /diagnostic_recommendation/

## Request Parameters

| Parameter  | Required | Type   | Description                                            |
| ---------- | -------- | ------ | ------------------------------------------------------ |
| question_level_code  | Yes      | string | The difficulty level of the quiz question. Options are "remember", "understand", "apply", "analyze", "evaluate", and "create". |
| marked     | Yes      | float  | The percentage score the user achieved for a previous quiz. |
| subtopic_id    | Yes      | int    | The ID of the subtopic that the quiz questions should be drawn from. |
| question_id    | No       | int    | The ID of a specific quiz question. Optional. |

## Response Parameters

| Parameter      | Type    | Description                                                                                                           |
| -------------- | ------- | --------------------------------------------------------------------------------------------------------------------- |
| error         | int     | Error code. 0 for no error, 1 for error.                                                                               |
| message        | string  | Message to provide additional information about the response.                                                          |
| prediction     | string  | The difficulty level of quiz questions recommended for the user based on their input.                                  |
| quiz_question  | list    | A list of quiz questions recommended for the user based on their input.                                                |

## Sample Request

```
{
    "question_level_code": "remember",
    "marked": 80,
    "subtopic_id": 123,
    "question_id": 456
}
```

### Sample Response

```
{
    "error": 0,
    "message": "Successful",
    "prediction": "recommend remember questions",
    "quiz_question": [
        {
            "question_id": 123,
            "question_text": "What is the capital city of France?",
            "question_level_code": "remember",
            "subtopic_id": 456,
            "options": [
                "Paris",
                "London",
                "New York",
                "Berlin"
            ]
        },
        {
            "question_id": 456,
            "question_text": "What is the formula for water?",
            "question_level_code": "remember",
            "subtopic_id": 456,
            "options": [
                "H2O",
                "CO2",
                "O2",
                "NaCl"
            ]
        }
    ]
}
```

# Retrieve Diagnostic Recommendation API

## Description
This API retrieves diagnostic recommendation based on the topic_id and answers provided.

## URL
```/api/retrieve_diagnostic_recommendation/```

## Method
POST

## Request Parameters
| Name      | Type    | Mandatory | Description                                           |
| --------- | ------- | --------- | ----------------------------------------------------- |
| topic_id  | integer | yes       | Topic ID to retrieve recommendation for                |
| answers   | array   | yes       | Array of answer objects with marked and question level |

Example of an answer object

```
{
    "question_id": 1,
    "question_level": "remember",
    "marked": 1
}
```

## Function `getQuestionLevelCode`

This function takes a string representing the code for the level of a question and returns an integer representing the corresponding level code.

### Parameters

- `question_code` (string): The code for the level of the question.

### Returns

- An integer representing the level code of the question.

### Level Codes

The function maps the following strings to their corresponding integer codes:

- `remember`: 1
- `understand`: 2
- `apply`: 3
- `analyze`: 4
- `evaluate`: 5
- `create`: 6

If the input code is not recognized, the function returns 0.

## Function Documentation: `low_level_material(questions, prediction)`

This function takes a list of `questions` and a `prediction` as input and returns a dictionary with `subtopics_to_read` and `prediction` keys.

### Arguments:
- `questions`: A list of questions.
- `prediction`: A string that represents the prediction made by the model.

### Returns:
- A dictionary with the following keys:
    - `subtopics_to_read`: A list of subtopic notes to read.
    - `prediction`: The prediction made by the model.


## Function Documentation: `high_level(questions, prediction)`

This function takes a list of `questions` and a `prediction` as input and returns a dictionary with `questions`, `subtopics_to_read`, and `prediction` keys.

### Arguments:
- `questions`: A list of questions.
- `prediction`: A string that represents the prediction made by the model.

### Returns:
- A dictionary with the following keys:
    - `questions`: A list of high-level questions to attempt.
    - `subtopics_to_read`: A list of subtopic notes to read.
    - `prediction`: The prediction made by the model.