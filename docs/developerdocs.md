## Points to remember

- [ ] Provide details about how to setup and run the project
- [ ] Provide guides to any external dependencies / software that might be needed to run the project
- [ ] Provide details on how to deploy, if it is a deployable solution
- [ ] Provide some insight on the files, what they do, what are the various classes, objects, functions, global variables, which might come in handy while developing
- [ ] If the software features APIs, point towards how to access the documentation for testing the APIs. (You can create the API documentation using Swagger or any other such tool)

---

# Developer Docs

## Setup

- This project is built using PHP with `mysqli` to connect with MySQL. Make sure these are installed in the environment you are developing. Preferred environments are [MAMP](https://www.mamp.info/) and [XAMPP](https://www.apachefriends.org/index.html).
- Make sure the `env.php` file has the environment variables set, these will be crucial throughout the code for the sake of the environment it has been deployed.
- You can directly run the folder by adding it to the `htdocs` folder of the environment that you are using.

## Dependencies

- The project uses SCSS for the styles. You are free to use any pre-processor to compile the code to CSS, [scout-app](https://scout-app.io/) is a preferred software for the same.

## How to deploy

If you wish to deploy your customised software (provided you attach the license and credits), you can do so on any Apache server which supports PHP and MySQL. A number of free hosting services are available which you can use.

## Glossary
There are a number of classes, functions and variables which are essential for the software package.

- Classes
    - `User`: This object helps us to access and iterate the user that has logged in to the software
        - Methods
            - `login(username, password)`: Pass on the username and password of the user after initializing the object instance.
        - Attributes
            - `username` - stores the username of the user
            - `password` - stores the password of the user
- Functions
    - `isAuthenticated(user: User) -> Boolean`: This function checks if an instance of `User` is authenticated of note. Returns a `boolean`.
- Variables
    - `environment`: Checks the environment in which the software is running. Supported values are `local`, `test` and `production`.

## API reference

The project contains APIs which can be tested by going to the `swagger.php` on the running environment. The API documentation is powered by [swagger-php](https://github.com/zircote/swagger-php) by [@zircote](https://github.com/zircote/)

**Note**: The documentation is shown only when the `environment` variable is set to `local` or `test`.