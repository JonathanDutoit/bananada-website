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

**Improvements from preprocessing pipeline**:

  - Parsed the comma-separated text vector properties into separate columns
  - Extracted `year`, `month`, `day`, `hour` features from `TIMESTAMP`
  - Created combined dataset from titles and bodies and differentiate them by new column called `source_type` which can take as value either 'title' or 'body'

<div class="clearfix vertical-center">
<!-- Left Column: Dataset metrics -->
  <div class="col-6 sm-width-full left pr-3">
    <h3 class="lh-condensed font-smoothing">Reddit User and Subreddit Embeddings</h3>
    <ul class="list-reset mt-2">
      <li><strong>Number of samples:</strong> 10,000</li>
      <li><strong>Number of features:</strong> 25</li>
      <li><strong>Preprocessing improvements:</strong> Normalized, cleaned missing values</li>
      <li><strong>Labels:</strong> 5 categories</li>
    </ul>
  </div>

  <!-- Right Column: Dataset image -->
  <div class="col-6 sm-width-full left pl-3">
    <h3 class="lh-condensed font-smoothing">Preview</h3>
    <img src="{{ site.baseurl }}/assets/images/dataset_preview.png" alt="Dataset preview" class="sm-width-full" />
  </div>
</div>