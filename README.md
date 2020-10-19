# PredictiveMaintainance
Detect the likelihood of IoT devices breaking down

Introduction
This example shows how a large company with over 50,000 vending machines can use the power of IoT (Internet of Things) and machine learning to determine an individual machine’s likelihood to break down. The company has invested to embed IoT sensors in all their vending machines to collect specific data points that are then sent back to a central data repository for analysis. For this example, we are using a raw data file to simulate the IoT Data Collection Repository.  With the data file as our input, we are going to use machine learning capabilities to build a model that can predict if a machine needs maintenance to prevent it from breaking down. 
 
 
Highlights
 
Machine Learning
Use the power of Talend Machine Learning capabilities to build a Random Forest model.
 
 
Scale with Spark
Use Spark to run your jobs and benefit from its scale-able architecture and power of distributed computing.
 
 
IoT Data
Look at how we use IoT data to achieve predictive maintenance.
 
 
Execution
Access the IoT Predictive Maintenance use-case portal from the sandbox loading page for quick-run directions and an interactive web interface.
 
Open Talend Studio within the sandbox environment.   For this example, we will be working in the IoTPredictiveMaintenance folder found in the repository view.  We will explore jobs in the Standard, and Big Data Batch Job Designs.   When ready to begin, follow the steps below: 
1.	Navigate to the IoTPredictiveMaintenance folder under Standard jobs.  Run job Step_01_SetupEnvironment.  This job initializes the demo environment based on the Big Data Platform you have chosen. Specifically, it loads the data into HDFS and creates a training dataset and testing dataset as well as a third dataset to use in our demo web page. 
2.	Navigate to the IoTPredictiveMaintenance folder under Big Data Batch jobs.  Run job Step_02_Train_PredictiveMaintenance. In this step, you are training a model based on a previous dataset using our tRandomForestModel component. The model will be store in HDFS. 
3.	Optional:  Navigate to the IoTPredictiveMaintenance folder under Big Data Batch jobs.  Run job Step_02bis_Test_PredictiveMaintenance.  The results of this job provide a look at the ratio of right predictions against false positives. In Machine Learning terminology, this is called the Confusion or Error Matrix – a summary of prediction results on a classification problem.  You should get more than 90% accuracy rate.  This job acts as a test of our trained model on a separate dataset.  
4.	Navigate to the IoTPredictiveMaintenance folder under Big Data Batch jobs.  Run job Step_03_PredictMachinesMaintenance. This job will predict needed maintenance of a vending machine based on the previously trained and tested model using a simulated “Live” dataset.  
5.	Navigate to the IoTPredictiveMaintenance folder under Standard jobs.  Run job Step_04_WebService. This job simply provides a Web API to the demo portal page and allows you to see the results.  
6.	With the Web Service running, navigate to or reload IoT Predictive Maintenance portal page to see all the machines that our model predicts will break down soon.  These machines will require preventative maintenance.  
 
Conclusion
This example highlights the use of IoT sensor data with Machine Learning to perform intelligent predictions.  Big data integration coupled with Spark processing provides a robust and scalable solution to achieve quick and reliable performance.  In this case, we are predicting the likelihood of a vending machine requiring maintenance before it becomes inoperable.  
