## Objective

The final goal of all industrial machine learning (ML) projects is to develop ML products and rapidly bring them into production.

## Principles

### Principle 1 - CI/CD Automation
CI/CD automation provides continuous integration, continuous delivery, and continuous deployment. It carries out the build, test, delivery, and deploy steps. It provides fast feedback to developers regarding the success or failure of certain steps, thus increasing the overall productivity.
Tools: Jenkins, and GitHub Actions
Model Serving Tools: use Docker, and K8s to containerize the ML model and leveraging Flask with and API for serving. Others like KServing of Kubeflow, TensorFlow Serving, AWS SageMaker Endpoints, and Google Vertex AI prediction service

### Principle 2 - Workflor Orchestration
Workflow orchestration coordinates the tasks of an ML workflow pipeline according to directed acyclic graphs (DAGs). DAGs define the task execution order by considering relationships and dependencies.
Tools: Apache Airflow, Kubeflow Pipelines, AWS SageMaker Pipelines, and Azure Pipelines

### Principle 3 - Reproducibility
Reproducibility is the ability to reproduce an ML experiment and obtain the exact same results.

### Principle 4 - Versioning
Versioning ensures the versioning of data, model, and code to enable not only reproducibility, but also traceability (for compliance and auditing reasons).
Source Code Repository Tools: BitBucket, GitHub
Feature Stores Tools (ensures central storage of commonly used online/offline features): Google Feast, Amazon Feature Store
Model Registry (stores trained ML models with their metadata) Tools: AWS SageMaker Model Registry, and Neptune.ai

### Principle 5 - Collaboration
Collaboration ensures the possibility to work collaboratively on data, model, and code. Besides the technical aspect, this principle emphasizes a collaborative and communicative work culture aiming to reduce domain silos between different roles.

### Priniciple 6 - Continous ML Training and Evaluation
Continuous training means periodic retraining of the ML model based on new feature data. Continuous training is enabled through the support of a monitoring component, a feedback loop, and an automated ML workflow pipeline. Continuous training always includes an evaluation run to assess the change in model quality.
Model Training Infrastructure Tools: K8s, and Red Hat OpenShift

### Principle 7 - ML metadata Tracking and Logging
Metadata is tracked and logged for each orchestrated ML workflow task. Metadata tracking and logging is required for each training job iteration (e.g., training date and time, duration, etc.), including the model specific metadata—e.g., used parameters and the resulting performance metrics, model lineage: data and code used—to ensure the full traceability of experiment runs.
ML Metadata Stores Tools: Kubeflow Pipelines, AWS SageMaker Pipelines

### Principle 8 - Continous Monitoring 
Continuous monitoring implies the periodic assessment of data, model, code, infrastructure resources, and model serving performance (e.g., prediction accuracy) to detect potential errors or changes that influence the product quality.
Tools: Prometheus with Grafana, ELK, TensorBoard

### Principle 9 - Feedback Loops
Multiple feedback loops are required to integrate insights from the quality assessment step into the development or engineering process (e.g., a feedback loop from the experimental model engineering stage to the previous feature engineering stage). Another feedback loop is required from the monitoring component (e.g., observing the model serving performance) to the scheduler to enable the retraining.

![image](https://user-images.githubusercontent.com/37369603/224610976-fdd9ce5f-007c-447a-aee4-553250ee9f07.png)

## Architecture

It is an end-to-end process, from MLOps project initiation to the model serving. 
It includes: 
* the MLOps project initiation steps
* the feature engineering pipeline, including the data ingestion to the feature store
* the experimentation
* the automated ML workflow pipeline up to the model serving

![image](https://user-images.githubusercontent.com/37369603/224613734-30bccf15-1749-470d-abd2-8b54c9986943.png)

## Challenges for Adopting MLOps

* To successfully develop and run ML products, there needs to be a culture shift away from model-driven ML toward a product-oriented discipline
* ML system challenges - designing for fluctuating demand which makes it difficult to estimate infrastructure resources like CPU/GPU, RAM, ...
* Operational challenges - In productive settings, it is challenging to operate ML manually due to different stacks of software and hardware components and their interplay. Therefore, robust automation is required

Reference - https://arxiv.org/abs/2205.02302


