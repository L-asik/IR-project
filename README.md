# IR-project
## Project developed by Mateusz Małecki, Mateusz Zieleziński and Antoni Lasik during the Erasmus+ exchange at FCT NOVA School of Science and Technology within the course Information Retrieval
In this project, we were deriving from the set of medical documents, patient cases that were our queries, and a set of pairs (document, query) with labeled relevance. 


The first phase was focused on introducing the ideas of the vector space model and the model with Jelineck-Mercer smoothing, different metrics, and evaluation. We had to develop a ranking function and based on the provided metrics evaluate the obtained ranks. Later we had to compare the rankings based on these two models. In this phase, we were using only the titles of medical documents, as a sort of baseline for further experiments. 

In the second phase, we were using all of the medical documents fields, with the handling of the missing values. We used the previously developed models to calculate the similarity measures between each document, and query pair and then used logistic regression(with different regularisation parameters) to calculate the importance weights for each field in each model. This is how we have obtained the third model-LETOR(Learning to rank). Basing on these weights we could evaluate this LETOR model and introduce the third ranking function and compare them with previous ones. 


In the third phase we were introduced to the pertained BERT model, contextual embeddings, and tokenizers, we had to play around a bit and analyze how the embedding layers and tokenizer behave. Then we had to extract the CLS-token embeddings for the next sentence prediction task, where our pairs of sentences were a detailed description field of a medical document and a patient case. We have failed to evaluate this approach because of the hidden bug in our implementation and the overwhelming amount of computational power needed to do this for this size of the dataset. 

The whole project is described in detail in the report.
