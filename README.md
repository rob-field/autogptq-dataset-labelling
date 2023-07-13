# autogptq-dataset-labelling
This is an exploratory notebook to show the implementation of automatic dataset emotion labelling using LLMs and autogptq.

Use of a drug review dataset that contains a review and a 1-10 star rating.
Prompt engineering can be used to return an emotion from the following list: {approval, disapproval, anxiety, fear, joy}. The prompt also allows for the star rating to be taken into context (i.e. a rating of 10 is good, a rating of 1 is bad). Additonal prompt modification could be used to return another label (e.g. "Unsure") if the review and rating is contradictory.

This could be implemented to provide labelled datasets for downstream tasks, such as finetuning an emotion detection classifier, especially in domains where extensive labelled data isn't available.

Compute and time complexity are the limiting factors, especially if larger models are used. This notebook uses a 13B parameter model and 100 instances takes ~60s to run (which wouldn't scale well.)
