---
title: DATA STORY
anchor: datastory
layout: page
---

## Data Story

<div style="font-family: Verdana, Geneva, sans-serif; color: black; max-width: 700px;">

  <!-- Community -->
  <div style="font-size: 12px; font-weight: bold; margin-bottom: 2px;">
    r/ADA
  </div>

  <!-- User -->
  <div style="font-size: 12px; color: #555; margin-bottom: 10px;">
    u/BananaADA
  </div>

  <!-- Title -->
  <div style="font-size: 22px; font-weight: bold; margin-bottom: 14px;">
    We dug into 3 years of Reddit data to see how the 2016 election warped the platform. Here’s what we found.
  </div>

  <!-- Body text -->
  <div style="font-size: 14px; line-height: 1.6;">
    <p>
      Alright folks, after spending way too many nights staring at hyperlink graphs and user embeddings instead of touching grass, our team finally wrapped up a deep dive into how Reddit reacted to the 2016 U.S. election.
    </p>

    <p>
      You know how everyone remembers that era as a nonstop flame war between Trump supporters and… basically everyone else? We wanted to check whether that collective memory actually shows up in the data. Were pro-Trump subs isolated echo chambers? Were they constantly fighting with the rest of Reddit? Did hostility spike around real-world events, or was it just Reddit being Reddit?
    </p>

    <p>
      So we pulled together two massive datasets and tried to reconstruct the social dynamics of that period.
    </p>

    <p>
      If you’ve ever wondered what political polarization looks like in network form, or whether the stereotypes about these communities hold up, this is for you.
    </p>
  </div>

</div>


### Do Pro-Trump and Non-Trump Communities Interact?

Which subreddits interact with pro-Trump communities? Do these communities interact at all? Are they isolated?

<div style="font-family: Verdana, Geneva, sans-serif; color: black; max-width: 700px; margin-top: 20px;">

  <div style="font-size: 12px; color: #555; margin-bottom: 6px;">
    <strong>u/BlueStateReader</strong>
  </div>

  <div style="font-size: 14px; line-height: 1.6; padding-left: 10px; border-left: 3px solid #e0e0e0;">
    Honestly, I feel like Trump subs never talk to anyone outside their bubble.
    Do they even interact with the rest of Reddit?
  </div>

</div>

<div style="font-family: Verdana, Geneva, sans-serif; color: black; max-width: 700px; margin-top: 20px;">

  <div style="font-size: 12px; color: #555; margin-bottom: 6px;">
    <strong>u/Patriot1776</strong>
  </div>

  <div style="font-size: 14px; line-height: 1.6; padding-left: 10px; border-left: 3px solid #e0e0e0;">
    Lol what? People link to us all the time and usually to complain. Trust me, we see them.
  </div><br><br>

</div>  


The answer to these questions, we can directly analyze which subreddits interact the most with Trump-related subreddits.

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
      The graph uses a spring layout while also preserving spatial relationships between subreddits based on the embedding.
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


<div style="font-family: Verdana, Geneva, sans-serif; color: black; max-width: 700px; margin-top: 20px;">

  <div style="font-size: 12px; color: #555; margin-bottom: 6px;">
    <strong>u/BananADA</strong>
  </div>

  <div style="font-size: 14px; line-height: 1.6; padding-left: 10px; border-left: 3px solid #e0e0e0;">
    Turns out you’re both right. The interactions do happen, and they’re not rare, but they’re concentrated among a handful of highly active communities. Not isolation, but definitely not free flowing conversation either. Next up: breaking down these interactions and their frequency.
  </div>

</div>

### How Did Interactions Evolve During the Campaign?
How did the frequency of exchanges evolve during the campaign?
Did interactions cease after the election?

<div style="font-family: Verdana, Geneva, sans-serif; color: black; max-width: 700px; margin-top: 20px;">

  <div style="font-size: 12px; color: #555; margin-bottom: 6px;">
    <strong>u/LoveHistory</strong>
  </div>

  <div style="font-size: 14px; line-height: 1.6; padding-left: 10px; border-left: 3px solid #e0e0e0;">
    Did things actually heat up during the campaign, or is that just how we remember it?
  </div>

</div>

<div style="font-family: Verdana, Geneva, sans-serif; color: black; max-width: 700px; margin-top: 20px;">

  <div style="font-size: 12px; color: #555; margin-bottom: 6px;">
    <strong>u/PoliticalJunkie</strong>
  </div>

  <div style="font-size: 14px; line-height: 1.6; padding-left: 10px; border-left: 3px solid #e0e0e0;">
    If Reddit didn’t explode in 2016, I’ll eat my keyboard.
  </div><br/><br/>

</div>

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

<div style="font-family: Verdana, Geneva, sans-serif; color: black; max-width: 700px; margin-top: 20px;">

  <div style="font-size: 12px; color: #555; margin-bottom: 6px;">
    <strong>u/BananADA</strong>
  </div>

  <div style="font-size: 14px; line-height: 1.6; padding-left: 10px; border-left: 3px solid #e0e0e0;">
    The graph doesn’t lie. Activity skyrockets in early 2016, peaks in November, the month of the election, then slowly cools off but never returns to baseline. The election sparked conversation, and Trump’s way of governing kept fueling it
  </div>

</div>


### Who Initiates Cross-Community Interactions?

Who initiates cross-community interactions? Are interactions symmetrical?

<div style="font-family: Verdana, Geneva, sans-serif; color: black; max-width: 700px; margin-top: 20px;">

  <div style="font-size: 12px; color: #555; margin-bottom: 6px;">
    <strong>u/NeutralObserver</strong>
  </div>

  <div style="font-size: 14px; line-height: 1.6; padding-left: 10px; border-left: 3px solid #e0e0e0;">
    I always assumed Trump subs were the ones starting fights. Isn’t that their whole reputation?
  </div>

</div>

<div style="font-family: Verdana, Geneva, sans-serif; color: black; max-width: 700px; margin-top: 20px;">

  <div style="font-size: 12px; color: #555; margin-bottom: 6px;">
    <strong>u/ConservativeCoder</strong>
  </div>

  <div style="font-size: 14px; line-height: 1.6; padding-left: 10px; border-left: 3px solid #e0e0e0;">
    Bro, have you seen how often people link to us just to dunk? We’re basically a magnet.
  </div><br><br>

</div>


In the graph below, we observe that **pro-Trump subreddits** appear much more frequently as **targets** than as sources of interactions, whether positive or negative.

This pattern is expected: the pro-Trump group is contrasted with the rest of the Reddit communities, which naturally leads to a larger volume of interactions directed toward them rather than originating from them.
<div class="clearfix">
 <img src="{{ site.baseurl }}/assets/images/trump_interactions_dual.png" alt="User Embedding Projection" style="width: 100%; height: auto;"/>
</div>

<div style="font-family: Verdana, Geneva, sans-serif; color: black; max-width: 700px; margin-top: 20px;">

  <div style="font-size: 12px; color: #555; margin-bottom: 6px;">
    <strong>u/BananADA</strong>
  </div>

  <div style="font-size: 14px; line-height: 1.6; padding-left: 10px; border-left: 3px solid #e0e0e0;">
    First things first guys, this is about interactions in general, not specifically attacks. Trump related subs are far more often targets than sources. The traffic flows naturally toward them more than away from them.  Now let’s see what happens when we focus on attacks.
  </div>

</div>




### What Is the Overall Sentiment of Interactions?

From the dataset paper, we already know that most interactions are positive, and the graph above confirms it. So let’s take a closer look at the negative interactions, the ones having the strongest impact.

<div style="font-family: Verdana, Geneva, sans-serif; color: black; max-width: 700px; margin-top: 20px;">

  <div style="font-size: 12px; color: #555; margin-bottom: 6px;">
    <strong>u/DramaKing</strong>
  </div>

  <div style="font-size: 14px; line-height: 1.6; padding-left: 10px; border-left: 3px solid #e0e0e0;">
    Can you see the plot twist coming?
  </div>

</div>


<div class="clearfix">
 <img src="{{ site.baseurl }}/assets/images/plot_negative_interactions.png" alt="User Embedding Projection" style="width: 100%; height: auto;"/>
</div>

The graph above reveals an interesting dynamic. Pro-Trump communities become significantly more **prominent as sources** when we isolate **negative interactions**. For some months, they produce as many or even more negative interactions than they receive.

The curves for negative interactions show only partially similar slopes: although they do not perfectly overlap, they tend to rise and fall in a loosely coordinated way. This suggests some degree of reactive behavior, where increases in negative interactions from one side are often followed, though not always closely, by a corresponding response from the other.


### What Triggered Peaks of Hostility?

What triggered the peaks of hostility?
Which political events or media controversies act as catalysts?


The interactions began on January 2016. This can be explained by his infamous quote: "I could shoot somebody and i wouldn't lose voters". This also marks the beginning of negative interactions involving Trump it being one way or the other (see previous graph). In March, it reached a steady level where it would stay there for the large part of our data story, excluding of course the major events. This was provoked by the start of his aggressive campaign. During the weekend of the 12th march 2016, we saw many protests happening and a Trump rally got cancelled because of protests in Chicago, Illinois. He refused to take responsibility for such a violent 48 hours and thus sparked fire to the relations between Blue and Red.
Obviously the 2 largest peaks of interactions occured during November 2016 and February 2017. Those are the result of, respectively, the election month and "Not My Presidents Day", a series of rallies against the president, held on Washington's Birthday, February 20, 2017, after Trump took office.


<div style="font-family: Verdana, Geneva, sans-serif; color: black; max-width: 700px; margin-top: 20px;">

  <div style="font-size: 12px; color: #555; margin-bottom: 6px;">
    <strong>u/DataLinguist</strong>
  </div>

  <div style="font-size: 14px; line-height: 1.6; padding-left: 10px; border-left: 3px solid #e0e0e0;">
    Do pro-Trump communities use the same hostile language as opposing communities?
  </div>
</div>

### How does pro-Trump posts differs from others?

To answer this question, we perform a analysis of the language used in posts interacting with Trump written on pro-trump subreddits versus posts written on non-pro-trump subreddits. The graph below presents the temporal language analysis.

<div class="clearfix">
 <img src="{{ site.baseurl }}/assets/images/temporal_language_analysis.png" alt="Temporal language analysis" style="width: 100%; height: auto;"/>
</div>

We first note that the left-most values in the plot must be interpreted with a grain of salt, as they have **high variance due to a small amount of data** during this time period. 

Therefore, the first important dynamic we can observe is the spike in language feature importance in **August 2016**. This coincides with **allegations and media coverage regarding Russian interference in the election and Trump’s alleged connections to Russia**. In this spike, we can in particular note that the language features of `liwc_friends` and `liwc_negemo` and `liwc_affect` spiked. This suggests that **the non-pro-trump posts generally had a negative view of Trump**, addressing the pro-trump community as a group negatively.

The second important spike occurs in **November/December 2016**. This coincides with the **U.S. presidential election** (November 8, 2016) and its aftermath. We observe that all of the language features shown experience a visible jump. The features `liwc_bio` and `liwc_affect` jump up whereas the rest `liwc_negemo`, `liwc_posemo` go down. The most interesting features to interpret here are: `liwc_affect` going up and its sub-categories `liwc_posemo` and `liwc_negemo` going down. This seems counter-intuitive, but it suggests that people were using affective words that could not be categorized as positive or negative emotions. This can happen when **a community enters a state of "constant hype**", experessing their emotions with high energy, as the pro-trump community probably did. Another feature we can interpret is the spike in `liwc_bio`, which corresponds to the language of biological processes. In this scenario however, it likely reflected a **use of strength an vitality in the posts**, expressing the power of the Trump movement through biological terms (e.g., strength, blood, heart, life).

<div style="font-family: Verdana, Geneva, sans-serif; color: black; max-width: 700px; margin-top: 20px;">

  <div style="font-size: 12px; color: #555; margin-bottom: 6px;">
    <strong>u/BananADA</strong>
  </div>

  <div style="font-size: 14px; line-height: 1.6; padding-left: 10px; border-left: 3px solid #e0e0e0;">
    The spikes line up almost perfectly with major political moments: controversial statements, rallies, protests, and of course the election itself. Hostility wasn’t random, it followed the news cycle like a shadow.
  </div>

</div>

### Are These Communities Actually That Different?

Do targeted communities and pro-Trump communities share characteristics?
Are users similar?
<div style="font-family: Verdana, Geneva, sans-serif; color: black; max-width: 700px; margin-top: 20px;">

  <div style="font-size: 12px; color: #555; margin-bottom: 6px;">
    <strong>u/AnthroGeek</strong>
  </div>

  <div style="font-size: 14px; line-height: 1.6; padding-left: 10px; border-left: 3px solid #e0e0e0;">
    Okay but what about the users? Are Trump supporters and feminists like… from different planets?
  </div>

</div>

<div style="font-family: Verdana, Geneva, sans-serif; color: black; max-width: 700px; margin-top: 20px;">

  <div style="font-size: 12px; color: #555; margin-bottom: 6px;">
    <strong>u/VectorMathFan</strong>
  </div>

  <div style="font-size: 14px; line-height: 1.6; padding-left: 10px; border-left: 3px solid #e0e0e0;">
    Let’s see what the embeddings say. High‑dimensional drama incoming.
  </div><br/><br/>

</div>



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


Three notable exceptions are `r/trump_train`, `r/trumppa` and `r/hottiesfortrump`(outliers), isolated at the top-right of the graph. This separation may indicate that the subreddits focuse on more niche topics and/or exhibit a distinct discussion style compared to the other subreddits in the projection. Further, more targeted analysis would be required to determine whether these subreddits represent a typical statistical outlier or an extreme case of topical or community isolation among smaller Reddit groups.

**Summary**:
- Semantically (_LDA Chart_): These communities are linked to the mainstream. They talk about what everyone else is talking about.
- Structurally (_t-SNE Chart_): They behave like a fortress. While they observe the mainstream topics, they do so from a tightly clustered position at the edge of the ecosystem, rarely mixing freely with the general population despite discussing the same news.

### Do users from pro-Trump subreddits and opposing subreddits share similar characteristics?

To understand how different communities of Reddit users behave and relate to each other, we can analyze user embeddings—vector representations that capture behavioral patterns and similarity between users. Users are represented as an embedding, and we measured similarity between any two users by using cosine similarity, a common metric for comparing high-dimensional vectors. Higher cosine similarity indicates that two users tend to express themselves in more similar ways.

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



<div style="font-family: Verdana, Geneva, sans-serif; color: black; max-width: 700px; margin-top: 20px;">

  <div style="font-size: 12px; color: #555; margin-bottom: 6px;">
    <strong>u/BananADA</strong>
  </div>

  <div style="font-size: 14px; line-height: 1.6; padding-left: 10px; border-left: 3px solid #e0e0e0;">
    Bottom line: the embeddings capture real differences in interests, but everyone’s still pretty diverse, even within their own communities.
  </div>
