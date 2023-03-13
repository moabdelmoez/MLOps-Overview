## Objective

The final goal of all industrial machine learning (ML) projects is to develop ML products and rapidly bring them into production.

## Principles

### Principle 1 - CI/CD Automation
CI/CD automation provides continuous integration, continuous delivery, and continuous deployment. It carries out the build, test, delivery, and deploy steps. It provides fast feedback to developers regarding the success or failure of certain steps, thus increasing the overall productivity.

### Principle 2 - Workflor Orchestration
Workflow orchestration coordinates the tasks of an ML workflow pipeline according to directed acyclic graphs (DAGs). DAGs define the task execution order by considering relationships and dependencies.

### Principle 3 - Reproducibility
Reproducibility is the ability to reproduce an ML experiment and obtain the exact same results.

### Principle 4 - Versioning
Versioning ensures the versioning of data, model, and code to enable not only reproducibility, but also traceability (for compliance and auditing reasons).

### Principle 5 - Collaboration
Collaboration ensures the possibility to work collaboratively on data, model, and code. Besides the technical aspect, this principle emphasizes a collaborative and communicative work culture aiming to reduce domain silos between different roles.

### Priniciple 6 - Continous ML Training and Evaluation
Continuous training means periodic retraining of the ML model based on new feature data. Continuous training is enabled through the support of a monitoring component, a feedback loop, and an automated ML workflow pipeline. Continuous training always includes an evaluation run to assess the change in model quality.

### Principle 7 - ML metadata Tracking and Logging
Metadata is tracked and logged for each orchestrated ML workflow task. Metadata tracking and logging is required for each training job iteration (e.g., training date and time, duration, etc.), including the model specific metadata—e.g., used parameters and the resulting performance metrics, model lineage: data and code used—to ensure the full traceability of experiment runs.

### Principle 8 - Continous Monitoring 
Continuous monitoring implies the periodic assessment of data, model, code, infrastructure resources, and model serving performance (e.g., prediction accuracy) to detect potential errors or changes that influence the product quality.

### Principle 9 - Feedback Loops
Multiple feedback loops are required to integrate insights from the quality assessment step into the development or engineering process (e.g., a feedback loop from the experimental model engineering stage to the previous feature engineering stage). Another feedback loop is required from the monitoring component (e.g., observing the model serving performance) to the scheduler to enable the retraining.

![image](https://user-images.githubusercontent.com/37369603/224610976-fdd9ce5f-007c-447a-aee4-553250ee9f07.png)


