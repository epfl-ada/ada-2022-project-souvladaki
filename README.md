# Does the position of Wikipedia links affect user behavior?
Exploring Wikipedia links position exploiting user common sense, meaning the human behavior with the goal of reaching a specific article.

Henri Allegre (henri.allegre@epfl.ch), Ioannis Bantzis (ioannis.bantzis@epfl.ch), Emmanouil Chatzakis (emmanouil.chatzakis@epfl.ch), Basile Tornare (basile.tornare@epfl.ch)

This is the proposal of our ADA project, in which we are working on the Wikispeedia dataset. For this milestone we provide:
- This README as our official project proposal
- The initial_analysis.ipynb which contains our initial analysis steps for the dataset. In the notebook you will find:
    - Code for initial processing of the dataset, data loading and basic analysis
    - Code for graph analytics and visualizations over the Wikispeedia graph
    - Code for path analysis
    - Preliminary code for our link position ideas.
- The wiki_graph.pdf which is the plot of the article network provided by the dataset.
- The page_pos_dict2.json, which is a dictionary containing the link page structure of each article
- A folder containing the initial ideas due to the milestone 1.

This proposal follows the roadmap below:
* [Abstract](#abstract-closed_book)
* [Research Questions](#research-questions-question)
* [Methods](#methods-dart)
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
- Are there specific sections that their links are generally prefered? 
- Are the results of visual link analysis on Wikispeedia (which is based on common sense) similar or different with the ones already observed in the literature? 
- How are our results on visual link analysis compared to graph analytics over our data? Are the links that belong to the most "clicked" sections of the page also important in terms of graph analysis? 


## Methods :dart:
Our initial analysis has been performed in few parts. All the way long, when an incoherence is found in the data, it is cleaned and justify in the code.
First the importation and shaping of the data into a convenient way (article/categories/links) with panda.
Some general analysis and visualization about the overall dataset (with panda,numpy):
  - Number of links per articles 
  - Number of articles per categories (a way of classification)
  - Path analysis ((un)-finished paths) 
  - Time duration distribution per game

The overall network analysis (with networkx):
  - The raw network map of wikispeedia (need to be clearer asap)
  - The rank of the most clicked articles 

Link position analysis (with BeautifulSoup):


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
* P-M7 [Final Results]. Gather all information we want to present, polish the repository data, finalize datastory.
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
* Networkx: For network analysis
* BeatifulSoup: For HTML page analysis and link position


## Related Work :copyright:
We are aware of the related work about studying the page structure of Wikipedia in order to determine the position of the links that users are most likely to follow (see [References](#References)). This work mainly consists of data gathered from users that "free browse" Wikipedia pages, without the aim of reaching a final target, and the users click on pages that they find interesting in general. We differ from this because our data come from users that click on pages that might lead them to their goal, exploiting their common sense about pages that are semantically similar to the final destination. This notion of semantic similairity between pages in not captured by previous work. An interesting aspect of our project would be to compare the existing results in the literature with our results, which will include the common sense knowledge from Wikispeedia. 


## References :coffee:
* Dimitrov, Dimitar, et al. "Visual positions of links and clicks on wikipedia." Proceedings of the 25th International Conference Companion on World Wide Web. 2016.
* Dimitrov, Dimitar, et al. "What makes a link successful on wikipedia?." Proceedings of the 26th International Conference on World Wide Web. 2017.
* West, Robert, Joelle Pineau, and Doina Precup. "Wikispeedia: An online game for inferring semantic distances between concepts." Twenty-First International Joint Conference on Artificial Intelligence. 2009.
* Leskovec, Jure. "Human wayfinding in information networks." In WWW-12. 2012.


## Questions to the TAs :postbox:
* Throughout our work we may encounter results that could provide more insights about our research questions. Can we (slightly) modify our proposal throughout the duration of the project.
* 