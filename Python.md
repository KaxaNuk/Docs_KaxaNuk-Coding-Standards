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

## Steps to Create an Strategy Code Strucutre

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

**/__pycache__/*

!/Config/.gitkeep

!/Input/.gitkeep

!/Output/.gitkeep

PROJECT_NAME

![image](https://github.com/KaxaNuk/Docs_KaxaNuk-Coding-Standards/assets/96888291/4728b737-3b5d-4508-a394-2c991f587b8d)

src

![image](https://github.com/KaxaNuk/Docs_KaxaNuk-Coding-Standards/assets/96888291/ee69d27f-a966-4c41-9639-d0e993920064)

In GitHub Desktop create a new branch called dev and commit this changes:

![image](https://github.com/KaxaNuk/Docs_KaxaNuk-Coding-Standards/assets/96888291/15a19f0a-28fb-4716-940a-5aece9754cf3)


![image](https://github.com/KaxaNuk/Docs_KaxaNuk-Coding-Standards/assets/96888291/df755cf8-f596-4898-ae68-f8c4a269c7a0)

## Configuración del Entorno y Dependencias

Para configurar tu entorno y asegurarte de que todas las dependencias necesarias están instaladas, sigue estos pasos:

1. **Descargar Anaconda**: Descarga la versión más reciente de Anaconda desde su [sitio web oficial](https://www.anaconda.com/products/distribution). Asegúrate de elegir la versión que corresponda a tu sistema operativo.

2. **Abrir Anaconda Prompt**: Una vez instalado Anaconda, inicia Anaconda Prompt desde tu menú de inicio.

3. **Crear un Nuevo Environment con Python 3.11**: En Anaconda Prompt, crea un nuevo environment llamado `alexa` con Python 3.11 utilizando el siguiente comando:
   ```bash
   conda create --name alexa python=3.11

4. **Activar el Environment**: Activa el environment recién creado con el comando:
   ```bash
   conda activate alexa
   
5. **Cambiar al Directorio del Repositorio**: Navega al directorio donde está clonado el repositorio utilizando el comando cd. Por ejemplo:    
    ```bash
    cd C:\Users\TuUsuario\Documents\C_AGBC-Alexa
    
6. **Instalar PDM**: Dentro del environment activado, instala PDM utilizando pip con el siguiente comando:
    ```bash
    pip install pdm

change directory 
cd /d D:\Open Projects\O_Clustering-Rotation

![image](https://github.com/KaxaNuk/Docs_KaxaNuk-Coding-Standards/assets/96888291/03489327-f168-47a6-b227-bb3f0f39eb50)


6.a pdm init

![image](https://github.com/KaxaNuk/Docs_KaxaNuk-Coding-Standards/assets/96888291/978fe7f0-f3f9-42cb-850a-d177e4cdef66)

pdm install

7. **Instalar Dependencias con PDM**: Ejecuta pdm install para instalar todas las dependencias del proyecto definidas en el archivo pyproject.toml. Usa el siguiente comando:
    ```bash
    pdm install

conda list

if you want to add a new lbrar then

pdm update

aafter adding to toml the library needed

8. **Abrir Anaconda Navigator**: Finalmente, selecciona el environment alexa, este lo podemos encontrar en la parte izquierda en la seccion de Environments, una vez hecho eso, regresamos a Home e instalamos Spyder, una vez instalado, lo abrimos y cambiamos el directorio de trabajo como lo hemos hecho anteriormente para posteriormente abrir app.py y correrlo.

Siguiendo estos pasos, tendrás configurado el entorno necesario para trabajar en el proyecto C_AGBC-Alexa Dashboard de manera eficiente y ordenada.




## Steps to Create a Function for KaxaNuk's Library

pdm

* **src/entities/** This folder contains only modules declaring entity classes.

* **src/interfaces/** This folder contains only modules declaring interfaces.


