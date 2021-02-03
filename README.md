# Operationalizing-Machine-Learning
*NOTE:* This file is a template that you can use to create the README for your project. The *TODO* comments below will highlight the information you should be sure to include.


# Operationalizing-Machine-Learning

*TODO:* Write an overview to your project.

## Architectural Diagram
*TODO*: Provide an architectual diagram of the project and give an introduction of each step. An architectural diagram is an image that helps visualize the flow of operations from start to finish. In this case, it has to be related to the completed project, with its various stages that are critical to the overall flow. For example, one stage for managing models could be "using Automated ML to determine the best model". 
![image](https://user-images.githubusercontent.com/59551550/106652856-0e1d7280-65bc-11eb-8508-3384857eee10.png)

## Key Steps
*TODO*: Write a short discription of the key steps. Remeber to include all the screenshots required to demonstrate key steps. 
### Authentication
For the continuous flow of operations, authentication should not require human interaction. Continuous Integration and Delivery system (CI/CD) rely on uninterrupted flows and thus, so that the system doesn't have to wait for a user to manually enter the password, it is good to use authentication with automation.

### Automated ML Experiment
AutoML or Automated ML, is the process of automating the task of machine learning model development. Using this feature, you can predict the best ML model, and it's hyperparameters suited for your problem statement.
For this experiment in Azure ML Studio: We train a model using the on the bank marketing dataset with Automated ML; we create a new compute cluster; and run the AutoML experiment.

### Deploy the best model
After the bike-no.csv dataset has been trained with Automated ML, the deployment of the model happens next. This allows for consuming this model.
After we have completed the AutoML run on the bank marketing dataset, we deploy ht model next. Deploying the model allows us to then consume it. In this exercise, we deploy the model into a production environment using Azure Container Instance (ACI).

### Enable logging
Application Insights is used to detect anomalies, visualize performance etc. It can be enabled before or after a deployment, but for this experiment we enable it after.
In this demo, you learned how to enable Application Insights from a deployed model and then produced logging output with the Python SDK.

### Swagger Documentation
Swagger is a tool that helps build, document, and consume RESTful web services. Through it we get to know what types of HTTP requests that an API can consume(POST, GET).
Azure provides a swagger.json that is used to create a web site that documents the HTTP endpoint for a deployed model. 

In this project, the localhoston port 9000 is used to display the Swagger page. Next we run serve.py so that the contents of swagger.json can be consumed locally by Swagger.

### Consume model endpoints
### Create and publish a pipeline
### Documentation

## Screen Recording
*TODO* Provide a link to a screen recording of the project in action. Remember that the screencast should demonstrate:

## Standout Suggestions
*TODO (Optional):* This is where you can provide information about any standout suggestions that you have attempted.
