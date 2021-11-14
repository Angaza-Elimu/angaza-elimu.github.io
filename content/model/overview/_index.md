---
title: "Overview" 
weight: 5
draft: false
pre : "<b>1. </b>"
---


Welcome to the Angaza adaptive learning library documentation.

This project is develoeped by Angaza Elimu and provides a modernized method of categorizing students and predicting perfomance periodically
based on their engagement with the Angaza System and any other system that implements similar features.
The main objective was to build a tool that supplements the perfomance of assessment recommendations on the Angaza Elimu E-Learning Platform.

### How it works

The model is built as a standalone django application with which specific digits based on the following features are sent.
The features used in the situation are the following: - 

- Resource Access  (How much a student interacts with platform resources such as notes and assessments)
- Announcements View (Count of Student Interaction and acting on Platform Notifications)
- Absence (The number of times a student has been absent from the platform for more than x number of days)
- Discussion (The number of times a student asks questions using a discussions feature / Class Forum feature engaging with fellow classmates)


An example on the raw request sent to the API is shown below

        {
            "resource_access": 77,
            "announcements_view":14,
            "abscence":0,
            "discussion":28,
            "raised_hands":50
        }

and a sample response from the system per student gives a specific level according to the bloom's taxonomy and the specific standardized values of the request params sent. Example Below:-

        {
            "error": "0",
            "message": "Successful",
            "prediction": [
                "M"
            ],
            "scaled": [
                [
                    0.10361541892477977,
                    0.667523991293091,
                    -0.8624863170229388,
                    -0.5348551391185068,
                    -0.7993900113485922
                ]
            ]
        }

### USAGE

This classification enables one to have a map of expected students perfomance and what they need to do in order to improve on their perfomance.
It as well predicts the class of the student according to current engagement and the expected outcome after a specific learning period.
It is generally measured against their classroom perfomance and associated with the Bloom's taxonomy pyramid for learning. Therefore it helps suggest content according to the
Bloom's taxonomy pyramid by halving the six classes into 3 general ones L(low - bottom two classes), M(mid - Middle two classes), H(high - Top two classes).
This helps track student progress when ran on the student database regularly. An ideal outcome would be a rise between the 3 classes. However desirably we would be able to flag
the students the model predicts would not do so well.