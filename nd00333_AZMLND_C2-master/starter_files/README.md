# Operationalizing Machine Learning

## OVERVIEW

MLO's aspects have been explored in this project. Project contains three parts: Deploying the best model run by AutoML, consuming through the end points, and automating the process by creating a pipleine from creating the dataset to deploying model and scoring using that model by consuming the endpoint of deployed model.

Deploying the best model: AutoML run has been set up for given bank-marketing dataset for classification task type. Best model has been identified with highest accuracy as VotingEnsemble. This model was deployed using the Azure ML UI using ACI container and enabling Authentication. Logging is enabled which helps in figuring out problems during deployment and consumption process. Application Insights are turned on for this purpose and best model is deployed successfully in 'Healthy' state providing all the endpoint details.

Second part is swagger documentation, Azure ML produces JSON file for deployed model, which can be found in Endpoint section. Swagger is a tool that helps build, document, and consume RESTful web services like the ones you are deploying in Azure ML Studio. JSON file is used to create a web site that documents the HTTP endpoint for a deployed model. Contents of the API for the model are displayed in the localhost website, and different HTTP requests are visible that are supported for the specified model. You can consume a deployed service via an HTTP API. An HTTP API is a URL that is exposed over the network so that interaction with a trained model can happen via HTTP requests. A benchmark is used to create a baseline or acceptable performance measure. Benchmarking HTTP APIs is used to find the average response time for a deployed model.

Last part of the project is to create, publish and consume the Pipeline. The above mentioned process is automed using Pipeline section in Azure using Python SDK. Using a jupyter notebook, an AutoML run was initiated, best model was obtained, endpoint was created and the new data was scored using the model endpoint. A REST endpoint of the Pipeline was created. The entire process was repeated by passing the dataset through this endpoint.


## Architectural Diagram

![0  Architectural_diagram](https://user-images.githubusercontent.com/76555474/114868256-573b3f80-9e13-11eb-8f16-b89f99aeb67a.png)

## KEY STEPS

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


### Create, publish and consume Pipeline 
1. Pipeline is been created in Azure ML studio
![15  Pipeline_created](https://user-images.githubusercontent.com/76555474/114881348-8ad09680-9e20-11eb-8bf6-ed0f008318c8.png)

2. Bank marketing dataset in Azure ML studio
![16  Bankmarketing_dataset](https://user-images.githubusercontent.com/76555474/114881645-d125f580-9e20-11eb-8076-33f32b323212.png)

3. Published Pipeline overview
![17  Pipeline_overview](https://user-images.githubusercontent.com/76555474/114881723-e26f0200-9e20-11eb-92b7-0d01d65c343b.png)

4. Pipeline end point created and Active
![19  Pipeline_endpoint_active](https://user-images.githubusercontent.com/76555474/114881997-1e09cc00-9e21-11eb-8504-1c103a71d20e.png)

5. Configuring Pipeline with Python SDK and showing RunDetails widget from notebook
![20  RunDetails_widget](https://user-images.githubusercontent.com/76555474/114882272-6b863900-9e21-11eb-97b9-64e82a9d3d22.png)
![21  Scheduled_run_completed](https://user-images.githubusercontent.com/76555474/114882287-6de89300-9e21-11eb-83db-13d512f9ca30.png)

6. Endpoints from publish Pipelines in Azure ML studio
![22  Published_endpoints](https://user-images.githubusercontent.com/76555474/114882572-b4d68880-9e21-11eb-82c9-f4264f63519f.png)


## Screen Recording


## Standout Suggestions

1. Deep learning models can be included
2. Different types of datasets can be included for consuming the endpoints
3. 
