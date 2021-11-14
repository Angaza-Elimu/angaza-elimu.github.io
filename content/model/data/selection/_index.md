---
title: "Feature Selection" 

draft: false
---

The aim of feature selection isi to reduce the features that go into the prediction module and take out the irrelevant features in order to achieve a better accuracy.

The method used in Feature Selection for the adaptive learning model is the **Feature Importance** method.

Below are the methods used to determine the main features used on the model which are based on Student Participation and Resource Access.
These features will help us automate the flagging of specific students to teachers and help us recommend the types of content to serve to the students via platform recommendation(notifications, reports and reviews).

For the analysis of the different features we use the following:- 

- BoxPlots
- SwarmPlots (FacetGrid)
- FactorPlots

During the feature selection, student performance was classified into 3 sections, Mid, Low and High. The students were also classified on whether they had failed or not.

### 1. Student Participation

Under the student Participation we have 2 features offered by platform functions.


- Raised Hands(Based on the ask a teacher function).

- Discussions( Based on the class forum function).


#### a. Raised Hands (Ask a teacher)

The following boxplot shows that those that did not do well engaged more with the teacher while the worst performers were the least active.

![Raised Hands Box Plot](https://res.cloudinary.com/dh2c294kc/image/upload/v1625595894/raisedHandsBoxPlot_wftvly.png)

The students are categorized into the classes of failed or not(1 or 0).

The SwarmPlot below shows the 3 different clusters of the students, blue being those with a mid performance(blue), low performance(orange), and those with a high performance(green).

![](https://res.cloudinary.com/dh2c294kc/image/upload/v1625595906/raisedHands_rrcrzw.png)

We can therefore conclude based on the clusters that those with a higher number of teacher interactions performed better than those with a low number of interactions based on the highlighted areas on the swarm plot.

#### b. Discussions

Based on the same categorization of students used in the diagrams representing the raised hands students were classified again depending on their participations in discussions.

The Box Plot below shows that those who engaged more in discussions had a higher chance of passing than those who were inactive.

![](https://res.cloudinary.com/dh2c294kc/image/upload/v1625595893/discussionBoxPlot_rn3rtc.png)

THe swarm plot below clusters this students using the 3 classes to test clarity on the differentiate of perfomance based on the participationo in discussions.

![](https://res.cloudinary.com/dh2c294kc/image/upload/v1625595901/discussion_rfv4dj.png)

Albeit less clear on the specific levels one could argue that you could as well use this feature to identify the different perfomance classes in a dataset.

### 2. Resource Access

The following selected factors had to do with frequency of access of different resources provided by the platform, including platform notes, teacher notes, Quizzes, Assignments and Interactions with the notifications. Another factor taken into account was the amount of time away from the system, whether above 7 days at a time or less than 7days.

#### a. Visited Resources

The following box plot shows findings that differentiate the students performance based on resource access.

![](https://res.cloudinary.com/dh2c294kc/image/upload/v1625595883/visitedResourcesBoxPlot_q0exgj.png)


The biggest margin between high performance and low performance is seen in the measure of visited resources.

The higher the number of visited resources the higher the chances of good performance as shown by the clusters of students.

![](https://res.cloudinary.com/dh2c294kc/image/upload/v1625595889/visitedResourcesSwarm_h7jea9.png)


#### b. Viewed Notifications

THis feature has to do with interaction with push notifications and SMS sent from the platform with a link that contaiins a callback with system recommendations which include a redirect to notes, quizzes and suggested content.

The box plot shows the relations between students that were classified as failed and those classified as a pass according to notification access

![](https://res.cloudinary.com/dh2c294kc/image/upload/v1625595883/notificationViewBoxplot_uxzivd.png)


This shows a student is more likely to fail with little or no interaction with the notifications sent.

The swarm plot show the different student perfomance classificattions and their relation to this feature.

![](https://res.cloudinary.com/dh2c294kc/image/upload/v1625595894/notificationViewSwarm_r2r4kh.png)

#### c. Abscense Days 


This feature was determined to be the most significant when it came to determining/predicting student perfomance.
This is represented by the factor plot below

![](https://res.cloudinary.com/dh2c294kc/image/upload/v1625608484/factorPlot_cdckti.png)

The biggest visual trend can be seen in how frequently the student was absent. Over 90% of the students who did poorly were absent more than seven times, while almost none of the students who did well were absent more than seven times.

We will create a dummy variable for this category, and include it in our model.

![](https://res.cloudinary.com/dh2c294kc/image/upload/v1625608547/absenceBar_gyovcv.png)



These were the main features investigated and found to be able to predict and determine perfomance and thus they will assist in interventions in a student's learning outcome so as to be able to drive a students learning journey to the best possible path.