# Operationalizing Machine Learning 2023
The scope of the project was to create an end-to-end Machine Learning application on a dataset containing marketing data from costumers of a bank.
In Microsoft Azure a cloud-based production model was trained, deployed and consumed. After an Azure pipeline was created, published and consumed.

## Architectural Diagram

![](imgs/00_architecture.png)


## Key Steps
1. Upload dataset: I uploaded the provided [Bankmarketing dataset](https://automlsamplenotebookdata.blob.core.windows.net/automl-sample-notebook-data/bankmarketing_train.csv) to the Machine Learning workspace.

![](imgs/01_dataset.PNG)

2. I created an Automated ML Experiment with the Machine Learning studio. 

![](/imgs/02_completed_experiment.PNG)

3. I deployed the best model in the Machine learning studio. With the help of the logs.py file I enabled application insigths, and retrieved deployment logs. 

![](/imgs/03_best_model.PNG)

![](/imgs/04_endpoint_insights.PNG)

![](/imgs/05a_logs.PNG)

![](/imgs/05b_logs.PNG)

4. Consumed the deployed model with [swagger](https://swagger.io/blog/api-development/getting-started-with-swagger-i-what-is-swagger/). Called swagger/swagger.sh to run the swagger on the localhost. Than, I ran swagger/serve.py, to be able to see the model endpoint in swagger.

![](/imgs/06_swagger.PNG)

5. Consumed model by API requests. Input was data in dictionary as  JSON. I used the provided endpoint.py (with minor modifications) to interact with the model endpoint. 

![](/imgs/07_endpoint_results.PNG)

I ran benchmarking on this request.

![](/imgs/08a_benchmark.PNG)

![](/imgs/08b_benchmark.PNG)

![](/imgs/08c_benchmark.PNG)

![](/imgs/08d_benchmark.PNG)

6. Created, published and consumed a pipeline with the help of the provided notebook file.

![](/imgs/09_pipeline_created.PNG)

![](/imgs/10_pipeline_endpoint.PNG)

![](/imgs/11_automl_bankmarketing.PNG)

![](/imgs/12_pipeline_endpoint_active.PNG)

![](/imgs/13_run_details.PNG)

![](/imgs/14_job.PNG)

*TODO*: Write a short discription of the key steps. Remeber to include all the screencasts required to demonstrate key steps. 

*TODO* Remeber to provide screenshots of the `RunDetails` widget as well as a screenshot of the best model trained with it's parameters.

## Screen Recording

[Here](https://youtu.be/cZ5N4UeUWI4) you can find a quick overview of the Azure ML studio, showcasing the project.


## Future Suggestions
I have not saved the model before stepping out of the lab. If I exported it with ONNX, it could be used later on as well.
If I use a Parallel Run Step in a pipeline, data processing time could be decreased.
