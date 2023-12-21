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

* **\_\_main__.py** Entry script to set up the configurations and inject all dependencies. This is the only script that runs imperative code. All other scripts must include only declarative code (functions declarations, constants declarations, class declarations).

* **src/%MAIN_SCRIPT%.py** Main script should be named after the project. It requires a function called main(): that implements the main logic of the package and receives the injected dependencies from the entry script.

* **src/entities/** This folder contains only modules declaring entity classes.

* **src/interfaces/** This folder contains only modules declaring interfaces.

* **src/modules/** This folder should contain modules mainly declaring tools.

* 





