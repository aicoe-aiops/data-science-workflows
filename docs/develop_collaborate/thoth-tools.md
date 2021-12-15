# AICoE-CI and Thoth tools for data science

[Project Thoth](https://thoth-station.ninja/) is a collection of open source tools which use artificial intelligence (AI) to recommend software stacks for Python applications. It tightly integrates with [AICoE-CI](https://github.com/AICoE/aicoe-ci) which is a continuous integration and delivery system based on Tekton-Pipeline / OpenShift-Pipeline. 

AICoE-CI can aid various aspects of a data science development workflow such as running pre-commit checks, build checks, triggering pipelines to build images, etc. The tools offered by AICoE-CI and Thoth make data science developement processes easier by offering:

* [Status Checks](https://github.com/aicoe/aicoe-ci#configuring-checks-and-tests) on Pull Requests for testing and containerization such as pre-commit checks, build checks etc.
* [Thoth Advisor](https://github.com/thoth-station/adviser) for recommending software stacks for a python project.
* [GitHub ChatOps Options](https://github.com/AICoE/aicoe-ci#github-chatops-options) such as support of Github comment commands for Pull Request processing on GitHub.
* [Container image builds](https://github.com/aicoe/aicoe-ci#configuring-build-requirements) on Tag releases and from Pull requests.


