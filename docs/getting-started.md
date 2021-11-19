## Getting Started

Please use the following outline to get started with a new Data Science Project. If you run into any problems or need additional support, please join our [slack](https://operatefirst.slack.com/ssb/redirect) and post a message in the `#support` channel, or open an issue [here](https://github.com/operate-first/support/issues).  

### **Define a Project Document**

1. Review our project workflow document [here][1].

2. Create a new project description using our [template][2]. For reference, you can review an example project document [here][3].

3. Put your project document into a subfolder of this [shared directory][4]. 

### **Create Git Repository from a Template**

Next, create a [CookieCutter][5] formatted data science project repository from this [template][6]. To do so, please follow these [instructions][7] for creating a new repository from a template.

### **Set Up AICoE Continuous Integration (CI)**

[AICoE-CI](https://github.com/aicoe/aicoe-ci#getting-started) can aid various aspects of a development workflow such as running pre-commit checks, build checks, triggering pipelines to build images, etc.

For more information on AICoE CI and how to set it up for your project, you can follow the documentation [here](https://github.com/aicoe/aicoe-ci#getting-started).

### **Create Project Boards and Issues**

You can create Issues to highlight new features, bugs and break upcoming goals of a project into smaller chunks. You can create GitHub [Issues](https://docs.github.com/en/issues/tracking-your-work-with-issues) and include [Task Lists](https://docs.github.com/en/issues/tracking-your-work-with-issues/about-task-lists) for each task that you plan to work on.

Here is an [example Issue](https://github.com/aicoe-aiops/ocp-ci-analysis/issues/279) that we created to highlight a certain task for our project.

We use [project boards](https://docs.github.com/en/issues/organizing-your-work-with-project-boards/managing-project-boards/about-project-boards) to organize the tasks within the team.

Once your project board is created, begin to create issues and populate the board with them
* Create an issue for every task you plan to work on
    * Break issues down into smaller pieces if they cannot be completed in a single sprint
    * Be specific in the description of the issue 
    * Tag other related issues with a ‘#’ as necessary
    * Provide acceptance criteria for when the issue can be closed 
    * Assign yourself or your teammates who you plan to work with on the task to the issue

* Add the issues to the *New* column of you project board
* When you're almost ready to begin working on an issue, move it to the *To Do* column
* Once you start work on an issue, move it to the *In Progress* column

For more information of the remainder of our GitHub workflow, please visit [this page][10]. 

### **Develop on Operate First Jupyterhub**

The following resources are available for use to develop your project on the Operate First JupyterHub instance:

* **Start developing on the Operate First JupyterHub environment**
    - View the [video tutorial](https://www.youtube.com/watch?v=iI_-lqi3vP4&list=PL8VBRDTElCWpneB4dBu4u1kHElZVWfAwW&index=3)
    - Access the public [JupyterHub instance][11] on the Massachusetts Open Cloud (MOC) by selecting *operate-first* authentication and then signing in with your GitHub account

* **How to Monitor JupyterHub workloads using Grafana dashboards** 
    -  (Video tutorial forthcoming)
    -  To troubleshoot issues while running your notebooks, you can refer to the [Troubleshooting Runbooks][12]
    -  You can refer the existing [Grafana dashboard][13] for monitoring your Jupyterhub workloads such as CPU, RAM usage, percentage PVC usage.

### **Managing Dependencies**

Guidance for managing notebook dependencies can be found in this [video](https://www.youtube.com/watch?v=ifyQ2oSxjnU&list=PL8VBRDTElCWpneB4dBu4u1kHElZVWfAwW&index=4). The repository for our dependency management tool can be found [here](https://github.com/thoth-station/jupyterlab-requirements). 

### **Deliverables**

Here are potential ways to contribute and showcase work you have completed.
* Slide decks
* Blog posts ([example](https://www.operate-first.cloud/data-science/configuration-files-analysis/docs/blog/configuration-file-analysis-blog.md))
* Videos ([example](https://www.youtube.com/watch?v=BKnF174eZN0&list=PL8VBRDTElCWoGwMhCp04rQFMcIhshv33U&index=9))
* Tutorials ([example](https://www.operate-first.cloud/data-science/ai4ci/docs/automating-using-elyra.md))
* Content images
* Project Repositories ([example](https://github.com/aicoe-aiops/ocp-ci-analysis))
* Dashboards
* Model Services

### **Creating Jupyterhub Images**
JH images can be made from your projects to easily share reproducible ML experiments and create interactive Data Science working environments. Please refer to the following [guide](https://www.operate-first.cloud/users/data-science-workflows/docs/create_and_deploy_jh_image.md) for more information.

### **Creating Automated Model Workflows**

To automate your notebook workflows using Elyra and Kubeflow Pipelines on Open Data Hub, you can refer to the [guide](https://github.com/AICoE/elyra-aidevsecops-tutorial) and view our video [tutorial](https://www.youtube.com/watch?v=iMSOal8wRj4).

[1]: https://docs.google.com/document/d/1LqVXQbd81IdPfoXw2B0iCcnb-ygCVvdy_8vejY08zZ4/edit
[2]: https://docs.google.com/document/d/1CIFlKiVbNX3CKC-tD7kVDkP1S8eDfDEibdLM6jgIj2g/edit
[3]: https://docs.google.com/document/d/1prfyxHAQq60IU_K_f-eTNVCB6FKV2q00YAbmY-jI_HE/edit
[4]: https://drive.google.com/drive/folders/17nhASQZUbGISFQswUb-ft3V1dxbD7dtX
[5]: https://drivendata.github.io/cookiecutter-data-science/#cookiecutter-data-science
[6]: https://github.com/aicoe-aiops/project-template
[7]: https://help.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template
[8]: https://github.com/orgs/aicoe-aiops/projects/2
[10]: how-to-contribute.md
[11]: https://jupyterhub-opf-jupyterhub.apps.smaug.na.operate-first.cloud/
[12]: https://www.operate-first.cloud/hitchhikers-guide/apps/docs/odh/jupyterhub/runbook.md
[13]: https://grafana.operate-first.cloud/
