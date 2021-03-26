# Guidelines for Reviewing Data Science Code

Code reviews are common practice in the software engineering field and have been for some time. They provide developers with a well defined approach to sharing knowledge, ensuring exposure to new ideas and technologies, enforcing quality assurance of code and standards for the engineering process across both the code base and the team itself.  As members of the AI CoE in the office of the CTO, we believe that having a well defined approach for how to do the same thing with data science and machine learning code is critical. Although, code is code, and we approach data science work as a subset of software engineering, there are some data science specific challenges associated with the code review process that should be addressed. Below are the 11 guidelines we use in our group to review data science work.     

1. **Understand the PR** : When asked for a review, make sure to first understand the issue linked and the goal of the pull request.

2. **NB Review** : Use tools like NB review when possible while reviewing Jupyter Notebooks, this will make reviewing the notebooks easier.

3. **Don’t be afraid to ask questions** : When reviewing someone’s code, if you don't understand something or are curious about why a certain approach was implemented, ask questions and get clarification. 

4. **Read Carefully** : Read the notebook thoroughly and try to look for logical errors or bugs in the code. Make sure you bring up any possible edge cases the code will not handle correctly.

5. **Find ways to clean and condense the code** : Suggest alternate approaches to perform a similar action as the current code. This will present new techniques and various implementations for the team to consider.

6. **Future steps and actions** : Make sure the goals of the notebook are met in the end, the key takeaways are highlighted and should contain the data scientist's interpretation of any statistical and/ or experimental results. While reviewing the code, it is important to ensure that future actions are mentioned so that readers or future developers picking up the work will know the developer's intentions for follow up experiments or implementations. 

7. **Introduce new libraries or technologies** : When working on a data science project, there might be times when you are aware of a library or new technology that can address the problem in a more efficient way. In such scenarios, you should suggest this approach in the code review.

8. **Code Optimization** : Suggest ways to restructure nested functions/loops if possible. 

9. **Evaluate the output for each cell** : If you are unsure about any output, clone the pull request to your environment and try to run it yourself for better understanding.

10. **Understand the visualizations** : When reviewing a PR that includes visualizations, make sure to check for the proper labeling of axes and ticks. All the values mentioned should be clear and have an inference for each graph.

11. **Readability and Code Commenting** : Well commented code makes it easier to understand what the code is doing and, more importantly, why it is doing it a particular way. Comments are meant to be read by future programmers and should be clear and precise. If you need to pause frequently during the review yourself, it might be because readability is not that great and readability also depends on having appropriate comments in the code.
