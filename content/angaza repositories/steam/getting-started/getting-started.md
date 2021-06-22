---
title: "Getting Started"

draft: false
---


# ANGAZA STEAM PLATFORM
## A module that leverages the Angaza Science, Tech, Arts and Mathematics content 

Angaza Steam is a cross-device compatible web platform site used to distribute course content on the Steam topics.


## Tech

Angaza Steam Module uses a number of open source projects to work properly:

- [Angular] - HTML enhanced for web apps!
- [npm] - Used as a package manager
- [Laravel] - PHP framework used for retrieval and serving of content
- [Composer] - PHP package manager

And of course Angaza Steam itself is open source with a [public repository][AngazaSteam]
 on GitHub.
 
## Installation

Angaza Steam requires [Node.js](https://nodejs.org/) v10+ to run.

Install the dependencies and devDependencies and start the server.

```sh
git clone https://github.com/Angaza-Elimu/steam-web
cd steam-web
npm i
ng serve
```

Verify the server started by navigating to your server address in
your preferred browser.

```sh
http://localhost:4200
```


For production environments...

```sh
ng build
cd dist
```

to access the production build

```sh
ng build
cd dist
```

this will take you to the directory in which the production files have been generated.


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


   [Composer]: <https://getcomposer.org>
   [Angular]: <https://angular.io>
   [Laravel]: <https://laravel.com/>
   [npm]: <https://https://www.npmjs.com/>
   [AngazaSteam]: <https://github.com/Angaza-Elimu/steam-web>

