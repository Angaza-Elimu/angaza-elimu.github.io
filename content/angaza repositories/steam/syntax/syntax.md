---
title: "Syntax Documentation"

draft: false
---

This explains the different components included in the steam web application and the functions there in.

> All component code is written in the path /src/app folder


> All assets are stored in the path /src/assets folder

> Environment variables are present in the /src/environment folder




## /src /app

The project pages are built up of the following components:

- Age-Group
- Code
- Content
- Course
- Login
- Notes
- Project
- Resources
- Signup
- Topics


The services used to access the api are under the following:-

> api.service.ts
auth.service.ts

The route gurads used to control page access are under the following file:-
 > auth.guard.ts

# App.component.ts
The app component.ts file is the entry point for our application. It imports some of the necessary services to help our application work off the bat these include the `ToastrService` and the `ApiService`

`ToastrService` is used to display notifications on the screen. For use reference [ngx-toastr][toaster]

The main function here is to navigate to the expected normally either the login page or the application landing page.

`@angular/router` is used in the constructor to control navigation.

# app-routing.module.ts

This holds the routes in our application.

```sh
const routes: Routes = [
   
      {
        path: 'login',
        component: LoginComponent
      },
      {
        path: 'register',
        component: SignupComponent
      },
      {
        path: 'course',
        component: CourseComponent
      },
      {
        path: 'age-group',
        children: [
          {
            path: ':course',
            component: AgeGroupComponent
          },
          {
            path: ':course/content',
            component: ContentComponent,
            children: [
              {
                path: 'notes',
                component: NotesComponent
              },
              {
                path: 'code',
                component: CodeComponent
              },
              {
                path: 'project',
                component: ProjectComponent
              },
              {
                path: 'resources',
                component: ResourcesComponent
              }
            ]
          }
        ]
      },
      
    
    
  
];
```
All components are defined under the routes constant and the path in order to access the component are shown.

# api.service.ts
This file contains all the calls made to the API. The return type is a json object or an error to the component where it is handled.
 ```sh
      api_url: string = environment.DEV_URL; //API URL definitions referenced from environment file
 ```    
 
##### Functions
---
###### Logging In
---
```js
login(formData) {
    let data = {
      username: formData.username,
      password: formData.password
    }
    console.log(data);

    return this.http.post(this.api_url + '/api/auth/login', data);
  }
```

Login Request with the /api/auth/login endpoint.
Sample Response

```json
{
    "access_token": "TOKEN_TEXT_HERE",
    "token_type": "Bearer",
    "expires_at": "2022-03-03 01:44:16",
    "user": {
        "id": 3856,
        "username": "JOHN_DOE",
        "firstname": "JOHN",
        "lastname": "DOE",
        "email": "johndoe@gmail.com",
        "email_verified_at": null,
        "user_type": "student",
        "school_code": "4801",
        "last_login": {
            "date": "2021-03-03 01:44:16.141295",
            "timezone_type": 3,
            "timezone": "Africa/Nairobi"
        },
        "class": "9",
        "created_at": "2021-01-28 16:29:36",
        "updated_at": "2021-03-03 01:44:16",
        "student_code": "4801171",
        "phone": "0702124316",
        "reset_code": null,
        "phone_confirmation": null,
        "phone_confirmation_status": "unconfirmed",
        "user_account_status": 0
    },
    "login_time": 1614725056,
    "subscription": [
        {
            "id": 1801,
            "user_id": 3856,
            "plan_id": 7,
            "activation_status": 1,
            "expiry_timestamp": "-0001-11-30 00:00:00",
            "started_at": "-0001-11-30 00:00:00",
            "expired": 0,
            "created_at": "2021-01-28 16:29:36",
            "updated_at": "2021-01-28 16:29:36",
            "plan": null
        }
    ]
}
```

###### Registration
---
```js
register(formData){
    let data = {
      username: formData.username,
      password: formData.password,
      first_name: formData.first_name,
      last_name: formData.last_name,
      phone: formData.phone
    }

    return this.http.post(this.api_url + '/api/auth/signup', data);
  }
```

The above constitutes the request for registration.
Response received is similar to that of login on successful registration

###### Topic Retrieval
---

Topic Request includes a call to the API with a `course_id and level_id` parameter
```js
 getTopics(course_id: number, level_id: number) {
    let data = {
      course_id: course_id,
      level_id: level_id
    };
    return this.http.post(this.api_url + '/api/steamTopics', data).pipe(retry(1),
      catchError(this.handleError)
    );
  }
```
Simple request to retrive topics for our curriculum

```json
{
    "topics": [
        {
            "id": 10,
            "subject_id": 8,
            "topic_name": "Natural Numbers",
            "class": 9,
            "created_at": "2019-09-03 17:08:06",
            "updated_at": "2019-09-03 17:08:06"
        },
        {
            "id": 14,
            "subject_id": 8,
            "topic_name": "Greatest Common Divisor",
            "class": 9,
            "created_at": "2019-09-04 09:58:58",
            "updated_at": "2019-09-04 09:58:58"
        },
        {
            "id": 15,
            "subject_id": 8,
            "topic_name": "Least Common Multiple",
            "class": 9,
            "created_at": "2019-09-04 10:00:08",
            "updated_at": "2019-09-04 10:00:08"
        }]
}
```
This is a sample topic response

###### Subtopics
--- 
Subtopic Request includes a call to the API with a `topic_id` parameter
```js
getSubtopics(topic_id) {
    let data = {
      subtopic_id: topic_id
    }
    return this.http.post(this.api_url + '/api/steamSubtopics', data)
      .pipe(retry(1),
        catchError(this.handleError)
      );
  }
```

```json
{
    "subtopics": [
        {
            "id": 10,
            "subject_id": 8,
            "subtopic_name": "Natural Numbers",
            "class": 9,
            "created_at": "2019-09-03 17:08:06",
            "updated_at": "2019-09-03 17:08:06"
        },
        {
            "id": 14,
            "subject_id": 8,
            "subtopic_name": "Greatest Common Divisor",
            "class": 9,
            "created_at": "2019-09-04 09:58:58",
            "updated_at": "2019-09-04 09:58:58"
        },
        {
            "id": 15,
            "subject_id": 8,
            "subtopic_name": "Least Common Multiple",
            "class": 9,
            "created_at": "2019-09-04 10:00:08",
            "updated_at": "2019-09-04 10:00:08"
        }]
}
``` 

Sample Subtopic Reponse above
 
 


## Development

Want to contribute? Great!

For a great place to start visit our repositories and have a look at the feature requests and the issues.

Fork and create a branch on the feature/issue you will be working on.

Create a pull request... we will review and be in contact.

For other clarifications you can contact info@angazaelimu.com

Angaza Steam uses Webpack for fast developing.
Make a change in your file and instantaneously see your updates in the browser!


#### Building for source

For production release:

```sh
ng build --prod
```





> Note: `--capt-add=SYS-ADMIN` is required for PDF rendering.



## License

LGPL 3.0

**Happy Learning**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [toaster]: <https://www.npmjs.com/package/ngx-toastr>
   [Composer]: <https://getcomposer.org>
   [Angular]: <https://angular.io>
   [Laravel]: <https://laravel.com/>
   [npm]: <https://https://www.npmjs.com/>
   [AngazaSteam]: <https://github.com/Angaza-Elimu/steam-web>
