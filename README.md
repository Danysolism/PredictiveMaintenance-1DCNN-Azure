---
page_type: sample
languages:
- python
products:
- azure
- azure-machine-learning-service
- TF-Lite
description: "Tensorflow optimization using TF-Lite"
---
# PredictiveMaintenance-1DCNN-Azure


This project presents a predictive maintenance solution for failure prediction in hydraulic pipe systems. For every predefined period (cycle), we will predict if the cooling system is close to failing using temperature sensors. The model will predict if the system is close to total failure, it has reduced efficiency or full efficiency. This example uses Azure Machine Learning Service to ease training, evaluation and versioning of models.


By running this project, you will have the opportunity to work with the following: 

|Technology|Objective/Reason|
|----------|----------------|
|Azure Machine Learning Service|Service that manages Machine Learning development cycle in Azure |
|Tensorflow 2.0|Machine Learning framework|
|1D CNN|Deep Learning Architecture for sequence data|


### Dataset
The dataset used was the [Condition monitoring of hydraulic systems](https://archive.ics.uci.edu/ml/datasets/Condition+monitoring+of+hydraulic+systems#) from UCI repository. Four temperature sensors were used to predict the condition of hydraulic components which compose the pipeline. The sensor data  is split in cycles(frequency of 1 Hz), 60 observation for every single cycle. 


### Model
Since we are dealing with secuential data,  1DCNN  architecture was chosen. This model can identify time dependencies over fixed segments of time, and it works well when the location of the feature within the segment is not of high relevance.

![image](https://user-images.githubusercontent.com/7260235/115911988-14aae000-a46f-11eb-87ab-456ce27325a3.png)


### TF-Lite Model Optimization
Deep Learning models often require significant amounts of computational resources, memory and power to train and run. IoT devices are not able to meet the hardware requirements that deep learning models need. Using TF-Lite we can quantize our model by converting 32-bit floats to more efficient 8-bit integers. 

By [Sara San Luis](https://github.com/xoubinha) and [Daniela Solis](https://github.com/Danysolism)

### References
- [Azure Machine Learning](https://docs.microsoft.com/en-us/azure/machine-learning)
- [TF Optimization Toolkit](https://www.tensorflow.org/lite/guide/get_started)
