# KaxaNuk Official Coding Standards for Python Projects

## Code Conventions

### 1. All code must abide by [PEP 8](https://peps.python.org/pep-0008/)



<details>
<summary>Why?</summary>

As the official standard for all Python internal libraries, it has become the de-facto standard for most serious open-source Python libraries and projects.    

</details>


<!-- Project Structure -->

## Code Structure

*** Always import the specific function or class you are using from declarative codes to avoid variables naming collitions ***

*** All functions should be ordered alphabetically, with private (start with _) functions after public functions. The only exception is main(): ***

*** Folders that start with Upper Case could be edited by user, lowe case are the core structure of the package ***

## Steps to Create a Simple Code

Create the repository on GitHub and add a README.md

Clone the repository using GitHub Desktop

In the folder add the following basic strucure (depending on your proyect it could change, but this is how is expected to look):

* **\_\_main__.py** Entry script to set up the configurations and inject all dependencies. This is the only script that runs **imperative code**. All other scripts must include only declarative code (functions declarations, constants declarations, class declarations).

* **src/** Folder to save all the code that runs our project and it is not intended to interact with users

* **src/%PROJECT_NAME%.py** Main script should be named after the project. It requires a function called main(): that implements the main logic of the package and receives the injected dependencies from the entry script.

* **src/modules/** This folder should contain modules mainly declaring tools.

* **Config** This folder have the excel file parameters.xlsx to add a user friendly interface to parameterize the logic and create different scenarios, add .gitkeep file

* **Input** If you need to add files with securities trading and fundamental data or any other input for your project this is the place, add .gitkeep

* **Output** Whatever your project produce could be store here, add .gitkeep

 * **\_\.gitignore**

/Config/*
/Input/*
/Output/*

!/Config/.gitkeep
!/Input/.gitkeep
!/Output/.gitkeep

PROJECT_NAME
![image](https://github.com/KaxaNuk/Docs_KaxaNuk-Coding-Standards/assets/96888291/4728b737-3b5d-4508-a394-2c991f587b8d)

src
![image](https://github.com/KaxaNuk/Docs_KaxaNuk-Coding-Standards/assets/96888291/ee69d27f-a966-4c41-9639-d0e993920064)

## Steps to Create a Function for KaxaNuk's Library

pdm

* **src/entities/** This folder contains only modules declaring entity classes.

* **src/interfaces/** This folder contains only modules declaring interfaces.


