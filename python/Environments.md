# Environment Setup and Configuration

## Target Environments

All of our code must be runnable in the following environments without need for any code changes:
* Docker containers
* Conda
* Venv

This requires the following characteristics for each code project.


## Universal Project Requirements

1. All dependencies must be declared in the project's `pyproject.toml` file, so they can be managed by tools like `pdm`.
2. All configuration variables/constants must be populated either directly from environment variables (preferrable), or from files external to the repository provided through the entry script.
3. Because of the above point, **All hard coded configurations are expressly forbidden, including in any proof-of-concept scripts.** <details><summary>Why?</summary> This is a dangerous practice, as any secret credential commited by mistake to a git repository effectively leaks it to anyone with read access to the repository, no matter if the secret is removed from the file in later commits.</details>
4. All absolute paths are prohibited in any code. If you absolutely must import some file by path, use relative paths from your entry script.


## Development Requirements

1. Use a separate Python environment for each project you're working on.


## Environment Variables Setup

### Docker

Just setup all environment variables when first running the project's image, depending on the tool you're using to run it.
* **Terminal**: Use the `-e` flag for each env var KEY=VALUE: `docker run -e MYVAR1='value1' -e MYVAR2='value2' ...`
* **Docker Desktop**: Add all env vars on the configuration window of the first run of the image.
* **PyCharm**: Right click on the project's `Dockerfile`, select `Modify Run Configuration`, and on the `Run` section click on `Modify` and select `Environment Variables`. Now setup all the env vars in the Environment Variables configuration window.


### Conda

Open the terminal, and after activating your environment:

1. Set each environment variable one by one with `conda env config vars set MYVAR1=value1`, `conda env config vars set MYVAR2=value2`, and so on.
2. After having set all your env vars, reactivate your environment to be able to use them.
3. Now you can check they were correctly set by running `conda env config vars list`.

More info: [https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#setting-environment-variables](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#setting-environment-variables)


### Venv

You need to edit your venv's `postactivate` script as follows:

1. Activate your virtual environment.
2. Find your venv folder.
3. Inside that folder, find the `bin/activate` file, and edit it. Add your env var definitions at the end, one per line, in the following format: `export MYVAR1="value1"`
4. Reactivate the virtual environment.


## Loading the Environment Variables from Python

Once your env vars have been setup for your environment, you can load them using the `os.getenv` standard library function:
```python
import os
myvar1 = os.getenv("MYVAR1")
# just to show it worked, but avoid using print() in your code:
print(myvar1)
```
