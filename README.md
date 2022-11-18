# Does the position of Wikipedia links affect user behavior?
Exploring Wikipedia links position exploiting user common sense.

Henri Allegre (henri.allegre@epfl.ch), Ioannis Bantzis (ioannis.bantzis@epfl.ch), Emmanouil Chatzakis (emmanouil.chatzakis@epfl.ch), Basile Tornare (basile.tornare@epfl.ch)

This is the proposal of our ADA project, in which we are working on the Wikispeedia dataset. For this milestone we provide:
- This README as our official project proposal
- The initial_analysis.ipynb which contains our initial analysis steps for the dataset. In the notebook you will find:
    - Code for initial processing of the dataset, data loading and basic analysis
    - Code for graph analytics and visualizations over the Wikispeedia graph
    - Code for path analysis
    - Preliminary code for our link position ideas.

This proposal follows the roadmap below:
* [Abstract](#Abstract)
* [Research Questions](#Research-Questions)
* [Methods](#Methods)
* [Proposed Timeline](#Proposed-Timeline)
* [Internal Milestones](#Internal-Milestones)
* [Libraries and Implementation](#Libraries-and-Implementation)
* [Related Work](#Related-Work)
* [References](#References)


## Abstract :closed_book:
Wikispeedia provides a rich source of information about user navigation over Wikipedia pages, when they are given the task of reaching a target article starting from a given one. A crucial aspect of this procedure is what links the users follow when they are navigating over a page, in order to reach the final target. Through this project we plan to study how the position of the links in the page affects the user decision, in order to understand how important is the location of the URL in the page. We will examine in which paragraphs or section of a Wikipedia article the most followed links are, and determine how their positions affect the behavior of the player. Additionaly, we will compare our findings with results from general visual link analysis over Wikipeedia, already implemented in literature, and explore if our results are compatible with graph analytics insights (e.g. if the popular links from Wikipedia belong to the most clicked positions of the page). We plan to focus our datastory on the importance of the position of a link in a page, and provide insight on how it affects the user behavior.


## Research Questions :question:
Below you may find our initial research questions that we will explore throughout our project.
- How does the position of links in the HTML page of Wikipedia affects the user behavior?
- Are there specific sections that their links are generally preffered? 
- Are the results of visual link analysis on Wikispeedia (which is based on common sense) similar or different with the ones already observed in the literature? 
- How are our results on visual link analysis compared to graph analytics over our data? Are the links that belong to the most "clicked" sections of the page also important in terms of graph analysis? 


## Methods :dart:
TODO


## Proposed Timeline :clock8:
Here, we propose an indicative timeline that we will follow through the project. Please note that some project milestones P-MX could be implemented concurently. 
* P-M1 [Preprocessing]. Enrich initial analysis to get more insights.
    * Date: 18/11/2022 (Milestone P2 Deadline)
* P-M2 [API]. Delevop a family of functions and routines to ease the analysis of link position. 
    * Date: 02/12/2022 (Along with homework 2, as the workload will be high in this period and we already provide some initial steps about his in our notebook)
* P-M3 [Data Analysis]. Perform the final analysis for our research questions. Use previous initial analysis to get insights about our goals, implement the analysis in code and provide the first visualizations.
    * Date: 08/12/2022
* P-M5 [Literature Comparison & Result Evalution]. Compare the results with existing literature in the field (see [References](#References)). Provide more graphs and update implementations.
    * Date: 12/12/2022 
* P-M6 [Datastory Draft and Preparations]. Start creating a template (sketch-like) for the datastory. Finalize all code implementations and decide about the final graphs we will present.
    * Date: 17/12/2022 
* P-MX [Final Results]. Gather all information we want to present, polish the repository data, finalize datastory.
    * Date: 23/12/2022 (Milestone P3 Deadline).



## Internal Organization :memo:
Our team meets up to coordinate and syncronize, so that every member is aware of the different
aspects of our project, but every teammate is assigned specific parts of the work.
- Henri: Visualizations
- Ioannis: Code maintenance, Visualizations
- Manos: Code maintenance, Website, Datastory
- Basile: Website, Visualizations, Datastory
All members contributed to the initial analysis steps.


## Libraries and Implementation :telescope:
The project will be implemented in Python, using the following (indicative) packages.
* Pandas and Numpy: For data analysis
* Matplotlib and Seaborn: For visualizations
* Networkx: For graph analytics
* BeatifulSoup: For HTML page analysis and link position


## Related Work :copyright:
There has been related projects about studying the HTML structure (see [References](#References)) of Wikipedia pages, in order to determine the position of the links that users are most likely to follow. Our proposal is different from this work, as the aforementioned studies analysize the structure of the page with users that are just traversing the data of Wikipedia website, thus the links they follow are the ones that they find "interesting" in general. In our work, we analyze the clicks that users did based on their target article, thus providing more insight about the connections they form between articles. An interesting comparison at our final step would be to compare the results from the analysis of the corresponding literature and study if there are differences in the observations. For example, literature claims that users tend to click articles on the left side of the page, when browsing Wikipedia pages. We can compare if this behavior still remains when the users have a target article. 


## References :coffee:
* Dimitrov, Dimitar, et al. "Visual positions of links and clicks on wikipedia." Proceedings of the 25th International Conference Companion on World Wide Web. 2016.
* Dimitrov, Dimitar, et al. "What makes a link successful on wikipedia?." Proceedings of the 26th International Conference on World Wide Web. 2017.
* West, Robert, Joelle Pineau, and Doina Precup. "Wikispeedia: An online game for inferring semantic distances between concepts." Twenty-First International Joint Conference on Artificial Intelligence. 2009.
* Leskovec, Jure. "Human wayfinding in information networks." In WWW-12. 2012.