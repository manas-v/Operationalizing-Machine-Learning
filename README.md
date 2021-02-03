# Operationalizing-Machine-Learning
# Overview
This project is part of the Udacity Azure ML Nanodegree.
In this project, we will work with the Bank Marketing dataset. We will use Azure Machine Learning Studio to configure a cloud-based machine learning production model, deploy it, and consume it. We will also create, publish, and consume a pipeline.

## Dataset
The data is related to the direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be ('yes') or not ('no') subscribed. i.e. The classification goal is to predict if the client will subscribe (yes/no) to a term deposit (variable y).

![image](https://user-images.githubusercontent.com/59551550/106787649-fc000a80-6675-11eb-9689-815e71811c10.png)

## Architectural Diagram
*TODO*: Provide an architectual diagram of the project and give an introduction of each step. An architectural diagram is an image that helps visualize the flow of operations from start to finish. In this case, it has to be related to the completed project, with its various stages that are critical to the overall flow. For example, one stage for managing models could be "using Automated ML to determine the best model". 
![image](https://user-images.githubusercontent.com/59551550/106652856-0e1d7280-65bc-11eb-8508-3384857eee10.png)

## Key Steps
We have used the following steps in the project

### 1. Authentication
For the continuous flow of operations, authentication should not require human interaction. Continuous Integration and Delivery system (CI/CD) rely on uninterrupted flows and thus, so that the system doesn't have to wait for a user to manually enter the password, it is good to use authentication with automation.

### 2. Automated ML Experiment
AutoML or Automated ML, is the process of automating the task of machine learning model development. Using this feature, you can predict the best ML model, and it's hyperparameters suited for your problem statement.
For this experiment in Azure ML Studio: We train a model using the on the bank marketing dataset with Automated ML; we create a new compute cluster; and run the AutoML experiment.

### 3. Deploy the best model
After the bike-no.csv dataset has been trained with Automated ML, the deployment of the model happens next. This allows for consuming this model.
After we have completed the AutoML run on the bank marketing dataset, we deploy ht model next. Deploying the model allows us to then consume it. In this exercise, we deploy the model into a production environment using Azure Container Instance (ACI).

### 4. Enable logging
Application Insights is used to detect anomalies, visualize performance etc. It can be enabled before or after a deployment, but for this experiment we enable it after.
In this demo, you learned how to enable Application Insights from a deployed model and then produced logging output with the Python SDK.

### 5. Swagger Documentation
Swagger is a tool that helps build, document, and consume RESTful web services. Through it we get to know what types of HTTP requests that an API can consume(POST, GET).
Azure provides a swagger.json that is used to create a web site that documents the HTTP endpoint for a deployed model. 

In this project, the localhoston port 9000 is used to display the Swagger page. Next we run serve.py so that the contents of swagger.json can be consumed locally by Swagger.

### 6. Consume model endpoints
Consumption of a deployed service is done via an HTTP API(URL that is exposed over the network so that interaction with a trained model can happen via HTTP requests). If there is any issue in the deployed model, consuming the data from the service would allow identifying problems. It is also a great way to validate (test) outputs are working as expected.
The APIs exposed by Azure ML will use JSON (JavaScript Object Notation) to accept data and submit responses. It served as a bridge language among different environments.
To interact with the model endpoint, the the full URL to the endpoint and the key to authenticate should be provided in the endpoint.py script.

### 7. Benchmark the Endpoint
A benchmark is used to create a baseline or acceptable performance measure. Benchmarking HTTP APIs is used to find the average response time for a deployed model.
The benchmark.sh script includes the ab command that runs against the endpoint using the data.json file created by the endpoint.py file run previously. After running the benchmark.sh an output of requests sent to and responses from the endpoint are recieved, with this we also have a summary with key information to determine response performance.

### 8. Create and publish a pipeline
**Part 1: Create a pipeline with AutoML steps**
A machine learning pipeline is a meant for automating the machine learning workflow. In this porject we will use the Python SDK to create a pipeline with AutoML steps.

**Part 2: Publish the pipeline**
Publishing a pipeline is the process of making a pipeline publicly available., In this part we will publish the created pipeline using a combination of Azure ML studio and the Python SDK.

**Part 3: Consume the pipeline**
In this section we will consume a pipeline using the Azure Python SDK by sending a post request to the endpoint. The post request will trigger the pipeline and schedule an Automated ML experiment.

## Screen Recording
*TODO* Provide a link to a screen recording of the project in action. Remember that the screencast should demonstrate:

## Standout Suggestions
*TODO (Optional):* This is where you can provide information about any standout suggestions that you have attempted.
