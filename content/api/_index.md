---
title: "API Endpoints"

draft: false
---

<!-- START_INFO -->


<!-- START_416b299d72b39622b6c09eb54d700da9 -->
## Show the application dashboard.

> Example request:

```bash
curl -X GET \
    -G "http://localhost/apilogs" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/apilogs"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
null
```

### HTTP Request
`GET apilogs`


<!-- END_416b299d72b39622b6c09eb54d700da9 -->

<!-- START_746515ae6e54ff0687a5d2f1caa33150 -->
## apilogs/delete
> Example request:

```bash
curl -X DELETE \
    "http://localhost/apilogs/delete" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/apilogs/delete"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "DELETE",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`DELETE apilogs/delete`


<!-- END_746515ae6e54ff0687a5d2f1caa33150 -->

<!-- START_0c068b4037fb2e47e71bd44bd36e3e2a -->
## Authorize a client to access the user&#039;s account.

> Example request:

```bash
curl -X GET \
    -G "http://localhost/oauth/authorize" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/oauth/authorize"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET oauth/authorize`


<!-- END_0c068b4037fb2e47e71bd44bd36e3e2a -->

<!-- START_e48cc6a0b45dd21b7076ab2c03908687 -->
## Approve the authorization request.

> Example request:

```bash
curl -X POST \
    "http://localhost/oauth/authorize" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/oauth/authorize"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST oauth/authorize`


<!-- END_e48cc6a0b45dd21b7076ab2c03908687 -->

<!-- START_de5d7581ef1275fce2a229b6b6eaad9c -->
## Deny the authorization request.

> Example request:

```bash
curl -X DELETE \
    "http://localhost/oauth/authorize" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/oauth/authorize"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "DELETE",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`DELETE oauth/authorize`


<!-- END_de5d7581ef1275fce2a229b6b6eaad9c -->

<!-- START_a09d20357336aa979ecd8e3972ac9168 -->
## Authorize a client to access the user&#039;s account.

> Example request:

```bash
curl -X POST \
    "http://localhost/oauth/token" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/oauth/token"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST oauth/token`


<!-- END_a09d20357336aa979ecd8e3972ac9168 -->

<!-- START_d6a56149547e03307199e39e03e12d1c -->
## Get all of the authorized tokens for the authenticated user.

> Example request:

```bash
curl -X GET \
    -G "http://localhost/oauth/tokens" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/oauth/tokens"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET oauth/tokens`


<!-- END_d6a56149547e03307199e39e03e12d1c -->

<!-- START_a9a802c25737cca5324125e5f60b72a5 -->
## Delete the given token.

> Example request:

```bash
curl -X DELETE \
    "http://localhost/oauth/tokens/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/oauth/tokens/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "DELETE",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`DELETE oauth/tokens/{token_id}`


<!-- END_a9a802c25737cca5324125e5f60b72a5 -->

<!-- START_abe905e69f5d002aa7d26f433676d623 -->
## Get a fresh transient token cookie for the authenticated user.

> Example request:

```bash
curl -X POST \
    "http://localhost/oauth/token/refresh" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/oauth/token/refresh"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST oauth/token/refresh`


<!-- END_abe905e69f5d002aa7d26f433676d623 -->

<!-- START_babcfe12d87b8708f5985e9d39ba8f2c -->
## Get all of the clients for the authenticated user.

> Example request:

```bash
curl -X GET \
    -G "http://localhost/oauth/clients" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/oauth/clients"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET oauth/clients`


<!-- END_babcfe12d87b8708f5985e9d39ba8f2c -->

<!-- START_9eabf8d6e4ab449c24c503fcb42fba82 -->
## Store a new client.

> Example request:

```bash
curl -X POST \
    "http://localhost/oauth/clients" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/oauth/clients"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST oauth/clients`


<!-- END_9eabf8d6e4ab449c24c503fcb42fba82 -->

<!-- START_784aec390a455073fc7464335c1defa1 -->
## Update the given client.

> Example request:

```bash
curl -X PUT \
    "http://localhost/oauth/clients/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/oauth/clients/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "PUT",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`PUT oauth/clients/{client_id}`


<!-- END_784aec390a455073fc7464335c1defa1 -->

<!-- START_1f65a511dd86ba0541d7ba13ca57e364 -->
## Delete the given client.

> Example request:

```bash
curl -X DELETE \
    "http://localhost/oauth/clients/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/oauth/clients/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "DELETE",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`DELETE oauth/clients/{client_id}`


<!-- END_1f65a511dd86ba0541d7ba13ca57e364 -->

<!-- START_9e281bd3a1eb1d9eb63190c8effb607c -->
## Get all of the available scopes for the application.

> Example request:

```bash
curl -X GET \
    -G "http://localhost/oauth/scopes" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/oauth/scopes"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET oauth/scopes`


<!-- END_9e281bd3a1eb1d9eb63190c8effb607c -->

<!-- START_9b2a7699ce6214a79e0fd8107f8b1c9e -->
## Get all of the personal access tokens for the authenticated user.

> Example request:

```bash
curl -X GET \
    -G "http://localhost/oauth/personal-access-tokens" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/oauth/personal-access-tokens"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET oauth/personal-access-tokens`


<!-- END_9b2a7699ce6214a79e0fd8107f8b1c9e -->

<!-- START_a8dd9c0a5583742e671711f9bb3ee406 -->
## Create a new personal access token for the user.

> Example request:

```bash
curl -X POST \
    "http://localhost/oauth/personal-access-tokens" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/oauth/personal-access-tokens"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST oauth/personal-access-tokens`


<!-- END_a8dd9c0a5583742e671711f9bb3ee406 -->

<!-- START_bae65df80fd9d72a01439241a9ea20d0 -->
## Delete the given token.

> Example request:

```bash
curl -X DELETE \
    "http://localhost/oauth/personal-access-tokens/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/oauth/personal-access-tokens/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "DELETE",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`DELETE oauth/personal-access-tokens/{token_id}`


<!-- END_bae65df80fd9d72a01439241a9ea20d0 -->

<!-- START_a925a8d22b3615f12fca79456d286859 -->
## Login user and create token

> Example request:

```bash
curl -X POST \
    "http://localhost/api/auth/login" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/auth/login"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/auth/login`


<!-- END_a925a8d22b3615f12fca79456d286859 -->

<!-- START_9357c0a600c785fe4f708897facae8b8 -->
## Create user

> Example request:

```bash
curl -X POST \
    "http://localhost/api/auth/signup" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/auth/signup"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/auth/signup`


<!-- END_9357c0a600c785fe4f708897facae8b8 -->

<!-- START_d20d3bc6f1aeec95b2ced061348bcc14 -->
## api/auth/loginAdmin
> Example request:

```bash
curl -X POST \
    "http://localhost/api/auth/loginAdmin" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/auth/loginAdmin"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/auth/loginAdmin`


<!-- END_d20d3bc6f1aeec95b2ced061348bcc14 -->

<!-- START_ae317991e6921a111f1ee34194a3ab87 -->
## api/auth/resetByEmail
> Example request:

```bash
curl -X POST \
    "http://localhost/api/auth/resetByEmail" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/auth/resetByEmail"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/auth/resetByEmail`


<!-- END_ae317991e6921a111f1ee34194a3ab87 -->

<!-- START_e6cd0be2a3cfa51ee542c74289ab149c -->
## api/auth/resetByPhone
> Example request:

```bash
curl -X POST \
    "http://localhost/api/auth/resetByPhone" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/auth/resetByPhone"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/auth/resetByPhone`


<!-- END_e6cd0be2a3cfa51ee542c74289ab149c -->

<!-- START_122ad09ae420ddc84da53a5f59d9871c -->
## api/auth/addUser
> Example request:

```bash
curl -X POST \
    "http://localhost/api/auth/addUser" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/auth/addUser"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/auth/addUser`


<!-- END_122ad09ae420ddc84da53a5f59d9871c -->

<!-- START_c9eaca7ce3c6473c7b8d2ed5df0d92c4 -->
## api/auth/confirmPhone
> Example request:

```bash
curl -X POST \
    "http://localhost/api/auth/confirmPhone" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/auth/confirmPhone"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/auth/confirmPhone`


<!-- END_c9eaca7ce3c6473c7b8d2ed5df0d92c4 -->

<!-- START_65025b82114148f935e2a31f1e53a28d -->
## api/auth/requestConfirmation
> Example request:

```bash
curl -X POST \
    "http://localhost/api/auth/requestConfirmation" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/auth/requestConfirmation"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/auth/requestConfirmation`


<!-- END_65025b82114148f935e2a31f1e53a28d -->

<!-- START_1765cf12fac526f5d7efe60d246a3162 -->
## api/steamLevels
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/steamLevels" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/steamLevels"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET api/steamLevels`


<!-- END_1765cf12fac526f5d7efe60d246a3162 -->

<!-- START_3acb78936638838dc8374822ea5fd2e3 -->
## api/steamTopics
> Example request:

```bash
curl -X POST \
    "http://localhost/api/steamTopics" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/steamTopics"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/steamTopics`


<!-- END_3acb78936638838dc8374822ea5fd2e3 -->

<!-- START_a7498f8032ae0b645f081d75a14e7102 -->
## api/steamNotes
> Example request:

```bash
curl -X POST \
    "http://localhost/api/steamNotes" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/steamNotes"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/steamNotes`


<!-- END_a7498f8032ae0b645f081d75a14e7102 -->

<!-- START_efd0a43e2fd38c9b3ea79b6d61d8b5f1 -->
## api/testPayment
> Example request:

```bash
curl -X POST \
    "http://localhost/api/testPayment" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/testPayment"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/testPayment`


<!-- END_efd0a43e2fd38c9b3ea79b6d61d8b5f1 -->

<!-- START_2877369e544fc776cc23ecf38775d086 -->
## api/generateToken
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/generateToken" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/generateToken"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET api/generateToken`


<!-- END_2877369e544fc776cc23ecf38775d086 -->

<!-- START_5775966ed3d045c40aca6354359fc940 -->
## api/stk_callback
> Example request:

```bash
curl -X POST \
    "http://localhost/api/stk_callback" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/stk_callback"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/stk_callback`


<!-- END_5775966ed3d045c40aca6354359fc940 -->

<!-- START_fc1e4f6a697e3c48257de845299b71d5 -->
## api/users
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/users" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/users"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



```

### HTTP Request
`GET api/users`


<!-- END_fc1e4f6a697e3c48257de845299b71d5 -->

<!-- START_b03df3b941ec8d247cc9f10f986ce287 -->
## api/subscribeToPlan
> Example request:

```bash
curl -X POST \
    "http://localhost/api/subscribeToPlan" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/subscribeToPlan"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/subscribeToPlan`


<!-- END_b03df3b941ec8d247cc9f10f986ce287 -->

<!-- START_00e7e21641f05de650dbe13f242c6f2c -->
## Logout user (Revoke the token)

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/logout" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/logout"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/logout`


<!-- END_00e7e21641f05de650dbe13f242c6f2c -->

<!-- START_2b6e5a4b188cb183c7e59558cce36cb6 -->
## Get the authenticated User

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/user" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/user"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/user`


<!-- END_2b6e5a4b188cb183c7e59558cce36cb6 -->

<!-- START_955690e63c7ef6354797f0bea7787a39 -->
## api/userLogs
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/userLogs" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/userLogs"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/userLogs`


<!-- END_955690e63c7ef6354797f0bea7787a39 -->

<!-- START_dab60828c895168bd7bde2a72a4c1739 -->
## api/getPrimaryTopics
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getPrimaryTopics" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getPrimaryTopics"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getPrimaryTopics`


<!-- END_dab60828c895168bd7bde2a72a4c1739 -->

<!-- START_d47f95979e2f159b6e5273fedff929b6 -->
## api/createPrimaryTopic
> Example request:

```bash
curl -X POST \
    "http://localhost/api/createPrimaryTopic" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/createPrimaryTopic"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/createPrimaryTopic`


<!-- END_d47f95979e2f159b6e5273fedff929b6 -->

<!-- START_8455e8703db5103ce56ea7e2a98a49c7 -->
## api/updateData
> Example request:

```bash
curl -X POST \
    "http://localhost/api/updateData" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/updateData"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/updateData`


<!-- END_8455e8703db5103ce56ea7e2a98a49c7 -->

<!-- START_e4a1945a1afd75057f693e9a8c0f6966 -->
## api/getUserDetails
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/getUserDetails" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getUserDetails"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/getUserDetails`


<!-- END_e4a1945a1afd75057f693e9a8c0f6966 -->

<!-- START_ed164a6ae0cac4e4f7a78ca8013939c6 -->
## api/addStudent
> Example request:

```bash
curl -X POST \
    "http://localhost/api/addStudent" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/addStudent"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/addStudent`


<!-- END_ed164a6ae0cac4e4f7a78ca8013939c6 -->

<!-- START_e34cc0ef4f19626dbf4060b6e7bd0f78 -->
## api/createStudent
> Example request:

```bash
curl -X POST \
    "http://localhost/api/createStudent" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/createStudent"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/createStudent`


<!-- END_e34cc0ef4f19626dbf4060b6e7bd0f78 -->

<!-- START_54a38bcd4e9a472cea6ef0c1d8e361d1 -->
## api/getTopics
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getTopics" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getTopics"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getTopics`


<!-- END_54a38bcd4e9a472cea6ef0c1d8e361d1 -->

<!-- START_b6ae39f20936d65d5700ac730a80c1ab -->
## api/createTopic
> Example request:

```bash
curl -X POST \
    "http://localhost/api/createTopic" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/createTopic"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/createTopic`


<!-- END_b6ae39f20936d65d5700ac730a80c1ab -->

<!-- START_8627a3be8bb1cd2bfd17997d22076dfe -->
## api/createSubtopic
> Example request:

```bash
curl -X POST \
    "http://localhost/api/createSubtopic" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/createSubtopic"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/createSubtopic`


<!-- END_8627a3be8bb1cd2bfd17997d22076dfe -->

<!-- START_42cad04dc7c77d4cfd0a7be50f1a9582 -->
## api/getSubtopics
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getSubtopics" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getSubtopics"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getSubtopics`


<!-- END_42cad04dc7c77d4cfd0a7be50f1a9582 -->

<!-- START_fb1fd891a0f4b37d338cb72701c55525 -->
## api/getSubtopicNotes
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getSubtopicNotes" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getSubtopicNotes"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getSubtopicNotes`


<!-- END_fb1fd891a0f4b37d338cb72701c55525 -->

<!-- START_046de5bdd17d13fa06ad585a5086cf16 -->
## api/createLearningPlan
> Example request:

```bash
curl -X POST \
    "http://localhost/api/createLearningPlan" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/createLearningPlan"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/createLearningPlan`


<!-- END_046de5bdd17d13fa06ad585a5086cf16 -->

<!-- START_889aa7d2e504156f62c10724ed160808 -->
## api/lessonPlan
> Example request:

```bash
curl -X POST \
    "http://localhost/api/lessonPlan" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/lessonPlan"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/lessonPlan`


<!-- END_889aa7d2e504156f62c10724ed160808 -->

<!-- START_570152d1499535cc27a925d05f637158 -->
## api/createAssignmentQuestion
> Example request:

```bash
curl -X POST \
    "http://localhost/api/createAssignmentQuestion" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/createAssignmentQuestion"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/createAssignmentQuestion`


<!-- END_570152d1499535cc27a925d05f637158 -->

<!-- START_b71e7e953e2f1014dbc5efe57fd9ee98 -->
## api/createQuizQuestion
> Example request:

```bash
curl -X POST \
    "http://localhost/api/createQuizQuestion" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/createQuizQuestion"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/createQuizQuestion`


<!-- END_b71e7e953e2f1014dbc5efe57fd9ee98 -->

<!-- START_991e6abdcd1ca7f510799ec2608f7e68 -->
## api/getQuizQuestions
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getQuizQuestions" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getQuizQuestions"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getQuizQuestions`


<!-- END_991e6abdcd1ca7f510799ec2608f7e68 -->

<!-- START_83d9182ed81a9264f1c37713029abbe0 -->
## api/answerQuestion
> Example request:

```bash
curl -X POST \
    "http://localhost/api/answerQuestion" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/answerQuestion"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/answerQuestion`


<!-- END_83d9182ed81a9264f1c37713029abbe0 -->

<!-- START_521c4c09757d9930efe9d6a0236a9e5a -->
## api/getQuiz
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getQuiz" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getQuiz"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getQuiz`


<!-- END_521c4c09757d9930efe9d6a0236a9e5a -->

<!-- START_1acfb46ed17d368d5e941d7e24164034 -->
## api/createQuestionResponse
> Example request:

```bash
curl -X POST \
    "http://localhost/api/createQuestionResponse" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/createQuestionResponse"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/createQuestionResponse`


<!-- END_1acfb46ed17d368d5e941d7e24164034 -->

<!-- START_3c05b74b8cc8a89b0152d0e43e554f09 -->
## api/createOpenEnded
> Example request:

```bash
curl -X POST \
    "http://localhost/api/createOpenEnded" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/createOpenEnded"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/createOpenEnded`


<!-- END_3c05b74b8cc8a89b0152d0e43e554f09 -->

<!-- START_e843529f3fb3eec9a7c27a9594e88f1c -->
## api/createRevisionQuestion
> Example request:

```bash
curl -X POST \
    "http://localhost/api/createRevisionQuestion" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/createRevisionQuestion"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/createRevisionQuestion`


<!-- END_e843529f3fb3eec9a7c27a9594e88f1c -->

<!-- START_dbea4607ee9e7d058e5f3911550145d6 -->
## api/createRevisionOpenEndedQuestion
> Example request:

```bash
curl -X POST \
    "http://localhost/api/createRevisionOpenEndedQuestion" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/createRevisionOpenEndedQuestion"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/createRevisionOpenEndedQuestion`


<!-- END_dbea4607ee9e7d058e5f3911550145d6 -->

<!-- START_41d32180ccb3019db53014113065ed04 -->
## api/getRevisionQuestions
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getRevisionQuestions" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getRevisionQuestions"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getRevisionQuestions`


<!-- END_41d32180ccb3019db53014113065ed04 -->

<!-- START_198e798ea054fff0d499de4f15a5e58a -->
## api/getOpenEndedRevisionQuestions
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getOpenEndedRevisionQuestions" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getOpenEndedRevisionQuestions"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getOpenEndedRevisionQuestions`


<!-- END_198e798ea054fff0d499de4f15a5e58a -->

<!-- START_951d1055aac1c92ec94192f945f572f4 -->
## api/answerRevisionQuestion
> Example request:

```bash
curl -X POST \
    "http://localhost/api/answerRevisionQuestion" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/answerRevisionQuestion"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/answerRevisionQuestion`


<!-- END_951d1055aac1c92ec94192f945f572f4 -->

<!-- START_fde28e55e5b7b3afcfd54534a16ba382 -->
## api/openEndedRevisionAnswer
> Example request:

```bash
curl -X POST \
    "http://localhost/api/openEndedRevisionAnswer" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/openEndedRevisionAnswer"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/openEndedRevisionAnswer`


<!-- END_fde28e55e5b7b3afcfd54534a16ba382 -->

<!-- START_84b634189c956f6ff8767eb77647eb0e -->
## api/getAssignmentQuestionsTeacher
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getAssignmentQuestionsTeacher" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getAssignmentQuestionsTeacher"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getAssignmentQuestionsTeacher`


<!-- END_84b634189c956f6ff8767eb77647eb0e -->

<!-- START_76c44eeded886650b265ff1bada35d49 -->
## api/getAnswers
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getAnswers" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getAnswers"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getAnswers`


<!-- END_76c44eeded886650b265ff1bada35d49 -->

<!-- START_1c739bbd1ec6259a14032dac8207bac1 -->
## api/postAngazaNotes
> Example request:

```bash
curl -X POST \
    "http://localhost/api/postAngazaNotes" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/postAngazaNotes"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/postAngazaNotes`


<!-- END_1c739bbd1ec6259a14032dac8207bac1 -->

<!-- START_7097e3542010c1d222a1aafa5bd41f85 -->
## api/postTeacherNotes
> Example request:

```bash
curl -X POST \
    "http://localhost/api/postTeacherNotes" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/postTeacherNotes"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/postTeacherNotes`


<!-- END_7097e3542010c1d222a1aafa5bd41f85 -->

<!-- START_9a2a4a4222c7aa4a0642bc259b034f4e -->
## api/getTeachersNotes
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getTeachersNotes" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getTeachersNotes"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getTeachersNotes`


<!-- END_9a2a4a4222c7aa4a0642bc259b034f4e -->

<!-- START_955a246b1322842814da3da1811a4776 -->
## api/createSubject
> Example request:

```bash
curl -X POST \
    "http://localhost/api/createSubject" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/createSubject"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/createSubject`


<!-- END_955a246b1322842814da3da1811a4776 -->

<!-- START_07d4536a2fa1a3fa2770689ee60bb666 -->
## api/getSubjects
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/getSubjects" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getSubjects"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/getSubjects`


<!-- END_07d4536a2fa1a3fa2770689ee60bb666 -->

<!-- START_49263be7879b25bc2d15fdbcdda73009 -->
## api/getSubjectByName
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getSubjectByName" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getSubjectByName"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getSubjectByName`


<!-- END_49263be7879b25bc2d15fdbcdda73009 -->

<!-- START_0f77e22206d8148ad631f90d662bf2a0 -->
## api/commitSession
> Example request:

```bash
curl -X POST \
    "http://localhost/api/commitSession" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/commitSession"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/commitSession`


<!-- END_0f77e22206d8148ad631f90d662bf2a0 -->

<!-- START_0b828966a9f31e695693fe9650b70eb1 -->
## api/userData
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/userData" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/userData"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/userData`


<!-- END_0b828966a9f31e695693fe9650b70eb1 -->

<!-- START_a6da3c3b1d75b625329a4bead924c026 -->
## api/studentAnalytics
> Example request:

```bash
curl -X POST \
    "http://localhost/api/studentAnalytics" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/studentAnalytics"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/studentAnalytics`


<!-- END_a6da3c3b1d75b625329a4bead924c026 -->

<!-- START_700cd9ab61320ed1574f8ed8f0aba5f6 -->
## api/assignmentAnalytics
> Example request:

```bash
curl -X POST \
    "http://localhost/api/assignmentAnalytics" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/assignmentAnalytics"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/assignmentAnalytics`


<!-- END_700cd9ab61320ed1574f8ed8f0aba5f6 -->

<!-- START_a3406b5fc3234f9a4e89ad556f512cb4 -->
## api/teachersAnalytics
> Example request:

```bash
curl -X POST \
    "http://localhost/api/teachersAnalytics" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/teachersAnalytics"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/teachersAnalytics`


<!-- END_a3406b5fc3234f9a4e89ad556f512cb4 -->

<!-- START_4892d90804dc5f0349bd866bf6c2b360 -->
## api/getClasses
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/getClasses" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getClasses"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/getClasses`


<!-- END_4892d90804dc5f0349bd866bf6c2b360 -->

<!-- START_24b08ab2788b6c5cfd9ba20310e27783 -->
## api/getStudentClasses
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getStudentClasses" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getStudentClasses"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getStudentClasses`


<!-- END_24b08ab2788b6c5cfd9ba20310e27783 -->

<!-- START_7bd9abffb07b1c230370af56a9095377 -->
## api/getTopicByLearningSystem
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getTopicByLearningSystem" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getTopicByLearningSystem"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getTopicByLearningSystem`


<!-- END_7bd9abffb07b1c230370af56a9095377 -->

<!-- START_d285b6696e653eba8e99de0b4beef309 -->
## api/createClass
> Example request:

```bash
curl -X POST \
    "http://localhost/api/createClass" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/createClass"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/createClass`


<!-- END_d285b6696e653eba8e99de0b4beef309 -->

<!-- START_199e313f42c624c7c70a8e2e9e70cea5 -->
## api/getClassByLearningSystem
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getClassByLearningSystem" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getClassByLearningSystem"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getClassByLearningSystem`


<!-- END_199e313f42c624c7c70a8e2e9e70cea5 -->

<!-- START_ab8a9316a28a0ef908cd4c5306f9c402 -->
## api/getAllTopics
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/getAllTopics" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getAllTopics"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/getAllTopics`


<!-- END_ab8a9316a28a0ef908cd4c5306f9c402 -->

<!-- START_073046993fe8bad79c8f214d2e917ed9 -->
## api/getAllSubtopics
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/getAllSubtopics" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getAllSubtopics"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/getAllSubtopics`


<!-- END_073046993fe8bad79c8f214d2e917ed9 -->

<!-- START_4cf4662a742c9347e19ff3641efe876f -->
## api/createSchool
> Example request:

```bash
curl -X POST \
    "http://localhost/api/createSchool" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/createSchool"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/createSchool`


<!-- END_4cf4662a742c9347e19ff3641efe876f -->

<!-- START_bf547b645a64771c5e9fbac35fd07c7f -->
## api/createCounty
> Example request:

```bash
curl -X POST \
    "http://localhost/api/createCounty" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/createCounty"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/createCounty`


<!-- END_bf547b645a64771c5e9fbac35fd07c7f -->

<!-- START_494a0ac6aabf83cdcb18c7b5bb0692d2 -->
## api/createTeacher
> Example request:

```bash
curl -X POST \
    "http://localhost/api/createTeacher" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/createTeacher"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/createTeacher`


<!-- END_494a0ac6aabf83cdcb18c7b5bb0692d2 -->

<!-- START_f6ae82e14b8de1b5d9d05074f5ed7cd8 -->
## api/getCounties
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/getCounties" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getCounties"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/getCounties`


<!-- END_f6ae82e14b8de1b5d9d05074f5ed7cd8 -->

<!-- START_f3fb45d2a4ed7f2311329ed913ead6b4 -->
## api/getSchools
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/getSchools" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getSchools"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/getSchools`


<!-- END_f3fb45d2a4ed7f2311329ed913ead6b4 -->

<!-- START_44c59a1b85d6055924b1aeeef14fad9c -->
## api/submitRevision
> Example request:

```bash
curl -X POST \
    "http://localhost/api/submitRevision" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/submitRevision"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/submitRevision`


<!-- END_44c59a1b85d6055924b1aeeef14fad9c -->

<!-- START_0c5f24a5584e510a6f965a7caa91caf0 -->
## api/submitRevisionOpenEndedAttempt
> Example request:

```bash
curl -X POST \
    "http://localhost/api/submitRevisionOpenEndedAttempt" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/submitRevisionOpenEndedAttempt"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/submitRevisionOpenEndedAttempt`


<!-- END_0c5f24a5584e510a6f965a7caa91caf0 -->

<!-- START_97a8acb46faeaf2c96b2a8ec5e899d3d -->
## api/getRevisionAttempt
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getRevisionAttempt" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getRevisionAttempt"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getRevisionAttempt`


<!-- END_97a8acb46faeaf2c96b2a8ec5e899d3d -->

<!-- START_66b5a26ad783da3f36ff2709a81beb4c -->
## api/getSecondaryRevisionAttempt
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getSecondaryRevisionAttempt" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getSecondaryRevisionAttempt"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getSecondaryRevisionAttempt`


<!-- END_66b5a26ad783da3f36ff2709a81beb4c -->

<!-- START_330f8228fc295e982289542b1d1fb96d -->
## api/getTopicsFromClass
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getTopicsFromClass" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getTopicsFromClass"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getTopicsFromClass`


<!-- END_330f8228fc295e982289542b1d1fb96d -->

<!-- START_03f96155b738e7e1a668244fa77d0ae3 -->
## api/getSubtopicFromTopic
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getSubtopicFromTopic" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getSubtopicFromTopic"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getSubtopicFromTopic`


<!-- END_03f96155b738e7e1a668244fa77d0ae3 -->

<!-- START_5e8cfb1dd32d64903fc57399f5a97b3b -->
## api/getSubtopicsWhereTopic
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getSubtopicsWhereTopic" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getSubtopicsWhereTopic"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getSubtopicsWhereTopic`


<!-- END_5e8cfb1dd32d64903fc57399f5a97b3b -->

<!-- START_8207fdecd9f8287052ef6200433904c0 -->
## api/getStudentsFromSchool
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getStudentsFromSchool" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getStudentsFromSchool"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getStudentsFromSchool`


<!-- END_8207fdecd9f8287052ef6200433904c0 -->

<!-- START_55e3d0b94b0caed7fdc365e896c235ab -->
## api/getTeachers
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/getTeachers" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getTeachers"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/getTeachers`


<!-- END_55e3d0b94b0caed7fdc365e896c235ab -->

<!-- START_26b1a05ddedd742922a953933154ab8d -->
## api/getAllSchools
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/getAllSchools" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getAllSchools"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/getAllSchools`


<!-- END_26b1a05ddedd742922a953933154ab8d -->

<!-- START_b4601361f68ed77943adee9bbd72ede5 -->
## api/getAllStudents
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/getAllStudents" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getAllStudents"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/getAllStudents`


<!-- END_b4601361f68ed77943adee9bbd72ede5 -->

<!-- START_c5b6d1645679dc1e3fe5c31ee07c9965 -->
## api/getStudentSubtopicResults
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getStudentSubtopicResults" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getStudentSubtopicResults"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getStudentSubtopicResults`


<!-- END_c5b6d1645679dc1e3fe5c31ee07c9965 -->

<!-- START_b317e8d652a885aaebf0ac55cc90f04f -->
## api/submitQuiz
> Example request:

```bash
curl -X POST \
    "http://localhost/api/submitQuiz" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/submitQuiz"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/submitQuiz`


<!-- END_b317e8d652a885aaebf0ac55cc90f04f -->

<!-- START_247cd245eb16588edc3788af3d853c44 -->
## api/submitAssignment
> Example request:

```bash
curl -X POST \
    "http://localhost/api/submitAssignment" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/submitAssignment"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/submitAssignment`


<!-- END_247cd245eb16588edc3788af3d853c44 -->

<!-- START_bf0681086665ace22e0c0d009fab0cac -->
## api/getAttempt
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getAttempt" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getAttempt"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getAttempt`


<!-- END_bf0681086665ace22e0c0d009fab0cac -->

<!-- START_b8df8b000fb163fc60d8269e260bdc0b -->
## api/getStudents
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getStudents" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getStudents"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getStudents`


<!-- END_b8df8b000fb163fc60d8269e260bdc0b -->

<!-- START_7163ee68b870240bb3f55557ea24ee32 -->
## api/studentWithClassification
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/studentWithClassification" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/studentWithClassification"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/studentWithClassification`


<!-- END_7163ee68b870240bb3f55557ea24ee32 -->

<!-- START_a65d77feb7aacdd2b6d1215503d7c641 -->
## Ask Questions Endpoint

> Example request:

```bash
curl -X POST \
    "http://localhost/api/askQuestion" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/askQuestion"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/askQuestion`


<!-- END_a65d77feb7aacdd2b6d1215503d7c641 -->

<!-- START_9306aabaebe55377a5e038bfcb7efaa2 -->
## api/getQueries
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getQueries" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getQueries"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getQueries`


<!-- END_9306aabaebe55377a5e038bfcb7efaa2 -->

<!-- START_b15ede54c327a429a46b21704ee9ad19 -->
## api/getSchoolStudentsTeachers
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getSchoolStudentsTeachers" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getSchoolStudentsTeachers"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getSchoolStudentsTeachers`


<!-- END_b15ede54c327a429a46b21704ee9ad19 -->

<!-- START_52384e3f484cc05fd4135a89e85227d1 -->
## api/getUserActivity
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getUserActivity" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getUserActivity"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getUserActivity`


<!-- END_52384e3f484cc05fd4135a89e85227d1 -->

<!-- START_6fc7d051067259a3ec7a6779da7b8f91 -->
## api/createSenderList
> Example request:

```bash
curl -X POST \
    "http://localhost/api/createSenderList" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/createSenderList"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/createSenderList`


<!-- END_6fc7d051067259a3ec7a6779da7b8f91 -->

<!-- START_400b1d6f1f3b56e3b5068ef28ebf37c4 -->
## api/getSenderLists
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/getSenderLists" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getSenderLists"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/getSenderLists`


<!-- END_400b1d6f1f3b56e3b5068ef28ebf37c4 -->

<!-- START_ba2f11c8cfcd4eb23e44aca4021c25d7 -->
## api/getSenderListMembers
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/getSenderListMembers" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getSenderListMembers"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/getSenderListMembers`


<!-- END_ba2f11c8cfcd4eb23e44aca4021c25d7 -->

<!-- START_0245d2e6d6253bff5b98e16684f32e36 -->
## api/sendSingleSMS
> Example request:

```bash
curl -X POST \
    "http://localhost/api/sendSingleSMS" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/sendSingleSMS"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/sendSingleSMS`


<!-- END_0245d2e6d6253bff5b98e16684f32e36 -->

<!-- START_cfe38ce7617043713f41c5a50aafa8cf -->
## api/sendMultipleSMS
> Example request:

```bash
curl -X POST \
    "http://localhost/api/sendMultipleSMS" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/sendMultipleSMS"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/sendMultipleSMS`


<!-- END_cfe38ce7617043713f41c5a50aafa8cf -->

<!-- START_3b8e32991db5b3977168462149a3e6f0 -->
## api/getUsers
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/getUsers" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getUsers"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/getUsers`


<!-- END_3b8e32991db5b3977168462149a3e6f0 -->

<!-- START_52a75e230a4f4caed4c0875251f05b81 -->
## api/addSenders
> Example request:

```bash
curl -X POST \
    "http://localhost/api/addSenders" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/addSenders"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/addSenders`


<!-- END_52a75e230a4f4caed4c0875251f05b81 -->

<!-- START_279992c7f166a5cfb5328c935da44df3 -->
## api/date_test
> Example request:

```bash
curl -X POST \
    "http://localhost/api/date_test" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/date_test"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/date_test`


<!-- END_279992c7f166a5cfb5328c935da44df3 -->

<!-- START_ffd5e027323f2a10a6850550c19e46bc -->
## api/getStudentActivityData
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/getStudentActivityData" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getStudentActivityData"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/getStudentActivityData`


<!-- END_ffd5e027323f2a10a6850550c19e46bc -->

<!-- START_3eb0e6e8581c76ee4c64c78d9bd1b609 -->
## api/getTeacherActivityData
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/getTeacherActivityData" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getTeacherActivityData"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/getTeacherActivityData`


<!-- END_3eb0e6e8581c76ee4c64c78d9bd1b609 -->

<!-- START_49359f29e21578e8157432ee327edf28 -->
## api/fileUpload
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/fileUpload" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/fileUpload"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "fileName": "",
    "url": "",
    "uploaded": "false",
    "error": {
        "message": "error msg"
    }
}
```

### HTTP Request
`GET api/fileUpload`

`POST api/fileUpload`

`PUT api/fileUpload`

`PATCH api/fileUpload`

`DELETE api/fileUpload`

`OPTIONS api/fileUpload`


<!-- END_49359f29e21578e8157432ee327edf28 -->

<!-- START_56788de495646542aebe1b35a50c6d88 -->
## api/updateTopics
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/updateTopics" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/updateTopics"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "status": "ok",
    "topics": 364,
    "topics2": 409
}
```

### HTTP Request
`GET api/updateTopics`


<!-- END_56788de495646542aebe1b35a50c6d88 -->

<!-- START_62f7bbca4036f16bc1d5e33cfb05abbc -->
## api/getAssignmentQuestions
> Example request:

```bash
curl -X POST \
    "http://localhost/api/getAssignmentQuestions" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getAssignmentQuestions"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/getAssignmentQuestions`


<!-- END_62f7bbca4036f16bc1d5e33cfb05abbc -->

<!-- START_a26973dca0ee94aefb46f613876e99bb -->
## api/testPhoneCleaner
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/testPhoneCleaner" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/testPhoneCleaner"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET api/testPhoneCleaner`


<!-- END_a26973dca0ee94aefb46f613876e99bb -->

<!-- START_d3ce742a03f1dc9cc050b8fb8abe46e1 -->
## api/stats
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/stats" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/stats"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "teachers_count": 1467,
    "users_count": 3637,
    "student_count": 2090,
    "schools_count": 824,
    "learning_plans": 197,
    "assignments": 1
}
```

### HTTP Request
`GET api/stats`


<!-- END_d3ce742a03f1dc9cc050b8fb8abe46e1 -->

<!-- START_3bacf783d6d7049453981fc8ad599971 -->
## api/school_stats
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/school_stats" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/school_stats"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET api/school_stats`


<!-- END_3bacf783d6d7049453981fc8ad599971 -->

<!-- START_07b6891508934c3d62b760fb2c80e20b -->
## api/test_sms
> Example request:

```bash
curl -X POST \
    "http://localhost/api/test_sms" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/test_sms"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/test_sms`


<!-- END_07b6891508934c3d62b760fb2c80e20b -->

<!-- START_0fd442551f0a98ab8822f13844747fea -->
## api/getUsersFromList
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/getUsersFromList" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/getUsersFromList"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
[
    {
        "id": 1,
        "user_id": 17,
        "sender_list_id": 1,
        "created_at": "2021-06-02 02:00:53",
        "updated_at": "2021-06-02 02:00:53"
    },
    {
        "id": 2,
        "user_id": 33,
        "sender_list_id": 1,
        "created_at": "2021-06-02 02:00:53",
        "updated_at": "2021-06-02 02:00:53"
    },
    {
        "id": 3,
        "user_id": 546,
        "sender_list_id": 1,
        "created_at": "2021-06-02 02:00:53",
        "updated_at": "2021-06-02 02:00:53"
    }
]
```

### HTTP Request
`GET api/getUsersFromList`


<!-- END_0fd442551f0a98ab8822f13844747fea -->

<!-- START_396f393f47d4fbbbc7ccf5c798ce2ac8 -->

## Show the application&#039;s login form.

> Example request:

```bash
curl -X GET \
    -G "http://localhost/login" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/login"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
null
```

### HTTP Request
`GET login`


<!-- END_66e08d3cc8222573018fed49e121e96d -->

<!-- START_ba35aa39474cb98cfb31829e70eb8b74 -->
## Handle a login request to the application.

> Example request:

```bash
curl -X POST \
    "http://localhost/login" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/login"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST login`


<!-- END_ba35aa39474cb98cfb31829e70eb8b74 -->

<!-- START_e65925f23b9bc6b93d9356895f29f80c -->
## Log the user out of the application.

> Example request:

```bash
curl -X POST \
    "http://localhost/logout" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/logout"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST logout`


<!-- END_e65925f23b9bc6b93d9356895f29f80c -->

<!-- START_ff38dfb1bd1bb7e1aa24b4e1792a9768 -->
## Show the application registration form.

> Example request:

```bash
curl -X GET \
    -G "http://localhost/register" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/register"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
null
```

### HTTP Request
`GET register`


<!-- END_ff38dfb1bd1bb7e1aa24b4e1792a9768 -->

<!-- START_d7aad7b5ac127700500280d511a3db01 -->
## Handle a registration request for the application.

> Example request:

```bash
curl -X POST \
    "http://localhost/register" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/register"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST register`


<!-- END_d7aad7b5ac127700500280d511a3db01 -->

<!-- START_d72797bae6d0b1f3a341ebb1f8900441 -->
## Display the form to request a password reset link.

> Example request:

```bash
curl -X GET \
    -G "http://localhost/password/reset" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/password/reset"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
null
```

### HTTP Request
`GET password/reset`


<!-- END_d72797bae6d0b1f3a341ebb1f8900441 -->

<!-- START_feb40f06a93c80d742181b6ffb6b734e -->
## Send a reset link to the given user.

> Example request:

```bash
curl -X POST \
    "http://localhost/password/email" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/password/email"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST password/email`


<!-- END_feb40f06a93c80d742181b6ffb6b734e -->

<!-- START_e1605a6e5ceee9d1aeb7729216635fd7 -->
## Display the password reset view for the given token.

If no token is present, display the link request form.

> Example request:

```bash
curl -X GET \
    -G "http://localhost/password/reset/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/password/reset/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
null
```

### HTTP Request
`GET password/reset/{token}`


<!-- END_e1605a6e5ceee9d1aeb7729216635fd7 -->

<!-- START_cafb407b7a846b31491f97719bb15aef -->
## Reset the given user&#039;s password.

> Example request:

```bash
curl -X POST \
    "http://localhost/password/reset" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/password/reset"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST password/reset`


<!-- END_cafb407b7a846b31491f97719bb15aef -->

<!-- START_cb859c8e84c35d7133b6a6c8eac253f8 -->
## Show the application dashboard.

> Example request:

```bash
curl -X GET \
    -G "http://localhost/home" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/home"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET home`


<!-- END_cb859c8e84c35d7133b6a6c8eac253f8 -->


