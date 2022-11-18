# User navigation and visual link position on Wikipedia: Are they related?
*Towards understanding user behavior by exploiting the visual position of links in Wikipedia pages*

*SouvlADAki Team: Henri Allegre (henri.allegre@epfl.ch), Ioannis Bantzis (ioannis.bantzis@epfl.ch), Emmanouil Chatzakis (emmanouil.chatzakis@epfl.ch), Basile Tornare (basile.tornare@epfl.ch)*

This is the proposal of our ADA project, in which we are working on the Wikispeedia dataset. For this milestone we provide:
- This README as our project proposal
- The initial_analysis.ipynb which contains our initial analysis steps for the dataset. In the notebook you will find:
    - Code for initial processing of the dataset, data loading and basic analysis
    - Code for graph analytics and visualizations over the Wikispeedia graph
    - Code for path analysis
    - Code for our visual link position ideas.
- The wiki_graph.pdf which is the plot of the article network provided by the dataset.
- The page_pos_dict.json, which is a dictionary containing the link page structure of each article
- A folder containing the initial ideas for milestone P1.

This proposal follows the roadmap below:
* [Abstract](#abstract-closed_book)
* [Research Questions](#research-questions-question)
* [Methods](#methods-dart)
* [Proposed Timeline](#proposed-timeline-clock8)
* [Internal Organization](#internal-organization-memo)
* [Related Work](#related-work-copyright)
* [References](#references-coffee)
* [Questions to the TAs](#questions-to-the-tas-postbox)

## Abstract :closed_book:
Wikispeedia provides a rich source of information about user navigation over Wikipedia pages. In the Wikispeedia game, users are assigned the task of reaching a given target article from a given source article, exclusively by clicking the links that they encounter at each article. A crucial aspect of this navigation is that the users click on links by thinking which of them are the most semantically similar to their goal, using their common sense. In this work, we will study how the visual position of those links in a page affects the decision of the user, and how they impact the outcome of the game. We will provide insights about the positions of the most followed links and we will compare our findings with the user navigation knowledge that already exists in the literature. We will create our datastory with an emphasis on the statistical findings of the link position and human behavior and on the comparison of those results with the pre-existing knowledge in the field of user navigation. 

*Keywords: Wikipedia, Wikispeedia, User Navigation, Visual Link Position, Graph Analytics*


## Research Questions :question:
Below you may find our initial research questions that we will explore throughout our project.
- How does the position of links in the HTML page of Wikipedia affects the user behavior/selection?
- Are there specific sections in which their links are preferred by users when navigating the graph?
- Are the results of visual link analysis on Wikispeedia (which is based on human behavior) similar or different with the ones already observed in the literature?
- How our results on visual link analysis compare to analytics over the graph? Are the links that belong to the most "clicked" sections of the page also important in terms of graph analysis?


## Methods :dart:
Our initial analysis has been performed in a few parts. In our notebook, we justify how we preprocessed and cleaned the data.
After the preprocessing and shaping of the data we performed some **preliminary analysis** routines (using pandas, numpy, matplotlib), calculating:
  - Number of links per article
  - Number of articles per category
  - Path analysis ((un)-finished paths)
  - Time duration comparison per game for finished and unfinished paths
  - Comparison of backtracks between finished and unfinished paths

We experimented with a **wikipedia graph analysis** (using networkx):
  - We visualized the dense Wikispeedia network 
  - We simulated multiple graph analytics algorithms over the graph (Pagerank, Clustering Coef., Eigenvector Centrality)

We conducted a **link position analysis** (using BeautifulSoup):
The visual location of the links in wikipedia articles has been used in the past to study reader preferences. We propose a conceptually simple approach by analysing the paragraph location of the links. The HTML source code of a wikipedia is composed of paragraph elements containing the link elements of the page. We use the paragraph number of the link as an aggregate for the true visual location of the links in the page. With this approach we cannot distinguish between right or left but we can understand how far down the reader looks at every page before clicking the link. Furthermore, the advantage is the interpretability of this value as opposed to abstract (x,y) pixel coordinates. We can further distinguish between the lead section and the body section of the page as they are always seperated by an empty paragraph in the source code.

Our initial results support our intuition that users prefer links higher on the page and more often in the lead section. We "replay" each game and we keep track of the paragraph chosen at each click. Althought only around 20% of the links are located in the lead section, players prefer them 40% of the time. Similar figures are obtained by looking at each paragraph individually. Please refer to our notebook for more information.


## Proposed Timeline :clock8:
Here, we propose an indicative timeline that we will follow through the project. Please note that some project milestones P-MX could be implemented concurently.
* P-M1 [Preprocessing]. Enrich initial analysis to get more insights.
    * Date: 18/11/2022 (Milestone P2 Deadline)
* P-M2 [Preliminary Link Position Analysis]. Complete the preliminary link position analysis to summarize the first insights.
    * Date: 02/12/2022 (Along with homework 2, as many steps are already completed)
* P-M3 [Data Analysis]. Perform the link prediction analysis for our research questions. Use previous results to get insights about our goals, implement the programming part and provide the first visualizations.
    * Date: 08/12/2022
* P-M5 [Literature Comparison & Result Evalution]. Compare the results with existing literature in the field (see [References](#References)). Provide more graphs and update implementations. Also evaluate the comparison with graph analytics.
    * Date: 12/12/2022
* P-M6 [Datastory Draft and Preparations]. Start creating a template (sketch-like) for the datastory. Finalize all code implementations and decide about the final graphs we will present.
    * Date: 17/12/2022
* P-M7 [Final Results]. Gather the selected information and results for presentation, polish the repository data, finalize datastory.
    * Date: 23/12/2022 (Milestone P3 Deadline).


## Internal Organization :memo:
Here, we describe our internal organization. Our team meets up to coordinate and synchronize, so that every member is aware of the different aspects and components of our project, but every teammate is assigned specific parts of the work.
- Henri: Visualizations, Graph analytics classification
- Ioannis: Code maintenance, Visualizations
- Manos: Code maintenance, Website for Datastory
- Basile: Code maintenance, Website for Datastory, Visualizations, Datastory


## Related Work :copyright:
We are aware of the related work about studying the page structure of Wikipedia in order to determine the position of the links that users are most likely to follow (see [References](#References)). This work mainly consists of data gathered from users that "free browse" Wikipedia pages, without the aim of reaching a final target, and the users click on pages that they find interesting in general. We differ from this because our data come from users that click on pages that might lead them to their goal, exploiting their common sense about pages that are semantically similar to the final destination. This notion of semantic similarity between pages in not captured by previous work. An interesting aspect of our project would be to compare the existing results in the literature with our results, which will include the common sense knowledge from Wikispeedia.


## References :coffee:
1. Dimitrov, Dimitar, et al. "Visual positions of links and clicks on wikipedia." Proceedings of the 25th International Conference Companion on World Wide Web. 2016.
2. Dimitrov, Dimitar, et al. "What makes a link successful on wikipedia?." Proceedings of the 26th International Conference on World Wide Web. 2017.
3. West, Robert, Joelle Pineau, and Doina Precup. "Wikispeedia: An online game for inferring semantic distances between concepts." Twenty-First International Joint Conference on Artificial Intelligence. 2009.
4. Leskovec, Jure. "Human wayfinding in information networks." In WWW-12. 2012.
5.  Daniel Lamprecht, Dimitar Dimitrov, Denis Helic, and Markus Strohmaier."Evaluating and Improving Navigability of Wikipedia: A Comparative Study of Eight Language Editions." 2016.

## Questions to the TAs :postbox:
* Throughout our work we may encounter results that could provide more insights about our research questions. Can we modify our proposal according to those new results throughout the duration of the project?
