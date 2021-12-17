# AI Ops Projects 

_This document contains a list of active projects within the AI Ops Team_

1. **AI-CoE SRE** : The goal of this project is to outline and practice a common ‘bleeding edge technology’ approach for all AI CoE endeavors to operate their software components and services. All services target OpenShift as the primary platform, but still extending to the full stack - from underlying hardware up to the applications running on top of a service. E.g. supporting custom AI service on Seldon provided by DataHub on PSI on OpenStack. 

2. **AI-Enablement Initiative** : At AICoE, we have been actively involved in collaborating with teams within Red Hat to advance different products, services and operations using AI. In order to enable and/or educate teams and get engineers or stakeholders more involved in the projects, and in order to get them to be able to effectively use the solutions, we are working on a way to  streamline the process in which we make the engagements and measure the impact of each project. 

3. **Auto FAQ** : The OpenShift product management team has reached out to the AI CoE regarding developing a tool that could generate and continuously update an FAQ based on the content in our mailing lists. The stated goal of this project is to, “use Machine Learning technique(s) to auto-generate user-visible FAQs and keep them updated.” Which could be framed as a question answering systems or a text generator. This is being done in order to reduce the amount of time Openshift PM’s spend answering similar or duplicate questions.

4. **Ceph Data Drive Failure** : Recently, the Ceph team started collecting user data to create their own dataset. Since this data comes from actual Ceph clusters, the model can be made more accurate by re-training on this dataset. But since the data is not labelled, i.e. it does not have information on whether or not a hard drive failed, training our supervised model is not straightforward. The goal of this project is to explore whether, given the unlabeled data collected from Ceph users, it is possible to perform the same analysis as we did for Backblaze data, by implementing a heuristic or an active learning approach to generate labels.  

5. **CJA Topic Modeling** : The Voice of Customer team has been focused on developing a process to systematically track customer sentiment for a larger portfolio of our customers and products in order to know our customers better. The VoC team collaborated with AICoE to scale this process by using AI techniques to gather meaningful insights from customer data. In order to analyze customer feedback for themes we used topic analysis techniques and were able to detect key themes and topics in customer verbatim that need attention. By tying the key themes and topics to customer satisfaction scores and customer sentiment values, we can get a fair understanding of customer’s pain points and help one better improve one’s products and services. 

6. **Cloud Price List Analysis** : Most customers of Red Hat use various cloud services like Azure, AWS and many others for different tasks. These cloud providing companies keep changing their prices time to time. It would be really helpful to the customer to understand how the prices are changing and take appropriate measures to best manage the cost. This project aims to come up with solutions that will help the Cost Management team to make wise decisions on how cloud services should be managed with time.

7. **Data Science Workflows** : AI Ops team has been working on developing a more structured process around how we manage, execute and deliver on our data science projects, especially those where we collaborate with other Red Hat teams. Having a common framework that we can all start to build from as the team grows and continues to take on more data science projects, it will be hugely beneficial to have an agreed upon and documented process like this in place. And more important than just the existence of some documentation, is that we actually use these tools and find that they provide us with some value. Meaning, that we should keep updating and evolving this process to suit our needs.

8. **Insights Configuration Files Analysis** : Red Hat Insights is a tool that provides analytics for Red Hat systems. It collects the system data to find vulnerabilities through manually written rules. The systems data is collected periodically and stored in a warehouse for data analysis. The data comprises hardware and software description, configurations, and logs of the systems. In this project, the focus is on analysis of configuration files. Some of these files are written by experts and customized by users such as the tuned files. Others are completely configured by end users such as the sssd configuration files. This project aims to develop data-driven methods to analyze these configuration files and detect misconfiguration in these files.

9. **Insights Drift Analysis Baselines** : Drift Analysis application enables users to compare system configuration of one system to other systems or baselines in the cloud management services inventory. Baselines are configurations (set of name / value facts) that can be defined from scratch, as a copy of an existing system configuration, or as a copy of an existing baseline. We propose a method to recommend baseline configurations automatically to the users. They can then use the recommendation or tweak it further to compare their systems with the baselines. This approach of recommending baselines by utilizing the knowledge of other systems in the account would save time for users by identifying and recommending baselines. This would assist in standardizing RHEL configurations and in improving RHEL configuration management and operations.

10. **Insights Invocation Hints** : Given a timestamp of insight archive uploads, deduce how systems checkin and how they were initially registered. 

11. **Insights SAP Analysis** : In this project, we analyze SAP instances on user systems through data collected from Insights. We create a superset dashboard that illustrates the topology of SAP workloads running on RHEL systems.

12. **OCP Alert Prediction** : If a customer’s OpenShift cluster goes down, it can have a significant impact on their business. Since there are a variety of reasons why an OpenShift cluster might fail, finding and fixing the issue that the cluster suffers from is not always trivial. However, if we can predict in advance whether a cluster will run into a given issue, then we may be able to fix it before it fails or before it severely impacts the customer. Issues in a cluster are often defined by, or closely related to, the alerts that it fires. So predicting alerts can be a step towards predicting the underlying issue. Thus, the goal of this project is to predict whether a cluster will fire a given alert within the next hour. 

13. **OCP4 Anomaly Detection** : OCP4 deployments can suffer from a number of different issues and bugs. It can be tedious for an engineer to inspect and diagnose each deployment individually, which in turn can adversely affect customer experience. In this project, we work on the following two initiatives to address this problem.
    * Anomaly Detection: In this approach, we try to identify issues before they occur, or before they significantly impact customers. To do so, we find deployments that behave “anomalously” and try to explain this behaviour.
    * Diagnosis Discovery: In this approach, we try to identify deployments that exhibit similar “symptoms” (issues), and determine exactly what makes these deployments similar to one another. The support engineer can then use this information to determine the “diagnosis” of the issues, and apply the same or similar fix to all the deployments.

14. **Openshift SME Mailing List Analysis** : The Openshift-SME mailing list contains many discussions about the issues occurring with OpenShift deployments on a monthly basis and suggestions for how to address the issues. This project aims to help the Openshift product management team bring a more data driven approach to their planning process by performing text analysis on the openshift-sme mailing list and gathering insights into the trends in the email conversations.

15. **Prometheus-api-client python** : A python library to make querying prometheus data simpler and also convert metric data into a more Data Science suitable format of a pandas dataframe.

16. **Sentiment Analysis** : Red Hat has a variety of text based artifacts coming from sources starting from partner and customer engagements to documentation and communication logs. These text based artifacts are valuable and can be used to generate business insights and inform decisions if appropriately mined. The goal of this project is to allow other teams across Red Hat to have a tool at their disposal allowing them to analyze their text data and make informed decisions based on the insights gained from them.   

17.  **Sync Pipelines** : Data ingress pipelines for DataHub via Argo pipelines.  