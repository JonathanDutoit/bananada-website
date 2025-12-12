---
title: DATA STORY
anchor: datastory
layout: page
---

## Data Story
- **Time Series of Interactions and their nature:**
(Claudie add)
Obviously the 2 largest peaks of interactions occured during November 2016 and February 2017. The first date represents the month with the election results and the second occurs when Trump took office on January 20th. 


- **Latent Dirichlet Allocation (topic map) analysis of the communities:**
As we can see all subreddits are pretty mixed, this being a T-SNE projection , we can conclude that the subjects and vocabulary treated by those are mixed between one another. The Trump subreddits are not isolated in any way, which would be revealing of being in a “bubble”. They speak about mainstream topics such as politics, news, culture, in the predominant language of Reddit: English. 
However we can see one outlier being r/trump_train. This subreddit can be seen isolated at the top of the graph. This can probably mean that this specific subreddit treats certain niche subjects and/or is particularly isolated in terms of discussions compared to the rest of the plotted subreddits. A more detailed analysis on this specific case could be made to have more insight on whether or not r/trump_train is a “normal” outlier or a rather extreme case of small communities of redditors.

- **t-SNE projection of Trump with the top 10% most interacting communities:**
Here, we see a massive cloud of Interacting communities, representing the mainstream Reddit ecosystem. The Trump communities form a tight, dense line at the bottom edge of this cloud.
Since the Trump communities lie in the middle of the graph, we can conclude that they are not especially treating niche subjects. They most likely interact with mainstream content as we already saw with the LDA topic map.
However: The Trump subreddits are all gathered into a small “cluster” which indicates extreme homophily,users in one Trump subreddit are extremely likely to be in the others. They form a tight neighborhood that sits on the periphery of the graph.
Conclusion: While the topics brought up on these subreddits are pretty similar to the ones globally on Reddit, they do so from an isolated “bubble” or community. They rarely mix with other users and stay tightly connected, despite having common discussion topics. 

- **t-SNE + LDA: Distinct but connected:**
- Semantically (LDA Chart): These communities are linked to the mainstream. They talk about what everyone else is talking about.
- Structurally (t-SNE Chart): They behave like a fortress. While they observe the mainstream topics, they do so from a tightly clustered position at the edge of the ecosystem, rarely mixing freely with the general population despite discussing the same news.
