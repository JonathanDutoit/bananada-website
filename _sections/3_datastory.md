---
title: DATA STORY
anchor: datastory
layout: page
---

## Data Story

### Do Pro-Trump and Non-Trump Communities Interact?

Which subreddits interact with pro-Trump communities? Do these communities interact at all? Are they isolated?

The answer these questions, we can directly analyze which subreddits interact the most with Trump-related subreddits.

The visualization below shows only strong links, defined as those above the 90th percentile. This focuses on the communities with the highest interaction between Trump-related and non–Trump-related subreddits, helping to keep the graph readable and avoid clutter.
<div class="clearfix vertical-center">
  <div class="col-9 sm-width-full">
    <iframe 
      src="{{ site.baseurl }}/assets/html/subreddit_interactions_graph.html" 
      style="width:100%; height:600px; border:0;" 
      class="sm-width-full">
    </iframe>
  </div>
  <div class="col-3 sm-width-full">
      When hovering over a node (subreddit), the graph displays its interactions with others. For non–Trump-related subreddits, this corresponds to the number of interactions with Trump-related communities. Here, interactions refer to posts that create hyperlinks from one subreddit to another.
      <br/><br/>
      The graph uses a spring lajyout while also preserving spatial relationships between subreddits based on the embedding.
  </div>
</div>

The following visualization represents the principal interacting communities with Pro-Trump subreddits represented as colorful nodes,
and grey points represent the rest of the subreddits.

<div class="clearfix">
     <iframe 
    src="{{ site.baseurl }}/assets/html/sub_embedding_interactions_visua.html" 
    style="width:100%; height:600px; border:0;" 
    class="sm-width-full">
  </iframe>
</div>

So, we have seen that yes, pro-Trump and non-Trump interact and they are not isolated one from the other. Next, we will analyze more these different aspects of these interactions, as well as they frequency. 

### How Did Interactions Evolve During the Campaign?
How did the frequency of exchanges evolve during the campaign?
Did interactions cease after the election?

In order to analyze how the U.S. presidential election affected interaction patterns between different Reddit communities, it is useful to study the frequency of exchanges between Trump-related and non-Trump-related communities.

<div class="clearfix vertical-center">
  <div class="col-7 sm-width-full mr-2">
      <img src="{{ site.baseurl }}/assets/images/monthly_growth.png" alt="User Embedding Projection" style="max-width: 800px; width: 100%; height: auto;"/>
  </div>
  <div class="col-5 sm-width-full ml-2">
      From the graph on the left, we see that the number of interactions rises quickly starting in early 2016, with a large spike in November 2016, which matches the U.S. presidential election on November 8.
      <br/><br/>

      After this peak, interactions slowly decrease but remain relatively high, likely because Trump’s election continued to drive discussions about how he was governing the country.

      <br/><br/>

      We also observe an increase in the number of subreddits involved, suggesting broader engagement across Reddit and interest from many different communities.
  </div>
</div>

### Who Initiates Cross-Community Interactions?

Who initiates cross-community interactions? Are interactions symmetrical?

In the graph below, we observe that **pro-Trump subreddits** appear much more frequently as **targets** than as sources of interactions, whether positive or negative.

This pattern is expected: the pro-Trump group is contrasted with the rest of the Reddit communities, which naturally leads to a larger volume of interactions directed toward them rather than originating from them.
<div class="clearfix">
 <img src="{{ site.baseurl }}/assets/images/trump_interactions_dual.png" alt="User Embedding Projection" style="width: 100%; height: auto;"/>
</div>

### What Triggered Peaks of Hostility?

What triggered the peaks of hostility?
Which political events or media controversies act as catalysts?

The interactions began on January 2016. This can be explained by his infamous quote: "I could shoot somebody and i wouldn't lose voters". This also marks the beginning of negative interactions involving Trump it being one way or the other. In March, it reached a steady level where it would stay there for the large part of our data story, excluding of course the major events. This was provoked by the start of his aggressive campaign. During the weekend of the 12th march 2016, we saw many protests happening and a Trump rally got cancelled because of protests in Chicago, Illinois. He refused to take responsibility for such a violent 48 hours and thus sparked fire to the relations between Blue and Red.
Obviously the 2 largest peaks of interactions occured during November 2016 and February 2017. The first date represents the month with the election results and the second occurs when Trump took office on January 20th.

### What Is the Overall Sentiment of Interactions?

What was the overall sentiment of the interactions?

<div class="clearfix">
 <img src="{{ site.baseurl }}/assets/images/plot_negative_interactions.png" alt="User Embedding Projection" style="width: 100%; height: auto;"/>
</div>
The graph above reveals an interesting dynamic. Pro-Trump communities become significantly more **prominent as sources** when we isolate **negative interactions**. For some months, they produce as many or even more negative interactions than they receive.

The curves for negative interactions show only partially similar slopes: although they do not perfectly overlap, they tend to rise and fall in a loosely coordinated way. This suggests some degree of reactive behavior, where increases in negative interactions from one side are often followed, though not always closely, by a corresponding response from the other.

The **total number of interactions** spikes sharply in **November 2016**, coinciding with the **U.S. presidential election won by Donald Trump**. This month also shows a substantial **rise in negative interactions**, indicating **heightened polarization during the election period**. 

Do pro-Trump communities use the same hostile language as opposing communities?

To answer this question, we perform a analysis of the language used in posts interacting with Trump written on pro-trump subreddits versus posts written on non-pro-trump subreddits. The graph below presents the temporal language analysis.

<div class="clearfix">
 <img src="{{ site.baseurl }}/assets/images/temporal_language_analysis.png" alt="User Embedding Projection" style="width: 100%; height: auto;"/>
</div>

We first note that the left-most values in the plot must be interpreted with a grain of salt, as they have **high variance due to a small amount of data** during this time period. 

Therefore, the first important dynamic we can observe is the spike in language feature importance in **August 2016**. This coincides with **allegations and media coverage regarding Russian interference in the election and Trump’s alleged connections to Russia**. In this spike, we can in particular observe that the language features of `liwc_friends` and `liwc_negemo` and `liwc_affect` spiked. This suggests that the non-pro-trump posts generally had a negative view of Trump, addressing the pro-trump community as a group negatively.

The second important spike occurs in **November/December 2016**. This coincides with the U.S. presidential election (November 8, 2016) and its results.



### What Kind of Conflict Is This? Ideology, Identity, or Belonging?

When communities attack, do they defend ideology, identity, or belonging?
How do linguistic markers reveal emotional grammar?

### Did Cross-Community Conflict Affect Community Growth?

Did exchanges contribute to community growth?
Which community experienced greater growth?

### Are These Communities Actually That Different?

Do targeted communities and pro-Trump communities share characteristics?
Are users similar?

From the T-SNE representation below, we can conclude that rather than ignoring one another, pro-Trump and non-Trump communities frequently intersected—often in politically adjacent spaces.

<div class="clearfix">
     <iframe 
    src="{{ site.baseurl }}/assets/html/tsne-plot.html" 
    style="width:100%; height:600px; border:0;" 
    class="sm-width-full">
  </iframe>
</div>

From the visualization, we see a massive cloud of interacting communities, representing the mainstream Reddit ecosystem. The Trump communities form a tight, dense line at the corner edge of this cloud. Thus, since they are among many other communities, we can conclude that they are not especially treating niche subjects. 

However, this structure reflects a high degree of homophily: users who participate in one Trump subreddit are very likely to participate in others as well. As a result, these communities create a compact neighborhood that remains largely peripheral to the rest of the network.

While the topics brought up on these subreddits are pretty similar to the ones globally on Reddit, they do so from an isolated “bubble” or community. They rarely mix with other users and stay tightly connected, despite having common discussion topics. 

<div class="clearfix vertical-center">
  <div class="col-4 sm-width-full left pr-3">
    The visualisation on the right shows that the subreddits are largely intermixed. Since this layout is based on a t-SNE projection of LDA topic distributions, this mixing suggests that the subjects and vocabulary discussed across these communities substantially overlap. In this space, Trump-related subreddits do not appear isolated, which indicates that they are not enclosed within a distinct topical or linguistic “bubble.” Instead, they engage with mainstream themes—such as politics, news, and culture—using the dominant language of Reddit, English.
  </div>

  <!-- Right Column: Dataset image -->
  <div class="col-8 sm-width-full left pl-3">
    <iframe 
    src="{{ site.baseurl }}/assets/html/LDA-topic-map.html" 
    style="width:100%; height:600px; border:0;" 
    class="sm-width-full">
  </iframe>
  </div>
</div>


One notable exception is `r/trump_train` (outlier), isolated at the top of the graph. This separation may indicate that the subreddit focuses on more niche topics and/or exhibits a distinct discussion style compared to the other subreddits in the projection. Further, more targeted analysis would be required to determine whether r/trump_train represents a typical statistical outlier or an extreme case of topical or community isolation among smaller Reddit groups.

**Summary**:
- Semantically (_LDA Chart_): These communities are linked to the mainstream. They talk about what everyone else is talking about.
- Structurally (_t-SNE Chart_): They behave like a fortress. While they observe the mainstream topics, they do so from a tightly clustered position at the edge of the ecosystem, rarely mixing freely with the general population despite discussing the same news.

<div class="clearfix">
  <h4 class="lh-condensed font-smoothing">User Embeddings Comparison</h4>
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