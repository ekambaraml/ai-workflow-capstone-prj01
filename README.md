# AI Enterprise Workflow Capstone Project


## Checklist
- [ ] Are there unit tests for the API?

- [ ] Are there unit tests for the model?

- [ ] Are there unit tests for the logging?

- [ ] Can all of the unit tests be run with a single script and do all of the unit tests pass? 

- [ ] Is there a mechanism to monitor performance? 

- [ ] Was there an attempt to isolate the read/write unit tests from production models and logs? 

- [ ] Does the API work as expected? For example, can you get predictions for a specific country as well as for all countries combined? 

- [ ] Does the data ingestion exists as a function or script to facilitate automation? 

- [ ] Were multiple models compared? 

- [ ] Did the EDA investigation use visualizations? 

- [ ] Is everything containerized within a working Docker image? 

- [ ] Did they use a visualization to compare their model to the baseline model? 




## Project Content

| Filename |Description |
| --- | --- |
| app.py | Application server based on python Flask for model training and predictioning |
| cslib.py | Collection of python functions for transforming the data into features for model training |
| model.py | Functions for Loading model, training model and predictions |
| unittest| Containing api, model and logging tests |
| public | Web portal pages |
| cs-train | Directory containing training data for Model|
| models | pre-trained models |
| notebooks/eda-analysis.ipynb | Solution visualization using jupyter notebooks |
| notebooks/performance-monitoring.ipynb | Performance monitoring notebook |
| Dockerfile| Definition file for building docker container|



# Instructions

$ cd ai-workflow-capstone-prj01

* To test `app.py`
    ```bash
    python app.py
    ```

* Accessing the Website
  Go to http://0.0.0.0:8080/ 
  
    
* To test the model directly and train the model see the code at the bottom of `model.py`
    ```bash
    python ModelTets.py
    ```


## How to build the model docker container

```
 git clone https://github.com/ekambaraml/ai-workflow-capstone-prj01
 cd ai-workflow-capstone-prj01
 docker build -t ai-workflow .
```

* List the newly built docker container images with the model.
    ```
    docker images
    ```
* Run the model container in background mode
    ```
    docker run -p 8080:8080 -d ai-workflow
    ```

* How to access the model portal
    Go to http://0.0.0.0:8080


## Testing the Model
Before running the unit tests launch the `app.py`.

* Run the application locally on a separate terminal
  ```
  python app.py
  ```

* To run only the api tests
    ```
    python unittests/ApiTests.py
    ```

* To run only the model tests
    ```
    python unittests/ModelTests.py
    ```

* To run all of the tests
    ```
    python run-api-model-logging-tests.py
    ```

