# Serverless-Question-Answering-API
Serverless BERT with Huggingface and AWS Lambda, Quantum Computing with AWS Braket - Tutorial

## Problem Statement

![image](https://user-images.githubusercontent.com/13203059/161676624-6f614b63-bb67-4ee0-b6e4-f169dbef1ca2.png)

## Architecture

![image](https://user-images.githubusercontent.com/13203059/161676732-d32d20ef-8ce0-428a-b941-8291b104d0b6.png)

# Deployed Elastic Container Registry image

![image](https://user-images.githubusercontent.com/13203059/162638435-779f49b0-18e5-4428-8143-5729fba8c5b9.png)

# Delployed AWS Lambda function with a custom docker image & serverless deploy

![image](https://user-images.githubusercontent.com/13203059/162638376-4214b02b-04a6-48cf-a84a-e805d9847c95.png)

# Test the deployed Q&A API

We test the API using AWS API gateway REST client. The first run of the API is the cold start and you will get server error because the model is getting loaded and initialized. But on subsequent API calls it wil run as expected.

```
Request Body -

{
  "context": "We introduce a new language representation model called BERT, which stands for idirectional Encoder Representations from Transformers. Unlike recent language epresentation models (Peters et al., 2018a; Radford et al., 2018), BERT is designed to pretrain deep bidirectional representations from unlabeled text by jointly conditioning on both left and right context in all layers. As a result, the pre-trained BERT model can be finetuned with just one additional output layer to create state-of-the-art models for a wide range of tasks, such as question answering and language inference, without substantial taskspecific architecture modifications. BERT is conceptually simple and empirically powerful. It obtains new state-of-the-art results on eleven natural language processing tasks, including pushing the GLUE score to 80.5% (7.7% point absolute improvement), MultiNLI accuracy to 86.7% (4.6% absolute improvement), SQuAD v1.1 question answering Test F1 to 93.2 (1.5 point absolute improvement) and SQuAD v2.0 Test F1 to 83.1 (5.1 point absolute improvement).",
  "question": "What is BERTs best score on Squadv2 ?"
}
```

![image](https://user-images.githubusercontent.com/13203059/162638533-dd822120-9c9c-4b25-a672-1cec73c23572.png)



