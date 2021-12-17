# How to Structure a Data Science Project: The Operate First Way! 

The purpose of this document is to provide teams of data scientists in the Operate First Community with some guidelines on how to best structure their projects in a way that encourages consistent workflows across projects, promotes collaboration and an "Operate First” mentality. 

# How do I manage my project?

Organizational overhead can be an easily overlooked, and a potentially crippling oversight for a new open source project. To make things worse, data science is still a relatively new discipline and the right tools and methodologies for project management are still being figured out.

Our approach to overcoming this issue is simply to focus on the fewest number of tools possible. That really comes down to using GitHub, for just about everything, and Slack if we want to have a real time conversations. What do you need to start your project and keep it moving? 

* GitHub
	* Public repository ([examples](https://github.com/aicoe-aiops))
	* Project board ([examples](https://github.com/orgs/aicoe-aiops/projects) )
	* Issues templates ([examples](https://github.com/aicoe-aiops/project-template/tree/master/.github/ISSUE_TEMPLATE))
	* [Helpful bots](https://github.com/apps/khebhut) 

*You can also jump start your repo with our [project template](https://github.com/aicoe-aiops/project-template).*
	 
* Slack
	* Project channel(s) ([example](https://join.slack.com/t/operatefirst/shared_invite/zt-o2gn4wn8-O39g7sthTAuPCvaCNRnLww))
</br></br>

# What are the phases of a data science project?

### 1. Project Definition and Use Case Understanding:

To start, contributors should create a public repo and include a README with an initial outline of the project, a description of any available data or similar projects and the desired outcomes and end-users of this intelligent application. If you need help coming up with a project outline, feel free to start with [this template](/project-document-template.md) for inspiration. 

The project outline can include: 

1. A concrete checklist of items that define when the project is complete (subject to ongoing review)

2. Defined performance criteria and success metrics that will be used to evaluate the success of the machine learning models.   

3. An alternative solution written in terms as though it would be solved manually by a human without AI, i.e, "I use my eyes to look at a picture and respond that it is or is not a cat based on my knowledge of the appearance of cats". This helps to identify any potential mismatch between desired outcome and available data. 

4. Outline a path to operationalization. Make sure there is some consideration given to the infrastructure, deployment, and user interactions of your projects final form.  
 
Once this is done, you can move on to step 2, OR share your new project proposal with the Operate Fist DS Community on [Slack](https://join.slack.com/t/operatefirst/shared_invite/zt-o2gn4wn8-O39g7sthTAuPCvaCNRnLww) (#data-science) to get some feedback and potential contributors.   

### 2. Research and Problem Understanding:

Now that you have a problem you'd like to solve, its time to do some research!!! This phase of a project is quite flexible and is bound to be traversed differently by every individual. However, before jumping into any hard-core development we generally like to make sure to do the following at the bare minimum:

1. Compile and read 3-4 relevant papers on the problem domain. [Papers With Code](https://paperswithcode.com/) and [arxiv](https://arxiv.org/) will be your friends here. 

2. Find 1-2 comparable open source projects and try to deploy them yourself. Maybe the solution you're looking for already exists and you can re-use or contribute to an existing project instead of starting from scratch. 

3. Add a `research.md` doc to your repo outlining the papers and projects explored above. This may be useful to you for reference or documentation later on. Plus, anyone who needs to do the same research in the future will thank you. 

### 3. Data Preparation and EDA: 

Time to dig into the data. Before getting right into the Machine Learning development, we think its best practice to take some focused time to familiarize yourself with the data and to write all the data preparation, processing and management functions you'll need to make life easier in the future. 


1. Make sure your data is publicly available and accessible. We recommend using a Ceph bucket on the OPF cluster (request one [here](https://github.com/operate-first/support/issues/new?assignees=first-operator&labels=kind%2Fonboarding%2Carea%2Fbucket&template=ceph_bucket_request.yaml&title=BUCKET%3A+%3Cname%3E)) 

2. Develop an EDA Notebook to help explain to others (and your future self) what the data looks like and what it represents.

3. Write all necessary ETL, data cleaning and preprocessing code. 

4. Select and separate immutable training, testing and evaluation datasets. Store each separately in your Ceph bucket.   

5. Make any required updates to the project Readme/Plan if needed due to discoveries in the data set.  


### 4. Implement proof of concept AI/ML model:

Here is were we start to do some ML exploration and put together our bare-bones mvp application. 

1. Create a jupyter notebook and start experimenting with different models and approaches until your results meet the performance criteria defined earlier. At this stage there are a number of options for experiment tracking, but we recommend using [kubeflow pipelines](demovideo).   

2. Clean up your experimental notebook so that another data scientists would be able to follow the logic, re-run it and understand your results. This means, clearly written markdown cells, well labeled plots and commented code.     

3. Once your Proof of Concept notebook(s) are done. Push them to your github repo and share them using [project meteor](https://shower.meteor.zone/)   

### 5. Deployed PoC as a service:

Your work is ready to leave the safety of a jupyter notebook and become a deployed service that will become the center of a new intelligent application. Get Excited! 

1. Deploy your model. There are a number of tools out their to make this easy, but we recommend using Seldon. Here is a link to a [tutorial](TBD) on how to deploy your model with Seldon on Operate First.  

2. Write a short notebook that can send and receive inference requests from your model services endpoint to make it easy for others to test and try out. 


### 6. Evaluation:

Now that your model is out in the wild, its a good idea to see if it's actually useful to anyone and evaluate its real world performance. 

1. Share your work on [Slack](https://join.slack.com/t/operatefirst/shared_invite/zt-o2gn4wn8-O39g7sthTAuPCvaCNRnLww) (#data-science) or present it at the [Operate First Data Science Meet Up](https://github.com/aicoe-aiops/operate-first-data-science-community/issues/new/choose) to get people using and testing out your model. 

2. If there are any issues or areas to improve (which there will be) loop back to previous steps in this workflow and repeat until your project meets your desired outcome. 

