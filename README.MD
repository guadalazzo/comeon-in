<h1 align="center">Welcome to Frontend Challenge for ComeOn - backend 👋</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-0.0.1-blue.svg?cacheSeconds=2592000" />
  <a href="https://github.com/guadalazzo/comeOn#readme" target="_blank">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" />
  </a>
  <a href="https://github.com/guadalazzo/comeOn/graphs/commit-activity" target="_blank">
    <img alt="Maintenance" src="https://img.shields.io/badge/Maintained%3F-yes-green.svg" />
  </a>
  <a href="https://github.com/guadalazzo/comeOn/blob/master/LICENSE" target="_blank">
    <img alt="License: ISC" src="https://img.shields.io/github/license/guadalazzo/Frontend Challenge for ComeOn - front" />
  </a>
  <a href="https://twitter.com/luppelazzo" target="_blank">
    <img alt="Twitter: luppelazzo" src="https://img.shields.io/twitter/follow/luppelazzo.svg?style=social" />
  </a>
</p>

A simple Registration and login flow created in react without any precreated setups connected to a node server, it use formik and Yup for validations, Jest for unit testing, Sass as a css preprocessor, and eslint as code formatter.


## Mock Server

We are using json-server to run a mock server. Nodemon for recharging on change, and jwt for creating the token.
What I've change?
Changed the response for security, I send a jwt token who have the user info, then the frontend will decoded and save it on context. 

Steps to run:

```
npm install

```

```
npm start

```
The server will start running in port 3003

### API

 #### Authenticate existing user and register for new users. (for screen 1) 
```
POST  /authenticate
``` 

Sample Payload 

```
{
    username: "harish.kulur",
    password: "secret"
}

```

Successful Response **200 OK**

```
{
    status:"SUCCESS",
    token: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6NCwidXNlcm5hbWUiOiJoYXJpc2giLCJwYXNzd29yZCI6InNlY3JldDAwIiwic2hvd0VtYWlsUGhvbmVTY3JlZW4iOnRydWUsInNob3dUZXJtc0FuZENvbmRpdGlvbiI6ZmFsc2UsInNob3dXZWxjb21lU2NyZWVuIjpmYWxzZSwiaWF0IjoxNTg0OTcyODI3LCJleHAiOjE1ODUwNTkyMjd9"
}

```

```
    token: {
      id: 0,
      username: "harish.kulur",
      showEmailPhoneScreen: true,
      showTermsAndCondition: false,
      showWelcomeScreen: false
      }
```

Failure Response **401 Unauthorized**

```
{
   status: "FAILURE",
   response: {
      errorKey: "INVALID_CREDENTIALS",
      errorDescription: "Invalid username and password"
   }
}

```

 #### For updating player details. (for screen 2,3,4) 

```
PUT /player
``` 

Sample Payload for screen 2 

```
{
   id: 0,
   username: "harish.kulur",
   password: "secret",
   email: 'john.doe@comeon.com',
   phone: "46-700111000",
   acceptMarketing: true
}

```

Sample Response for screen-2  (**200 OK**)

```
{
   status: "SUCCESS",
   token: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6NCwidXNlcm5hbWUiOiJoYXJpc2giLCJwYXNzd29yZCI6InNlY3JldDAwIiwic2hvd0VtYWlsUGhvbmVTY3JlZW4iOnRydWUsInNob3dUZXJtc0FuZENvbmRpdGlvbiI6ZmFsc2UsInNob3dXZWxjb21lU2NyZWVuIjpmYWxzZSwiaWF0IjoxNTg0OTcyODI3LCJleHAiOjE1ODUwNTkyMjd9"
}

```

```
token:{
   id: 0,
   username: "harish.kulur",
   showEmailPhoneScreen: false,
   email: 'john.doe@comeon.com',
   phone: "46-700111000",
   acceptMarketing: true,
   showTermsAndCondition: true,
   showWelcomeScreen: false
}
```
## Author

👤 **Guadalupe Jazmin Lazzo**

* Website: http://guadalazzo.github.io
* Twitter: [@luppelazzo](https://twitter.com/luppelazzo)
* Github: [@guadalazzo](https://github.com/guadalazzo)
* LinkedIn: [@https:\/\/www.linkedin.com\/in\/guadalupe-jazmin-lazzo\/](https://linkedin.com/in/https:\/\/www.linkedin.com\/in\/guadalupe-jazmin-lazzo\/)

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/guadalazzo/comeOn/issues). 

## Show your support

Give a ⭐️ if this project helped you!

## 📝 License

Copyright © 2020 [Guadalupe Jazmin Lazzo](https://github.com/guadalazzo).<br />
