# Hivemind's Infrastructure Challenge

The challenge consists in developing a simple microservice (or function/lambda) and deploying the resulting architecture in the cloud (e.g. AWS).

## Story

The team is tasked with the development of a simple web ui for sentiment analysis of tweets. The user shall be able to enter a tweet and the ui will return a thumbs up or down depending on the result of the sentiment analysis. 

Your team has already defined an architecture consisting of a single-page-app ui, a backend http api and a sentiment analysis service. The sentiment analysis service is an internal service so it shouldn't be made public. Instead, the ui should talk via a backend http-api which then calls the sentiment analysis service.

## Task

The ui and the sentiment analysis service have already been developed in the previous sprint and are thus ready to use. You are tasked with the development of the backend http api that serves the ui and calls the sentiment analysis. The team leaves it up to you to choose the programming language for this task, but since they are big functional programming geeks, they recommend you to use a functional programming language.

Upon completion, you are asked to deploy the infrastructure in the cloud using infrastructure as code (IaC). The usage of the cloud provider & programming language is up to you, but if you don't know what to use a good choice is AWS and CDK.

## Services

* [tweet ui](./tweet-ui/README.md)
* [sentiment analysis](./sentiment-analysis/README.md)

## Resources

- [AWS Cloud Development Kit](https://aws.amazon.com/cdk/)
- [Terraform](https://www.terraform.io/)
