---
title: DATA STORY
anchor: datastory
layout: page
---

## Data Story

### How did the frequency of exchanges evolve during the campaign? Did interactions cease after the election?
(TO BE MODIFIED) Although the user and subreddit embeddings do not provide any information about the interactions in the reddit network, they contain crucial information about the layout of reddit. They essentially allow us to visualize how similar users and subreddits are.

These datasets will be used to differentiate communities within Reddit. In particular, we use them to identify clusters of thematically related subreddits and groups of users with shared interests or behavioral patterns. By examining the spatial relationships between embeddings, we can detect natural boundaries between communities and uncover latent structures that may not be visible through direct interaction data alone.

Combined with the later analyses of interactions between subreddits, we will better understand how these communities relate to one another — whether through cooperation, conflict, or shared discourse. This integration of similarity-based and interaction-based perspectives will help reveal both the internal cohesion of communities and the larger dynamics shaping Reddit’s social and ideological landscape.
In order to analyze how the U.S. presidential election affected interaction patterns between different Reddit communities, it is useful to study the frequency of exchanges—for example, discussions about one of the candidates. In this case, we examine the frequency of interactions between Trump-related and non-Trump-related communities.

To begin, we first need to identify the subreddits related to Trump. This is achieved by clustering subreddit embeddings, starting from a seed set of known Trump-related subreddits.

With the clustering pipeline as previously, we use the same the core of Trump-related subreddits relevant_list.
<div class="clearfix">
  <iframe 
    src="{{ site.baseurl }}/assets/html/subreddit_interactions_graph.html" 
    style="width:100%; height:600px; border:0;" 
    class="sm-width-full">
  </iframe>
</div>


Explanation of the graph:

When hovering over the nodes (subreddits), the graph displays the interactions each subredddit has with others. By "interactions" we mean of course posts that create hyperlinks from one subreddit to another.

The visualized data includes only strong links, defined as those above the 90th percentile threshold. In other words, it focuses on the communities that interact the most between Trump-related and non-Trump-related subreddits. This filtering helps prevent the graph from becoming too cluttered.

The total number of interactions (without filtering ior percentile threshold) between Trump-related and non-Trump-related communities can be summarized as follows:
<div class="clearfix">
  <img src="{{ site.baseurl }}/assets/images/monthly_growth.png" alt="User Embedding Projection" style="max-width: 800px; width: 100%; height: auto;"/>
</div>
- **Time Series of Interactions and their nature:**
(Claudie add)
The interactions began on January 2016. This can be explained by his infamous quote: "I could shoot somebody and i wouldn't lose voters". This also marks the beginning of negative interactions involving Trump it being one way or the other. In March, it reached a steady level where it would stay there for the large part of our data story, excluding of course the major events. This was provoked by the start of his aggressive campaign. During the weekend of the 12th march 2016, we saw many protests happening and a Trump rally got cancelled because of protests in Chicago, Illinois. He refused to take responsibility for such a violent 48 hours and thus sparked fire to the relations between Blue and Red.
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

<div class="clearfix">
  <h3 class="lh-condensed font-smoothing">User Embeddings Comparison</h3>
</div>
To understand how different communities of Reddit users behave and relate to each other, we analyzed user embeddings—vector representations that capture behavioral patterns and similarity between users. Users are represented as an embedding, and we measured similarity between any two users by using cosine similarity, a common metric for comparing high-dimensional vectors. Higher cosine similarity indicates that two users tend to express themselves in more similar ways.

This analysis focuses on three distinct Reddit user populations. The first group includes users active in pro-Trump subreddits, communities known for strong support of Donald Trump and related political discourse. The second group consists of users engaged in feminist subreddits, where conversations center on gender equality, social justice, and feminist theory. The third group is a randomly sampled set of Reddit users, serving as a neutral baseline to represent general platform activity without any ideological or topical filtering.

<div class="clearfix vertical-center">
  <div class="col-6 sm-width-full left pr-3">
    <div class="clearfix prose py-2" markdown="1">

  | Comparison                          | Mean Cosine Similarity |
|-------------------------------------|--------------------------|
| The_Donald vs Feminism              | 0.154                  |
| The_Donald vs Random Users          | 0.146                  |
| Feminism vs Random Users            | 0.164                  |
| The_Donald (within-group)           | 0.166                  |
| Feminism (within-group)             | 0.217                  |
| Random Users (within-group)         | 0.186                  |

  </div>
  </div>

  <!-- Right Column: Dataset image -->
  <div class="col-6 sm-width-full left pl-3">
    <img src="{{ site.baseurl }}/assets/images/user_embedding_projection.png" alt="User Embedding Projection" style="max-width: 500px; width: 100%; height: auto;"/>
  </div>
</div>

Overall, the embedding comparison shows that users from pro-Trump and Feminism communities form two distinct populations with noticeably lower similarity across groups than within them. Both groups exhibit only modest internal cohesion, but the Feminism group is consistently more internally similar and forms a more compact cluster, while the Trump group is more dispersed and resembles the randomness of general Reddit users. Despite the low absolute similarity values, the separation between groups remains visible in the 2D projection, confirming that the embeddings capture meaningful differences in interest. However, the lack of strong, well-defined clusters also indicates that users—even within the same community—are highly diverse.