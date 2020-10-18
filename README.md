# Assignment 2: Bias in data

The annotated datasets from Wikipedia Talk Corpus are used to train machine learning models as part of a project called Conversation AI. The trained models can be accessed through [Perspective API](https://github.com/conversationai/perspectiveapi/blob/master/2-api/methods.md)

The goal of this assignment is to perform a self-directed exploratory data analysis and identify potential sources of bias in attack data and aggression data  and describe how such bias could lead to potential unintended negative outcomes using machine learning models.

**Research Question #1**

How does the labelling behavior in the comments change over time?

![alt text](https://github.com/jeffrey25706660/data512-a2/blob/main/graphs/Average%20Aggression%20%26%20Attack%20Score%20by%20time.jpg)

**Research Question #2**

How does gender affect the labeling behavior in the comments over time?

![alt text](https://github.com/jeffrey25706660/data512-a2/blob/main/graphs/attack%20%26%20aggresion%20score%20by%20gender.png)
![alt text](https://github.com/jeffrey25706660/data512-a2/blob/main/graphs/Average%20Aggression%20Score%20by%20Gender.jpg?raw=true)
![alt text](https://github.com/jeffrey25706660/data512-a2/blob/main/graphs/Average%20Attack%20Score%20by%20Gender.jpg)

# Data Sources

The data sources can be downloaded on [Figshare](https://figshare.com/projects/Wikipedia_Talk/16731), per Wikipedia Detox project [access policy](https://foundation.wikimedia.org/wiki/Open_access_policy). 

For this assignment, we choose Personal Attacks and Aggression data for analysis. 

For each annotated corpora, there are three files:

1. **{attack/aggression}_annotated_comments.tsv**: Raw revisions and derived comments that were labelled by crowdworkers.

2. **{attack/aggression}_annotations.tsv**: Annotations labeled by several crowdworkers for each comment in {attack/aggression}_annotated_comments.tsv.

3. **{attack/aggression}_worker_demographics.tsv**: Basic anonymized demographic information about on the crowdworkers who provided the labels.

For complete information of dataset description and schemas, please visit [here](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release).

# Output Schema
The data output (agg_att_data.rar) combines aggression, attack, and worker demographic data. It includes nineteen columns with the definition as follows:
Column | Description | 
--- | --- |
rev_id |MediaWiki revision id of the edit that added the comment to a talk page  | 
comment | Comment text | 
year | The year the comment was posted in | 
logged_in | Indicator for whether the user who made the comment was logged in. Takes on values in {0, 1} | 
ns | Namespace of the discussion page the comment was made in. Takes on values in {user, article} | 
sample| Indicates whether the comment came via random sampling of all comments. Takes on values in {random, blocked}|
split| Takes on values in {train, dev, test}|
worker_id| Crowd-worker id.|
gender| Takes a value in {'male', 'female', and 'other'}.|
english_first_language| Does the crowd-worker describe English as their first language. Takes a value in {0, 1}.|
age_group| The age group of the crowd-worker.|
education|Takes on values in {'none', 'some', 'hs', 'bachelors', 'masters', 'doctorate', 'professional'}.|
worker_id| Anonymized crowd-worker id.|
aggression_score| Categorical variable ranging from very aggressive (-2), to neutral (0), to very friendly (2).|
aggression| Indicator variable for whether the worker thought the comment has an aggressive tone.| 
quoting_attack| Indicator for whether the worker thought the comment is quoting or reporting a personal attack that originated in a different comment.|
recipient_attack| Indicator for whether the worker thought the comment contains a personal attack directed at the recipient of the comment.|
third_party_attack| Indicator for whether the worker thought the comment contains a personal attack directed at a third party.|
other_attack| Indicator for whether the worker thought the comment contains a personal attack but is not quoting attack, a recipient attack or third party attack.|
attack| The annotation takes on value 0 if the worker selected the option "This is not an attack or harassment" and value 1 otherwise.|

For complete information of attribute description, please visit [here](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release)

# License
Wikimedia Foundation [License](https://wiki.creativecommons.org/wiki/CC0)
