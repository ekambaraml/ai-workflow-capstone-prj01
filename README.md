# AI Enterprise Workflow Capstone Project


| Filename |Description |
| --- | --- |
| app.py | Application server based on python Flask for model training and predictioning |
| cslib.py | Collection of python functions for transforming the data into features for model training |
| model.py | Functions for Loading model, training model and predictions |
| unittest| Containing api, model and logging tests |
| public | Web portal pages |
| cs-train | Directory containing training data for Model|
| models | pre-trained models |
| notebooks | Solution visualization using jupyter notebooks |
| Dockerfile| Definition file for building docker container|



# Instructions

$ cd ai-enterprise-workflow-capstone

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
 git clone <repository>
 cd ai-enterprise-workflow-capstone
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
    python run-tests.py
    ```

