# Assignment 2: Bias in data
The goal of this assignment is to perform a self-directed exploratory data analysis and identify potential sources of bias in attack data and aggression data from Wikipedia Talk Corpus and describe how such bias could lead to potential unintended negative outcomes using machine learning models.

**Research Question #1**

How does the labelling behavior in the comments change over time?

**Research Question #2**

How does gender affect the labeling behavior in the comments over time?


# Data Sources
The data sources can be downloaded on [Figshare](https://figshare.com/projects/Wikipedia_Talk/16731), per Wikipedia Detox project [access policy](https://foundation.wikimedia.org/wiki/Open_access_policy). 

For each annotated corpora, there are three files:

1. **{attack/aggression}_annotated_comments.tsv**: Raw revisions and derived comments that were labelled by crowdworkers.

2. **{attack/aggression}_annotations.tsv**: Annotations labeled by several crowdworkers for each comment in {attack/aggression}_annotated_comments.tsv.

3. **{attack/aggression}_worker_demographics.tsv**: Basic anonymized demographic information about on the crowdworkers who provided the labels.

For complete information of dataset description and schemas, please visit [here](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release).

# Output Schema
The data output (agg_att_data.csv.csv) combines aggression data, attack data, and worker demographics data. It includes nineteen columns with the definition as follows:

# Notes


# License
Wikimedia Foundation [Term of Use](https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions) and [Privacy Policy](https://foundation.wikimedia.org/wiki/Privacy_policy)
