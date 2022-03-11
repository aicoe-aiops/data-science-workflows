# Data Science Workflow

This repo contains a set of resources, tutorials and general best practices that our team has developed and continues to refine for effectively collaborating as a group of data scientists. Our team relies heavily on the [Open Data Hub](https://opendatahub.io/) (ODH) project (which we also recommend), so many of our examples will use that toolbox. But our hope is that there is enough generally applicable content that this information can be helpful to those outside the ODH ecosystem. Further, we invite others to [contribute](https://github.com/aicoe-aiops/data-science-workflows/issues/new) their best practices and implementation alternatives : )

## Setup Your Environment

* [What is the Open Data Hub and Operate First?](docs/setup_environment/odh_and_opf.md) 
* [Access JupyterHub](docs/setup_environment/JH_access.md)
* [Manage data with remote storage](docs/setup_environment/remote-storage.md)
* [Setup CI](docs/setup_environment/thoth.md)

## Develop + Collaborate 
* [Use Thoth tooling to enhance development](docs/develop_collaborate/thoth-tools.md)
* [Best practice for contributing as a Data Scientist](docs/develop_collaborate/how-to-contribute.md)
* [Build ML pipelines from notebooks](docs/develop_collaborate/automated-pipelines.md)
* [Track your metrics and experiments](docs/develop_collaborate/track-metrics-using-kubeflow.md)
* [Share reproducible notebook images](docs/develop_collaborate/create_and_deploy_jh_image.md)
* [Quickly deploy interactive environments and JupyterBooks](docs/develop_collaborate/meteorize.md)
* [Create interactive dashboards to visualize results](docs/visualization/trino_and_superset.md)
* [Getting Started with Data Science](docs/develop_collaborate/getting-started-with-data-science.md)

## Serving + Monitoring
* [Monitor JupyterHub environment workloads](docs/serving_monitoring/monitor-jh.md)
* [Serve your model with Seldon](docs/serving_monitoring/deploy-models-using-seldon.md)
* [Create custom serving images with Seldon](docs/serving_monitoring/deploy-custom-model.md)

## Project Organization + Structure
* [Tips for starting a new ML project from scratch](docs/project_structure/getting-started.md)
* [Recommendations for structuring an E2E ML project](docs/project_structure/project-structure.md)
* [Template for writing a project document](docs/project_structure/project-document-template.md)
* [Simplify Project Management with GitHub project boards and issue](docs/project_structure/boards-and-issues.md)

## E2E Example Projects
* [AI4CI](https://github.com/aicoe-aiops/ocp-ci-analysis)
* [OS-Climate](https://github.com/os-climate/aicoe-osc-demo)


## Contact

This project is maintained as part of the [Operate First](https://www.operate-first.cloud/) and Emerging Technologies group in Red Hat’s Office of the CTO. More information can be found at https://www.operate-first.cloud/.

Have a question? Open an issue in [this repo](https://github.com/aicoe-aiops/data-science-workflows/issues/new) or join us on [Slack](https://join.slack.com/t/operatefirst/shared_invite/zt-o2gn4wn8-O39g7sthTAuPCvaCNRnLww) in the #data-science channel. :) 
