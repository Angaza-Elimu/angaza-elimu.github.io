---
title: "Architecture" 
weight: 6
draft: false
pre : "<b>2. </b>"
---

The library is built in python3 using the Django Rest Framework to host APIs.
It is made up of a training module and the prediction module.

![](https://res.cloudinary.com/dh2c294kc/image/upload/v1636926135/architect.drawio_qi3bgm.png)

Non-Angaza LMS can host and deploy the solution locally with the diagram showing a typical use-case.
The module built enables the training of data and generation of a new pickled file from which the model weights can be stored to save time 
when it comes to making continuous requests for individual students.

The model stores Non Personally Identifiable data in the form of numbers just based on the student metrics sent.
The data is validated and stored on a structured database whose schema doesn't allow for identifiable personal data.

### Training 
Training data differs from prediction data in that there's an extra field sent in terms of the actual student level based on the platform's scoring.

        {
            "resource_access": 77,
            "announcements_view":14,
            "abscence":0,
            "discussion":28,
            "raised_hands":50,
            "actual_level" "L"
        }

The additional value which is actual_level helps train the model by evaluating the model's output against the user's input. This helps in the training process where a split dataset
where the training and the test are created.

### Technology Stack

The module is built on [Python3](https://www.python.org/downloads/) and [Django Rest Framework](https://www.django-rest-framework.org/) with the dependencies and versions linked [here](https://github.com/Angaza-Elimu/learning_recommendation/blob/main/requirements.txt).

