---
title: "Automated Training and Redeployment"

draft: false
---

### AI Pipeline

The main objective of the AI Pipeline is to make the training process more effectient and automated. This is done to reduce the amount of human intervention needed in training the AI model. As well as to enable frequent retraining and redeploying of the model that serves the Angaza Platform.
Fo

You can use ML pipelines to:

* Apply MLOps strategies to automate repeatable processes.
* Experiment by running an ML workflow with different sets of hyperparameters, number of training steps or iterations, etc.
* Reuse a pipeline's workflow to train a new model.


## Tools used

* [Django Rest Framework](https://www.django-rest-framework.org/)
* [MLOps](https://cloud.google.com/ai-platform/pipelines/docs/introduction)
* [Kubeflow](https://www.kubeflow.org/)


The ML process used is based on the following 
![ML workflow](https://cloud.google.com/ai-hub/docs/images/kubeflow-pipeline.svg)



The preprocess step Prepares the training data

The train step uses the preprocessed data to train the model

The confusion Matrix uses the output the prediction task to buiild a confusion matrix


## Event-triggered Pipeline calls

In order to automatically trigger the pipeline calls a google service Cloud Functions is used. New data has to be added to the GCS(Google Cloud Storage) bucket.

To connect to an AI Platform Pipelines cluster, you’ll first need to find the URL of its endpoint.


The following snippet is used to automatically run the pipeline.

```
    import kfp
    def get_access_token():
        url = 'http://metadata.google.internal/computeMetadata/v1/instance/service-accounts/default/token'
        r = requests.get(url, headers={'Metadata-Flavor': 'Google'})
        r.raise_for_status()
        access_token = r.json()['access_token']
        return access_token

    token = get_access_token() 
    client = kfp.Client(host=HOST_URL, existing_token=token)

    res = client.run_pipeline(...)
```

