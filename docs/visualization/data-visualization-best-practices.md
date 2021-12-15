## Best Practices for Data Science Visualizations

### **Purpose**

_Visualizations are meant to supplement and provide clarity and insight into the claims being made about the data. People are generally not analytical and are naturally better at interpreting information visually. Thus, as a data scientist, it is important to present this information in a way that accurately provides a clear visual representation of the data, and what the story behind the data is._

### **Know your Audience**

1. Consider how much background information the viewer will have when deciding how much information to provide regarding the visualization
2. The goal is to provide enough information while still remaining clear and concise
3. If in doubt, have someone of a similar audience level look over the visualizations –
can they explain the visualization to you in the way you would like it to be interpreted?

### **Choosing the Correct Type of Visualization**

1. Consider the data you are presenting - categorical, numerical, continuous, discrete, etc.
2. Consider how it should be presented - plotted over time, histogram, heatmap, etc.
3. If in doubt, research methods that can be used to present your data type

### **Visualization Content**

1. Add descriptions! Clearly state...
    * What is being measured and plotted 
    * Why is it being measured and plotted - emphasize important points
    * Why is it important to visualize it specifically in the way it is being presented
    * What insights can be made based on the plots - include these points as a summary to explain any plots
2. More visualizations ≠ More clear
    * Each visualization should have a clear purpose and explanation so that it’s easier for the end user to understand

### **Formatting** **and Clean Up**

1. Add labels 
    * Title
    * Axis (include units if possible)
    * Capitalization in labels provides a cleaner look
    * Be consistent with labels
2. Plots should be the same size
3. Adjust plot, text, or axis size if necessary
    * i.e. if certain text is overlapping or not visible
4. Consider adding a legend if multiple things are being shown 
5. Ensure plots are scaled properly
    * If  multiple visualizations are being used for comparisons, scaling should be consistent across all visualizations
6. Rename things if necessary
    * Try to remove “-” and “_” from text within visualization labels
    * Try to remove abbreviations unless absolutely necessary

### **Examples**
Please view the _best-data-visualization-practices.ipynb_ Jupyter Notebook for examples of five basic data visualizations and their respective descriptions.

### **Libraries** 

1. [Seaborn ](https://seaborn.pydata.org/)
2. [Plotly](https://plotly.com/)
3. [Matplotlib](https://matplotlib.org/)


### **References :**

There are various guidelines for best Visualization practices, here are a few examples, but our principles take these best practices into consideration and targets Data Scientists working on visualizations using Jupyter Notebooks

* [https://towardsdatascience.com/8-best-visualizations-to-consider-for-your-data-science-projects-b9ace21564a](https://towardsdatascience.com/8-best-visualizations-to-consider-for-your-data-science-projects-b9ace21564a)
* [https://www.analytics8.com/blog/6-tips-to-create-powerful-data-visualizations/](https://www.analytics8.com/blog/6-tips-to-create-powerful-data-visualizations/)
* [https://www.columnfivemedia.com/25-tips-to-upgrade-your-data-visualization-design/](https://www.columnfivemedia.com/25-tips-to-upgrade-your-data-visualization-design/)
* [https://towardsdatascience.com/tips-for-effective-data-visualization-d4b2af91db37](https://towardsdatascience.com/tips-for-effective-data-visualization-d4b2af91db37)