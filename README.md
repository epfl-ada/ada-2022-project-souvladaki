# Common sense on Wikipedia links position
This is the proposal of our ADA project, in which we are working on the Wikispeedia dataset. For this milestone we provide:
- This README as our official project proposal
- The initial_analysis.ipynb which contains some initial analysis steps for the dataset.

This proposal follows the roadmap below:
* [Abstract](#Abstract)
* [Research Questions](#Research_Questions))
* [Methods](#Methods))
* [Proposed Timeline](#References))
* [Internal Milestones](#References))
* [Libraries and Implementation](#References))
* [Related Work](#References))
* [References](#References))



## Abstract 
The Wikispeedia dataset is a rich source of information on how users are browing Wikipedia pages, in order to reach a target article from a given, initial one. Given this rich source of "common sense" information, we plan to study how the position of the links in the HTML page affects the user decision. 


## Research Questions
- Is the position of a link in a Wikipedia page affects the decision of the user?
- In which sections of the page are the most clicked links?
- Do graph analytics insights (e.g. popular links) affect the user decision, no matter their position?
- How do this analysis, based on people "common sense" compares to results of general analysis in visual link predictions of Wikipedia, already implemented in literature?


## Methods
TODO


## Proposed Timeline
* Step 1. Enrich our initial analysis with more insights (using Pandas, Matplotlib, Numpy and NetworkX)
    * Proposed deadline: 
* Step 2. Create a family of functions to be able to get the positions of the links in the article (using Pandas and Beatidul Soup). 
    * Proposed deadline: 
* Step 3. 
    * Proposed deadline: 
* Step 4. Explore the literature in order to compare the results of our analysis to other research outcomes in this direction.
    * Proposed deadline: 
* Step 5. Gather our research results, filter the most interesting and start preparing the presentation-report-datastory.
    * Proposed deadline: 


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
