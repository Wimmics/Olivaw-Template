# Olivaw-Template

A template repository for projects using Olivaw to support ontology engineering using Acimov methodology.

## How to use

### Install the available tools

This project is using different GitHub Actions that automatize some developper work about test and branch initialization. These Actions require to have access to a Gist that will be needed to store information about badges that will appear at the top of the main `README.md` page.

Check the [olivaw getting started documentation](https://github.com/Wimmics/olivaw/tree/main?tab=readme-ov-file#getting-a-personnal-access-token-with-gist-scope) to know how to generate a GitHub access token with the `gist` scope and set it as a repository secret variable.

There are two olivaw usages that need local installation.

Both of them are using the [olivaw python package](https://pypi.org/project/olivaw/), which is relying on [Corese RDF](https://project.inria.fr/corese/), a Java RDF database system that supports OWL EL/QL/RL reasoning, ShaCL validation and OWL Profile diagnose.

Therefore any of these usages will require [python version 3.10 or greater](https://www.python.org/downloads/) and a [Java version 11 or greater](https://www.oracle.com/fr/java/technologies/downloads/)

[olivaw python package](https://pypi.org/project/olivaw/) can be used as a command tool to generate locally test reports over the ontology fragments, data fragments and competency questions of an acimov project. It also provides tools to facilitate the development process with features like repository or branch badges initializing. Given the previous prerequisites, it can be installed using [pypi](https://pypi.org/) command:

```shell
pip install olivaw
```

Installing from GitHub URL is also possible:

```shell
pip install git+https://github.com/Wimmics/olivaw
```

Then, using the access token generated above, generate the `.acimov/parameters.json` file using this command:

```shell
olivaw init repo
```

[olivaw pre-commit hook](https://github.com/Wimmics/olivaw/blob/main/docs/pre-commit.md) is a program relying on [pre-commit](https://pre-commit.com/) that tests locally the different files staged for commit before pushing to the repository origin. It works with git CLI and [GitHub Desktop](https://desktop.github.com/).
Pre-commit can be installed with the following command:

```shell
pip install pre-commit
```

In this template the [pre-commit hook configuration file](../.pre-commit-config.yaml) is already set, so the last step is to enable the hook using the following command:

```shell
pre-commit install
```

The first hook trigger will last longer since it needs to clone the repository and install the hook in a virtual environment.

Check the [olivaw functional documentation](https://github.com/Wimmics/olivaw/tree/main/docs) for more details about olivaw CLI and olivaw pre-commit hook.

### Fill the template files

Different files were made templates so that it can be adapted to any ontology project:

* [ONTOLOGY primer](../primer/README.md): A primer template that will provide all the key concepts explanations to use the ontology 
* [MODELING-ONTOLOGIES](../MODELING-ONTOLOGIES.md): A document meant to provides general guidelines about how to use the ontology
* [ONTOLOGY alignment](../primer/other-ontology-alignment.md): A template document that will provide all the required information to align a dataset expressed with a similar ontology with the current project ontology

Finally, the main README.md file that is intended is the [README template](../README.md) that can be found in this folder.

## Features

### Development features

* test generation against ontology fragments, data fragments and competency questions. Check the [olivaw test documentation](https://github.com/Wimmics/olivaw/blob/main/docs/tests.md) for more details about what is tested, [olivaw custom test documentation](https://github.com/Wimmics/olivaw/blob/main/docs/custom-tests.md) to see how to add more cutomized tests, [olivaw parameters documentation](https://github.com/Wimmics/olivaw/blob/main/docs/parameters.md) to see how to customize the olivaw project parameters, and [olivaw command line documentation](https://github.com/Wimmics/olivaw/blob/main/docs/commands.md) to see how to trigger these tests using CLI.
* pre-commit hook that will prevent blocking errors to be committed on client side to be pushed to origin repository. Check the [pre-commit documentation](https://pre-commit.com/) and [olivaw pre-commit hook documentation](https://github.com/Wimmics/olivaw/blob/main/docs/pre-commit.md) for more details.
* GitHub Actions that will manage the branches initializaton and provide health checks of the different branches at any time. Check the [GitHub Actions documentation](https://github.com/Wimmics/olivaw/blob/main/docs/actions.md)

## Project structure

Many files are already there and may be kept, updated, adapted or removed at will, such as:

* [README template](../README.md) that will provide the main element to redact a proper README.md file for the project
* [CODE OF CONDUCT](../CODE-OF-CONDUCT.md) that will provide the code of conduct to follow during any interaction during the ontology development
* [CONTRIBUTING file](../CONTRIBUTING.md) that provides the main guidelines to contribute for the ontology
* [license file](../LICENSE) that provides the copyrights that should apply to the project. The default version is [LGPL-2.1](https://www.gnu.org/licenses/old-licenses/lgpl-2.1.en.html)
* [ONTOLOGY primer](../primer/README.md): A primer template that will provide all the key concepts explanations to use the ontology 
* [MODELING-ONTOLOGIES](../MODELING-ONTOLOGIES.md): A document meant to provides general guidelines about how to use the ontology
* [ONTOLOGY alignment](../primer/other-ontology-alignment.md): A template document that will provide all the required information to align a dataset expressed with a similar ontology with the current project ontology
* [.gitignore](../.gitignore/): A file that exclude different files and folders to be commited so that no useless and polluting files are pushed to the repository

Different folders are also present as part of the acimov architecture, namely:
* [domains folder](../domains/) that will contain the different application domains and motivating scenarios, check the [domains documentation](../domains/)
* [src folder](../src/) that will contain the different modules that are expected to be published
* [use-cases folder](../use-cases/) that will contain all the scenarios that can show the actual abilities of the ontology
* [resources folder](../resources) that is expected to contain the different resources that may be useful for the main README file
* [primer folder](../primer/) that will contain the ontology primer and the different alignement documents
* [.acimov folder](../.acimov/) that will contain the different files and folders related to acimov process and olivaw
* [.github folder](../github/) that will contain the different files and folders related to github, including the workflow files

## Parameters

In order to customize this configuration, check the [olivaw actions documentation](https://github.com/Wimmics/olivaw/blob/main/docs/actions.md), the [olivaw custom test documentation](https://github.com/Wimmics/olivaw/blob/main/docs/custom-tests.md) and the [olivaw parameters.json documentation](https://github.com/Wimmics/olivaw/blob/main/docs/parameters.md).

### Contributing

Feel free to open an [issue](https://github.com/Wimmics/Olivaw-Template/issues) or submit a [pull request](https://github.com/Wimmics/Olivaw-Template/pulls).
