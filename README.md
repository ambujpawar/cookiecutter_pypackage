Cookiecutter template for personal projects.

## Usage:
This is a cookiecutter template for creating a new python project. It creates a new project with the following structure:
```
├── .github
├── .gitignore
├── .pre-commit-config.yaml
├── docs
├── README.md
├── src
│   └── {{cookiecutter.project_name}}
│       ├── __init__.py
└── tests
    ├── __init__.py

```

### Requirements:
You first need to install cookiecutter. You can do so by running the following command:
```bash
pip install cookiecutter
```
Skip the above step if you already have cookiecutter installed.

### Create a new project:
You can create a new project using the following command:

```bash
cookiecutter gh:ambujpawar/cookiecutter_pypackage.git
```

This will prompt you to enter the following details:
```
project_name [project_name]:
project_slug [project_name]:
project_short_description [A short description of the project.]:
author_name [Your name]:
author_email [Your email address]:
```

### Create repo on github:
You can add the newly created project to github by running the following commands:
```bash
gh repo create {{cookiecutter.project_slug}}
```

### Push to github:
You can push the newly created project to github by running the following commands:
```bash
git init .
git add .
git commit -m "Initial skeleton."
git remote add origin git@github.com:{AUTHOR_NAME}/{YOUR_PROJECT}.git
git push -u origin master
```


### Activate virtual environment:
You can activate the virtual environment by running the following commands:
```bash
poetry env use python3.10
poetry shell
```
You can then add dependencies to the project by running the following command:
```bash
poetry add <package_name>
```


### Add pre-commit hooks:
You can add pre-commit hooks by running the following commands:
```bash
pre-commit install
```

