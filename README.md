# TaskManagerApp
Welcome to TaskManagerApp, a team project developed during my Bootcamp at the IT Academy.   
We gained hands-on experience working with a custom-made PHP framework to create an application that allows users to manage their tasks seamlessly.  
The application supports task creation, updates, deletions, and provides a clear list of tasks with their respective statuses and timestamps.   
#### Below are the key features and instructions for using the app:

## Features

- **Task Creation:** Add new tasks with the following details:

    - **Author:** The person who creates the task.
    - **Title:** A couple of words to describe the task.
    - **Description:** Detailed task information.
    - **Status:** Categorize tasks as "Pending", "In Progress", or "Completed".

- **Update Tasks:** Modify task details, including description and status.

- **Delete Tasks:** Easily remove unwanted tasks from the list.

- **List Tasks:** Access a comprehensive list of all tasks and detailed information for each.

- **Responsive Design:** The front-end, designed with the Tailwind CSS framework for HTML pages, ensures a user-friendly experience.

## Demostration
<video src="web\videos\webVideoDemostration.mp4" type="video/mp4" width="640" controls></video>

## How to Use

1. **Clone or Download:** Copy the repository to your local machine. It's better if you place it in yout local host folder.
2. **Turn the server on:** Ussualy is XAMMP for Windows/MacOS or LAMMP in Linux, then go to "Admin"
6. **Access the Application:** Your browser should be now open, so go to the `web` folder. If is not, open it yourself and go to `http://localhost/TaskManagerApp-ToDoList-PHP-MVC/web`.
7. **User Interface:** Navigate the App interface to create, update, delete, and list tasks.

## Technologies Used

- **PHP:** Based, following the **Model-View-Controller** (MVC) pattern.
- **Tailwind CSS:** Employed for style a responsive front-end design on **HTML** pages.
- **JSON database** is used for data persistence

## Acknowledgements

This project was completed during my time at IT Academy, providing valuable experience in collaborative development, the use of a custom framework, and effective task management.

#### Below you can see the readme that we were given initially.
# PHP initial Project
Main structure of php project. Folders / files:
- **app**
  - **controllers**
  - **models**
  - **views**
- **config**
- **lib**
  - **base**
- **web**

### Usage

The web/index.php is the heart of the system.
This means that your web applications root folder is the “web” folder.

All requests go through this file and it decides how the routing of the app
should be.
You can add additional hooks in this file to add certain routes.

### Project Structure

The root of the project holds a few directories:
**/app** This is the folder where your magic will happen. Use the views, controllers and models folder for your app code.
**/config** this folder holds a few configuration files. Currently only the connection to the database.
**/lib** This is where you should put external libraries and other external files.
**/lib/base** The library files. Don’t change these :)
**/web** This folder holds files that are to be “downloaded” from your app. Stylesheets, javascripts and images used. (and more of course)

The system uses a basic MVC structure, with your web app’s files located in the
“app” folder.

#### app/controllers
Your application’s controllers should be defined here.

All controller names should end with “Controller”. E.g. TestController.
All controllers should inherit the library’s “Controller” class.
However, you should generally just make an ApplicationController, which extends
the Controller. Then you can defined beforeFilters etc in that, which will get run
at every request.

#### app/models
Models handles database interaction etc.

All models should inherit from the Model class, which provides basic functionality.
The Model class handles basic functionality such as:

Setting up a database connection (using PDO)
fetchOne(ID)
save(array) → both update/create
delete(ID)
app/views
Your view files.
The structure is made so that having a controller named TestController, it looks
in the app/views/test/ folder for it’s view files.

All view files end with .phtml
Having an action in the TestController called index, the view file
app/views/test/index.phtml will be rendered as default.

#### config/routes.php
Your routes around the system needs to be defined here.
A route consists of the URL you want to call + the controller#action you want it
to hit.

An example is:
$routes = array(
‘/test’ => ‘test#index’ // this will hit the TestController’s indexAction method.
);

#### Error handling
A general error handling has been added.

If a route doesn’t exist, then the error controller is hit.
If some other exception was thrown, the error controller is hit.
As default, the error controller just shows the exception occured, so remember
to style the error controller’s view file (app/views/error/error.phtml)


### Utilities
- [PHP Developers Guide](https://www.php.net/manual/en/index.php).
- .gitignore file configuration. [See Official Docs](https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files).
- Git branches. [See Official Docs](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell).
