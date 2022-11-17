# Common sense on Wikipedia links position
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


## Abstract 
The Wikispeedia dataset is a rich source of information on how users are browing Wikipedia pages, in order to reach a target article from a given, initial one. Using this rich source of "common sense" information, we plan to study how the position of the links in the HTML page affects the user decision, in order to gain insight on how the users tend to examine a given article, in order to proceed to the a following one. Our novelty lies in the fact that, although visual link analysis has been studied in the corresponding literature, we will combine the common sense data and study how the users traverse pages when browsing in Wikipedia when they have a goal to reach a final article, instead of "free" browsing a website. We want to study how the position of such links affects the users decision, the section of the page where the most followed links belong, combine our methods with graph analytics tasks to see if those links are also important in terms of graph analytics and compare our findings with the corresponding available research in this direction.


## Research Questions
- Is the position of a link in a Wikipedia page affects the decision of the user?
- In which sections of the page are the most clicked links?
- Do graph analytics insights (e.g. popular links) affect the user decision, no matter their position?
- How do this analysis, based on people "common sense" compares to results of general analysis in visual link predictions of Wikipedia, already implemented in literature?


## Methods
TODO


## Proposed Timeline
* Step 1. Enrich our initial analysis with more insights (using Pandas, Matplotlib, Numpy, BeatifulSoup and NetworkX)
    * Proposed deadline: Milestone P2 deadline, 18/11/2022
* Step 2. Create a family of functions to be able to get the positions of the links in the article (using Pandas and BeatifulSoup) and start making initial steps towards this direction. 
    * Proposed deadline: 
* Step 3. 
    * Proposed deadline: 
* Step 4. Explore the literature in order to compare the results of our analysis to other research outcomes in this direction.
    * Proposed deadline: 
* Step 5. Gather our research results, filter the most interesting and start preparing the presentation-report-datastory.
    * Proposed deadline: Milestone P3 deadline, 23/12/2022.


## Internal Milestones



## Libraries and Implementation
The project will be implemented in Python, using the following packages.
* Pandas and Numpy: For data analysis
* Matplotlib and Seaborn: For visualizations
* Networkx: For graph analytics
* BeatifulSoup: For HTML page analysis


## Related Work
There has been related projects about studying the HTML structure (see [References](#References)) of Wikipedia pages, in order to determine the position of the links that users are most likely to follow. Our proposal is different from this work, as the aforementioned studies analysize the structure of the page with users that are just traversing the data of Wikipedia website, thus the links they follow are the ones that they find "interesting" in general. In our work, we analyze the clicks that users did based on their target article, thus providing more insight about the connections they form between articles. An interesting comparison at our final step would be to compare the results from the analysis of the corresponding literature and study if there are differences in the observations. For example, literature claims that users tend to click articles on the left side of the page, when browsing Wikipedia pages. We can compare if this behavior still remains when the users have a target article. 


## References
* Dimitrov, Dimitar, et al. "Visual positions of links and clicks on wikipedia." Proceedings of the 25th International Conference Companion on World Wide Web. 2016.
* Dimitrov, Dimitar, et al. "What makes a link successful on wikipedia?." Proceedings of the 26th International Conference on World Wide Web. 2017.
* West, Robert, Joelle Pineau, and Doina Precup. "Wikispeedia: An online game for inferring semantic distances between concepts." Twenty-First International Joint Conference on Artificial Intelligence. 2009.
* Leskovec, Jure. "Human wayfinding in information networks." In WWW-12. 2012.