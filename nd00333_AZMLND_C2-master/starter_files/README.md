# Operationalizing Machine Learning

## Overview

MLO's aspects have been explored in this project. Project contains three parts: Deploying the best model run by AutoML, consuming through the end points, and automating the process by creating a pipleine from creating the dataset to deploying model and scoring using that model by consuming the endpoint of deployed model.

Deploying the best model: AutoML run has been set up for given bank-marketing dataset for classification task type. Best model has been identified with highest accuracy as VotingEnsemble. This model was deployed using the Azure ML UI using ACI container and enabling Authentication. Logging is enabled which helps in figuring out problems during deployment and consumption process. Application Insights are turned on for this purpose and best model is deployed successfully in 'Healthy' state providing all the endpoint details.

Second part is swagger 


## Architectural Diagram

![0  Architectural_diagram](https://user-images.githubusercontent.com/76555474/114868256-573b3f80-9e13-11eb-8f16-b89f99aeb67a.png)



## Key Steps

### Deploy the model
1. Dataset is created in the ML studio
![1  Dataset_loaded](https://user-images.githubusercontent.com/76555474/114868277-5bfff380-9e13-11eb-88b9-38eed1659b1a.png)

2. AutoMl experiment is set up for classification task type and completed
![2  AutoMLrun_completed](https://user-images.githubusercontent.com/76555474/114868606-bac56d00-9e13-11eb-91ba-83749256d7af.png)

3. Best model is produced as the experiment is completed
![3  Best_model](https://user-images.githubusercontent.com/76555474/114868657-c9ac1f80-9e13-11eb-8bd2-169ea0a28c88.png)

4. Model is deployed with enabling Authentication and using ACI
![4  Deploying_bestmodel](https://user-images.githubusercontent.com/76555474/114868702-d761a500-9e13-11eb-9e82-a925e42c5fb8.png)

5. Logging enabled in logs.py script
![5  Logging_enabled](https://user-images.githubusercontent.com/76555474/114868820-f5c7a080-9e13-11eb-96b0-3cae8b6855b4.png)

6. Output by running logs.py script
![6  Logging_running](https://user-images.githubusercontent.com/76555474/114868916-1132ab80-9e14-11eb-927a-05d075a2a890.png)

7. API insights and enabled and best model deployed 'Healthy'
![7  API_insights_enabled](https://user-images.githubusercontent.com/76555474/114869053-30c9d400-9e14-11eb-9c2d-b1036dc134de.png)


### Consume the endpoints
1. Swagger.sh script is excuted 
![8  Swagger_bash_running](https://user-images.githubusercontent.com/76555474/114869299-72f31580-9e14-11eb-9297-fafe2b3b1fe8.png)

2. Swagger runs on localhost
![9  Localhost_running](https://user-images.githubusercontent.com/76555474/114869705-ec8b0380-9e14-11eb-9161-4f69d2e5ee1f.png)

3. REST endpoint scoring URI and primary key
![10  Consuming_endpoints](https://user-images.githubusercontent.com/76555474/114869982-412e7e80-9e15-11eb-8e04-2d316e1dc76f.png)

4. Updating REST endpoint URI and primary key in endpoint.py script
![11  Updating_scoringURI_primarykey](https://user-images.githubusercontent.com/76555474/114870304-a08c8e80-9e15-11eb-8cec-47312196f262.png)

5. Consuming Model endpoints by running endpoint.py script
![12  Endpoint_Script_output ](https://user-images.githubusercontent.com/76555474/114870452-d2055a00-9e15-11eb-899f-2c1620446445.png)

6. Modifying benchmark.sh with scoring URI and primary key
![13  Modifying_benchmark](https://user-images.githubusercontent.com/76555474/114870726-227cb780-9e16-11eb-8f57-f0fdfcc4efc2.png)

7. data.json produced and benchmark.sh script executing
![14  Benchmark_output](https://user-images.githubusercontent.com/76555474/114871052-80110400-9e16-11eb-9319-c12f937858bd.png)





*TODO*: Write a short discription of the key steps. Remeber to include all the screenshots required to demonstrate key steps. 

## Screen Recording
*TODO* Provide a link to a screen recording of the project in action. Remember that the screencast should demonstrate:

## Standout Suggestions
*TODO (Optional):* This is where you can provide information about any standout suggestions that you have attempted.
