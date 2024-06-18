# Olivaw-Template

A template repository for projects using Olivaw to support ontology engineering using Acimov methodology.

This repository is affiliated to the [Wimmics reasearch team](https://www.inria.fr/fr/wimmics), check the other [Wimmics projects](https://github.com/Wimmics).

## How to use

This repository is made to help any developer to start an ACIMOV ontology development process, so check the [scientific article about the ACIMOV methodology](https://www.emse.fr/~zimmermann/Papers/mk2023.pdf).

This repository also relies on olivaw framework, so check the [olivaw repository and its documentation](https://github.com/Wimmics/olivaw).

### Quick start

* Instanciate a repository using the "Use this template"
* Add a repository secret variable named `GIST_SECRET` containing an access token with the `gist` scope (see [how to add make the token and add the secret](#add-gist-scope-access-token-to-secret-repository-variable))
* Clone the repository locally with `git clone ...`
* Install `olivaw` package
* Inside the repository folder, type `olivaw init repo` and follow the instructions
* Install `pre-commit package` using the command `pip install pre-commit`
* Inside the repository folder, type `pre-commit install`

Check the [olivaw functional documentation](https://github.com/Wimmics/olivaw/tree/main/docs) for more details about olivaw CLI and olivaw pre-commit hook.

### Add gist scope access token to secret repository variable

* First go to the [Github access token generation webpage](https://github.com/settings/tokens).
* Then create a personnal access token with only the `gist` scope. Copy/paste this token somewhere because it will never be shown again.
* Then go to `{repository_url}/settings/secrets/actions`, create a new repository secret named `GIST_SECRET` and paste the key

### Install olivaw

Olivaw requires [python version 3.10 or greater](https://www.python.org/downloads/) and a [Java version 11 or greater](https://www.oracle.com/fr/java/technologies/downloads/)

It can be installed using [pypi](https://pypi.org/):

```shell
pip install olivaw
```

Installing from GitHub URL is also possible:

```shell
pip install git+https://github.com/Wimmics/olivaw
```

### Fill the template files

Different files were made templates so that it can be adapted to any ontology project:

* [ONTOLOGY primer](../primer/README.md): A primer template that will provide all the key concepts explanations to use the ontology 
* [MODELING-ONTOLOGIES](../MODELING-ONTOLOGIES.md): A document meant to provides general guidelines about how to use the ontology
* [ONTOLOGY alignment](../primer/other-ontology-alignment.md): A template document that will provide all the required information to align a dataset expressed with a similar ontology with the current project ontology

Finally, the main README.md file that is intended is the [README template](../README.md) that can be found in this folder.

## Features

### Development features

* test run locally against ontology fragments, data fragments and competency questions. Check the [olivaw command line documentation](https://github.com/Wimmics/olivaw/blob/main/docs/commands.md) for how to run tests, [olivaw test documentation](https://github.com/Wimmics/olivaw/blob/main/docs/tests.md) for details about what is tested and what the default tests cover, [olivaw custom test documentation](https://github.com/Wimmics/olivaw/blob/main/docs/custom-tests.md) to see how to add cutomized tests and [olivaw parameters documentation](https://github.com/Wimmics/olivaw/blob/main/docs/parameters.md) to see how to customize the olivaw project parameters.
* pre-commit hook that will prevent blocking errors to be committed on client side to be pushed to origin repository. Check the [pre-commit documentation](https://pre-commit.com/) and [olivaw pre-commit hook documentation](https://github.com/Wimmics/olivaw/blob/main/docs/pre-commit.md) for more details.
* GitHub Actions that will manage the branches initializaton and provide health checks of the different branches at any time. Check the [GitHub Actions documentation](https://github.com/Wimmics/olivaw/blob/main/docs/actions.md)

## Project structure

Many files are already there and may be kept, updated, adapted or removed at will, such as:

* [README template](../README.md) that will provide the main element to redact a proper README.md file for the project
* [AUTHORS template](../AUTHORS.md) that should provide the information to developpers and some useful information about the project
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

A CITATION.cff at the root of the repository may be also a good idea for any people to cite the ontology properly. Several [CITATION.cff files generators](https://citation-file-format.github.io/cff-initializer-javascript/#/) exist to make one quite easily.

## Parameters

In order to customize this configuration, check the [olivaw actions documentation](https://github.com/Wimmics/olivaw/blob/main/docs/actions.md), the [olivaw custom test documentation](https://github.com/Wimmics/olivaw/blob/main/docs/custom-tests.md) and the [olivaw parameters.json documentation](https://github.com/Wimmics/olivaw/blob/main/docs/parameters.md).

### Contributing

Feel free to open an [issue](https://github.com/Wimmics/Olivaw-Template/issues) or submit a [pull request](https://github.com/Wimmics/Olivaw-Template/pulls).
