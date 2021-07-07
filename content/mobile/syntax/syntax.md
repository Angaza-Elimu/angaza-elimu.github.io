---
title: "Syntax"
draft: false
---



This explains the different components included in the Mobile application and the functions there in.

> All component code is written in the path /src/app folder


> All assets are stored in the path /src/assets folder

> Environment variables are present in the /src/environment folder




## /src /app

The project pages are built up of the following Screens:

- AccountType
- Assignment
- BottomTab
- Classes
- Home
- HomeScreen
- Landing
- Login
- Notes
- Topics
- Notifications
- OneTimePassword
- PhoneConfirm
- Profile
- Progress
- Quiz


The services used to access the api are under the following:-

> services\authService.js
> services\ContentRetrieval.js
> services\OfflineService.js

The route gurads used to control page access are under the following file:-
 > auth.guard.ts

# App.js
The App.js file is the entry point for our application. It imports some of the necessary modules to help our application work off the bat.

It also creates the SQLite tables needed in order to store our table data.
The SQLite module is used under a library called [expo-sqlite-query-helper][query-helper]



## Create Table

Async function to create new table.</br> _under the hood it runs `CREATE TABLE IF NOT EXIST`_.

```javascript
import { createTable } from 'expo-sqlite-query-helper';
```

```typescript
createTable(tableName: string, columns: { [key: string]: string }); 
```


## Insert

Async function to run insert data into the table, Takes array of objects to insert into specified table.</br> _under the hood it runs `INSERT INTO table (...columns{keys}) values ...(columns{values});`_

```javascript
import { insert } from 'expo-sqlite-query-helper';
```

```typescript
insert(table: string, data: InsertObject[]);
```

`tableName` - Name of the table to insert data.  
`data` - array of objects to insert into table.</br> example: `[{name:"test1",email:"test1@emmail.com"},{name:"test2",email:"test2@exmail.com"}]`.</br> Return promise resolving with
`rowsAffected, insertId, lastQuery`



# Routes

This holds the main routes in our application.

```js

          <Stack.Navigator initialRouteName={this.state.initialPage}>
            <Stack.Screen options={options} name="Landing" component={Landing} />

            <Stack.Screen options={options} name="Login" component={LoginScreen} />

            <Stack.Screen options={options} name="Account" component={AccountType} />

            <Stack.Screen options={options} name="Phone Confirm" component={PhoneConfirm} />

            <Stack.Screen options={options} name="Tab" component={BottomTab} />

            <Stack.Screen options={options} name="One Time Pass" component={OneTimePassword} />
          </Stack.Navigator>
```

The `Stack.Navigator` component accepts following props:

`initialRouteName`
The name of the route to render on first load of the navigator.

`screenOptions`
Default options to use for the screens in the navigator.



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
axios.post('https://staging.angazaelimu.com/api/auth/login', {
                username: this.state.username,
                password: this.state.password
            }).then((resp) => {
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
```javascript
 axios.post('http://staging.angazaelimu.com/api/auth/signup', {
            username: this.state.username,
            password: this.state.password,
            firstname: this.state.firstname,
            lastname: this.state.lastname,
            class: '7',
            phone: this.state.phone,
            learning_level: this.state.learning_level,
            user_type: 'student'
        }).then((resp) => {
```

The above constitutes the request for registration.
Response received is similar to that of login on successful registration

###### Topic Retrieval
---

Topic Request includes a call to the API with a `course_id and level_id` parameter
```ts
getTopics() {
        //fetch or check local sqlite based on configvalue
        console.log(this.state.netState);
        this.setState({ loading: true });
        if (this.state.netState == 'online') {
            DataService.retrieveTopics(this.state.class, this.state.subject_id).then(response => {

                this.setState({ topics: response });
                this.setState({ loading: false });
            })
        } else {
            console.log(
                {
                    class: this.state.class, subject_id: this.state.subject_id
                }
            )
            executeSql('SELECT * FROM topics WHERE class=' + this.state.class + ' AND subject_id=' + this.state.subject_id).then((rows) => {
                
                console.log(rows);
                this.setState({ topics: rows.rows._array });
                this.setState({ loading: false });
            });


        }
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

   [query-helper]: <https://www.npmjs.com/package/expo-sqlite-query-helper>
   [toaster]: <https://www.npmjs.com/package/ngx-toastr>
   [Composer]: <https://getcomposer.org>
   [Angular]: <https://angular.io>
   [Laravel]: <https://laravel.com/>
   [npm]: <https://https://www.npmjs.com/>
   [AngazaSteam]: <https://github.com/Angaza-Elimu/steam-web>
