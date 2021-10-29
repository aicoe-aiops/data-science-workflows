## How to Contribute

Please refer to this guide for information on how to contribute to our data science projects.

We encourage contribution to each of our [Data Science Projects](https://www.operate-first.cloud/data-science). In order to start contributing to our projects you can check out the "How to Contribute" section for each project under https://www.operate-first.cloud/data-science/.

### **GitHub Workflow**

1. Create an issue for every task you plan to work on.
2. Add the issue to the *New* column of the corresponding project board.
3. Let somebody from the team review the issue and refine it, until it's clear what should be done and what defines done.
   a. Provide some sort of acceptance criteria.
   b. Break the issue into smaller issues if it can't be done in one sprint.
4. Move the issue to the *To Do* column.
5. Once you start work on the issue move to the *In Progress* column and assign it to yourself.
6. Create a PR for the issue and reference the issue in the PR description.
7. Let somebody from the team review the PR - never merge your own PRs.

### **Contributing via Pull Requests**

Contributions to another data science project take the form of pull requests (PRs) against that project’s GitHub repository. Here are the steps for contributing using PRs:

1. Create a fork of the repository you wish to contribute to. The repo you fork from is referred to as the “upstream”. 
2. Clone your fork to your working environment (either local or on jupyterhub). 
3. Add the upstream repository you’ve forked from to your working repo: `git remote add upstream <upstream repo URL>`.
4. Create and checkout a new branch to work on the issue/feature you’d like to implement: `git checkout -b branch-name` will both create and switch over to a new branch.
5. Complete your work on this branch.
6. When the work is complete, push your changes to a feature branch on your remote fork. 
7. Make a PR from your fork’s feature branch to the upstream main.
8. Wait for someone to review your PR. They may suggest or request changes to your PR before approving it.
9. Once your PR is approved and merged into the repository, you can delete your branch. 

### **Reviewing Pull Requests**

Code reviews are common practice in the software engineering field and have been for some time. They provide developers with a well defined approach to sharing knowledge, ensuring exposure to new ideas and technologies, enforcing quality assurance of code and standards for the engineering process across both the code base and the team itself. As members of the AI CoE in the office of the CTO, we believe that having a well defined approach for how to do the same thing with data science and machine learning code is critical. Although, code is code, and we approach data science work as a subset of software engineering, there are some data science specific challenges associated with the code review process that should be addressed. Below are the 10 principles we use in our group to review data science work.

1. **Understand the Context :** Make sure you read the pull request description and any linked issues so you know the data scientist's goal. This will help you provide an appropriate level of feedback and focus on the meaningful changes.
2. **Rich Diffs :** Use tools like NBreview or nbdime when possible to review notebooks. These kinds of tools help you zero in on the notebook changes that actually matter.
3. **Is it Coherent? :** Notebooks generally contain a mix of code, markdown and plots. Do these elements reference each other correctly? Is the evaluation metric being used here suitable for the ML algorithm ? If you don’t understand something or are curious about why a certain approach was implemented, ask and get clarification.
4. **Check the Math! :** Machine Learning code can run successfully while still being wrong and not achieving the appropriate task. Read the notebook thoroughly and try to look for any mathematical errors in the code with reference to the PR's stated goal.
5. **Does it solve the right problem? :** Make sure the goals of the PR or notebook are met, the key takeaways are highlighted and the data scientist’s interpretation of any statistical and/ or experimental results are included.
6. **Introduce new libraries or technologies :** When working on a data science project, there might be times when you are aware of a library or new technology that can address the problem in a more efficient way. In such scenarios, you should suggest this approach in the code review.
7. **Is it reproducible? :** Are all of the dependencies used to run the code appropriately tracked using a pipfile or requirements.txt ? If you are unsure about any outputs or results, clone the pull request to your environment and run it yourself. It should run from top to bottom without error and generate the same outputs as are presented in the PR.
8. **Understand the visualizations :** When reviewing a PR that includes visualizations, make sure to check for the proper labeling of axes and ticks. All the values mentioned should be clear and have an explanation for each graph.
9. **Hardcoded Credentials and Paths :** Sometimes developers use hardcoded credentials, secrets and even data directories for quick tests and easy access when needed and forget to remove them before publishing them to github. When reviewing a Data Science code, make sure to check for any credentials/secrets as this practice poses a significant security risk that can allow attackers to bypass authentication mechanisms and ensure that the data management is handled properly and there are no hardcoded directories in the code.
10. **Evaluate the Output :** Everything looks right, but our validation results are way worse than expected. Sometimes the simplest things can go wrong like over-fitting, poorly tuned hyper-parameters or maybe an inappropriate distance metrics being used? Make sure to double-check all the smallest detail when reviewing a ML code.

### **References :**

There are various guidelines for standard Pull Request reviews, here are a few examples, but our principles take these best practices into consideration and targets Data Scientists working on AI/ML code using Jupyter Notebooks.
* https://thoughtbot.com/playbook/developing/code-reviews
* https://github.com/thoughtbot/guides/tree/main/code-review
* https://taingmeng.medium.com/what-you-should-look-out-for-when-you-review-pull-request-3f2d95a50ba9
* https://blog.codacy.com/how-to-code-review-in-a-pull-request/
* https://towardsdatascience.com/15-topics-to-consider-as-you-review-code-in-data-science-10eff0182e71
