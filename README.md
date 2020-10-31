# Exploring Gender Biases in Information Retrieval Relevance Judgement Datasets
This repository contains the code and resources for detecting the gender of queries (Female, Male, Neutral) along with the psychological characteristic of MS MARCO queries. 

First, to fine-tune BERT, we used some of the MS MARCO Dev set queries that have been labeled by Navid Rekabsaz (the queries can be found here) along with some gender specific terms (available in resources folder). Subsequently, we used the fine-tuned BERT model to classify the gender of other MS MARCO Dev set queries that had at least one related human-judged relevance judgement document, which consisted of 51,827 queries. In total, we ended up with 48,200 neutral queries, 2,222 male queries, and 1,405 female queries. To have a balanced setup, we retained all 1,405 female queries and randomly selected 1,405 male and 1,405 neutral queries from the other two classes (queries are available in Identified Gendered Queries folder). We utilized 1,405 queries in each class and their associated relevance judgement documents to investigate the presence of stereotypical gender biases. Finally, to extract the psychological characteristics of the queries in each group, we used Linguistic Inquiry and Word Count (LIWC) text analytics toolkit, a program that calculates the degree to which a text contains psychological words.
## Code:
- codes/train.py: The code for fine-tuning BERT on the [gender-annotated dataset](https://github.com/navid-rekabsaz/GenderBias_IR/blob/master/resources/queries_gender_annotated.csv).
- codes/predict.py: You can use this code to identify the gender of the queries by the fine-tuned model.
## Trained Model:
You can also use the fine-tuned BERT model for query gender identification task [here](https://drive.google.com/file/d/1_YTRs4v5DVUGUffnRHS_3Yk4qteJKO6w/view?usp=sharing).
## Results:
Psychological characteristics for queries of each group can be found in Quantifying Psychological Characteristics folder.
