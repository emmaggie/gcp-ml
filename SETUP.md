# Setup for GCP ML

## General GCP Account Setup

The following are general setup steps:
- **CREATE** a new gmail account for testing
    - **SIGN IN** to Chrome with this account
    
- **CREATE** a new GCP account using a gmail address
    - **LOGIN** to the GCP console with your gmail address
    - **CREATE** a billing account (required credit card)
    - **USE** 'new account' $ 300 credit

- **CREATE** a new GCP Project
    - **ASSOCIATE** a billing account with this GCP project
    - **SETUP** a billing alert for that project with a notification via pub/sub
    - (Optional) **CREATE** a non-owner IAM admin user to reduce the attack surface
    
---

## Code & Code Editor

You can use the editor and language of your choice.  I am using VSCode and Python on a MacOS.
- Verify Python - I am using Python 2.7
- Install VSCode - do not need to install Git
    - install these extentions for VSCode: 
        - TensorFlowSnippets
        - BigQuery highlight syntax
        - material theme icons
        - Python
        - VS Code Jupyter Notebook viewer

## GCP SDK 
 
 You can use the included console in GCP to run GCP SDK (gcloud) commands or you can download and install the GCP SDK locally

 - Download,unzip, install and authenticate to GCP SDK
 - Verify with `gcloud auth list` or `gcloud config list`

 ## Enable APIs

 You will be using a number of GCP services.  Some services are enabled by default, however, for other services you will need explicitly enable API or service.  

TIP: Verify that you using the intended GCP Project before you enable a service:

GCP Services enabled by default:
 - GCS, GCE, BigQuery, Kubernetes  

 Must be explicitly enabled:
 - Vision API, Video API, Natural Language API, Speech API, Translation API, Dialogflow
 - Cloud Machine Learning Engine
 - Cloud TPU
 - MLKit (for Firebase - TensorFlow Lite on mobile device)
 - Cloud Repositories (if using some of GCP-supplied code samples)
 
 ## GCP AI Hub
  - AI Hub - https://aihub.cloud.google.com/u/0/ (see screen shot below)
  - Resources in the AI Hub include the following:
    - sample training data
    - trained ML models & technical guides
    - compute templates - kubeflow pipelines, ML continers, Jupyter notebooks, ML services, TF models and VM images
    
![AI Hub](https://github.com/lynnlangit/gcp-ml/blob/master/images/ai-hub-main.png)
