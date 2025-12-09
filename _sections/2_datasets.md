---
title: DATASET
anchor: dataset
layout: page
---

## Datasets

<div class="clearfix">
  <h3 class="lh-condensed font-smoothing">Reddit Hyperlink Network</h3>
</div>
  The subreddit-to-subreddit hyperlink network is extracted from the posts that create hyperlinks from one subreddit to another. We say a hyperlink originates from a post in the source community and links to a post in the target community. Note that each post has a title and a body. The hyperlink can be present in either the title of the post or in the body. (source: [<u>Reddit Hyperlink Network</u>](https://snap.stanford.edu/data/soc-RedditHyperlinks.html))
<!-- Left Column: Dataset metrics -->
<div class="clearfix vertical-center">
  <div class="col-6 sm-width-full left pr-3">
    <div class="clearfix prose py-2" markdown="1">

  | Dataset Statistics                        | Value             |
  |:----------------------------------------- |:-----------------|
  | Number of nodes (subreddits)              | 55,863            |
  | Number of edges (hyperlink between subs)  | 858,490           |
  | Edge weights (label of hyperlink)         | -1 or +1          |
  | Edge attributes                           | Text property vectors | 
  | Timespan                                  | Jan 2014 - April 2017 |

  </div>
  </div>

  <!-- Right Column: Dataset image -->
  <div class="col-6 sm-width-full left pl-3">
    <img src="{{ site.baseurl }}/assets/images/reddit_hyperlink_network.png" alt="Dataset preview" style="max-width: 500px; width: 100%; height: auto;"/>
  </div>
</div>

- **Improvements from preprocessing pipeline**:

  - Parsed the comma-separated text vector properties into separate columns
  - Extracted `year`, `month`, `day`, `hour` features from `TIMESTAMP`
  - Created combined dataset from titles and bodies and differentiate them by new column called `source_type` which can take as value either 'title' or 'body'

<div class="clearfix">
  <h3 class="lh-condensed font-smoothing">Reddit User and Subreddit Embeddings</h3>
</div>
  **User embeddings**: Contains one numerical vector in low dimensional space (a.k.a. embeddings) for each user. The embeddings are 300 dimensions each. Two user embeddings are similar if they who post in similar subreddits.

  **Subreddit embeddings**: Contains one numerical vector in low dimensional space (a.k.a. embeddings) for each subreddit. The embeddings are 300 dimensions each. Two subreddit embeddings are similar if the users who post in them are similar.

  source: [<u>Reddit User and Subreddit Embeddings</u>](https://snap.stanford.edu/data/web-RedditEmbeddings.html)
<!-- Left Column: Dataset metrics -->
<div class="clearfix vertical-center">
  <div class="col-6 sm-width-full left pr-3">
    <div class="clearfix prose py-2" markdown="1">

  | Dataset Statistics                        | Value             |
  |:----------------------------------------- |:----------------- |
  | Number of users                           | 118,381           |
  | Number of subreddits                      | 51,278            |
  | Embedding length                          | 300               |
  | Timespan                                  | Jan 2014 - April 2017 |

  </div>
  </div>

  <!-- Right Column: Dataset image -->
  <div class="col-6 sm-width-full left pl-3">
    <img src="{{ site.baseurl }}/assets/images/embeddings_clustering.png" alt="Dataset preview" style="max-width: 500px; width: 100%; height: auto;"/>
  </div>
</div>

- **Improvements from preprocessing pipeline**:

  - Added column headers
  - Replaced 300 embeddings features columns for a new  single column called `VECTOR` which is a `numpy` array contained all the embedding features