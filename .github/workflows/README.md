# Olivaw template default workflows

In this folder will be found the actions that should be triggered during the different steps of the projects.

Check the [GitHub Actions docuumentation](https://docs.github.com/fr/actions).

Actions can be prevented to be triggered by adding `[skip actions]` in a commit message.

The following actions are set by default in this project:

* init-branch: On branch creation, an action will create new gist files that will store the badges data for this specific branch using the data from the parent branch, and the [project main README.md file](../../README.md) badges links will be replaced by the link of the badges related to the current branch.

* tests: On a push, all the different olivaw *model tests*, *data tests* and *query tests* will be run against the current project on that branch. The reports will be uploaded as [GitHub Artifacts](https://docs.github.com/fr/actions/using-workflows/storing-workflow-data-as-artifacts), the branch badges will be updated and the reports will be uploaded in the `.acimov/output/` folder if the pushed branch is `main`

For more information about these actions and how to modify their behavior, check the [olivaw branch initialization actions documentation](https://github.com/Wimmics/olivaw/tree/main/init-branch) and the [olivaw automatic tests actions documentation](https://github.com/Wimmics/olivaw/tree/main/test-actions).