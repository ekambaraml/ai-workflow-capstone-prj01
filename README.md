# AI Enterprise Workflow Capstone Project
### This project uses time series to forecast revenue prediction for the next 30 days.

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
    python model.py
    ```

## How to build the model docker container

```
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

