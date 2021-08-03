# Overview

Internet usage is increasing rapidly nowadays. This rapid increase has many benefits that make our lives easier, but it has many problems as well as benefits. The most dangerous and important of these problems may be cyber threats. These threats can cause all kinds of harm to many institutions, states, communities or individuals. Intrusion detection systems can be the most useful of the measures that can be taken against these damages. Today, machine learning algorithms are the basis of most intrusion detection systems. The aim of this study is to test the binary neural network (BNN) algorithm, which is generally tried on image data, against the attacks on IoT devices, on the IoTID20 dataset, which is one of the most up-to-date datasets, and to compare the results of this test with the test results of the artificial neural network (ANN) algorithm in this dataset.

We can briefly define IoT as the internet of things. IoT represents smart devices that can connect to the internet, as it is briefly mentioned in the internet and in many articles. IDS is referred to as an intrusion detection system. In short, it is called systems that detect intrusions in network traffic. We can call it IoT-IDS for short in systems formed to detect attacks on IoT devices.



# Paper

# Dataset (IoTID20)

The exponential growth of the Internet of Things (IoT) devices provides a large attack surface for intruders to launch more destructive cyber-attacks. The intruder aimed to exhaust the target IoT network resources with malicious activity. New techniques and detection algorithms required a well-designed dataset for IoT networks. We proposed a new dataset, namely IoTID20, generated dataset from [1]. The new IoT botnet dataset has a more comprehensive network and flow-based features. The flow-based feature can be used to analyze and evaluate a flow-based intrusion detection system. Our proposed IoT botnet dataset will provide a reference point to identify anomalous activity across the IoT networks. The IoT Botnet dataset can be accessed from [2]. The new IoTID20 dataset will provide a foundation for the development of new intrusion detection techniques in IoT networks.


<p align="center">
  <img src="https://user-images.githubusercontent.com/59619952/128051463-77aee342-7d21-4df0-865d-c8f546a70ad5.PNG"/>
</p>


<p align="center">
  <img src="https://user-images.githubusercontent.com/59619952/128054495-9bd612df-da5c-49f2-bcd8-ddaff23eee58.png"/>
</p>


For more information about the dataset: [1] https://ieee-dataport.org/open-access/iot-network-intrusion-dataset

Source: [2] https://sites.google.com/view/iot-network-intrusion-dataset/home 

Downloaded from - https://drive.google.com/drive/folders/1SmLczDUiCfcFb0HzdYM1wUuMoZobsUhp


# Method

## Normalization
-MinMax Normalization

-Standard Normalization

## Sampling
-SMOTE

## Feature Selection
-Variance Method

## Classifiers
### -Artificial Neural Network (ANN)
Artificial neural networks (ANN) are a system inspired by the working principle of the human brain. This system is a structure established in the form of layers. These are a machine learning model consisting of 3 layers: the input layer, the intermediate (hidden) layer, and the output layer . Each layer has its own neurons. And with various mathematical operations that occur in these neurons, it is decided whether this neuron is working. This is the general principle of operation.

### -Binary Neural Network (BNN)
Any layer has two types of inputs: the layer parameters, such as a weight matrix and biases, and incoming activations.  We can reduce the memory footprint of the model by binarizing parameters.  To get the efficiency of binary computations, the incoming activations need to be binary as well. This can be done by setting a input_quantizer.  Note that the output of a binarized layer is not binary. Instead the output is an integer, due to the summation that appears in most neural network layers.  When viewing binarization as an activation function just like ReLU, one may be inclined to binarize the outgoing activations rather than the incoming activations. However, if the network contains batch normalization layers or residual connections, this may result in unintentional non-binary operations. Therefore we have opted for an input_quantizer rather than an activation_quantizer[1]. When training a BNN, we constrain both the weights and the activations to either +1 or r 1. Those two values are very advantageous from a hardware perspective[2].
            
  ![Ekran_Alıhjkjlkşkllşkşntısı-removebg-preview (1)](https://user-images.githubusercontent.com/59619952/128050899-2a62eb29-c73a-4f51-afb1-fda1745cd084.png)

For more information about the BNN: [1]: https://docs.larq.dev/larq/

Source [2]: https://arxiv.org/abs/1602.02830


# The Process


<p align="center">
  <img src="https://user-images.githubusercontent.com/59619952/128087359-0c9c57ca-095c-46b1-b951-b1e46ac3cc6c.png"/>
</p>


# Hardwares on HPC



# Experiment Results





# Requirement
      1- jupyterlab
      2- tensorflow
      3- scikit-learn
      4- pandas
      5- numpy
      6- keras
      7- larg
      8- matplotlib
      9- itertools
      10- imblearn
      11- collections
      12- csv
      
      
# Explanation of Files
 * 1- Data_Cleaning-Mapping.ipynb           -->  Cleaning and mapping the raw data files.
 * 2- Graphic.ipynb                         -->  Visualization of data.
 * 3- Over_Sampling_Smote.ipynb             -->  
 * 4- ANN.ipynb                             -->  Build model with ANN.
 * 5- ANN with feature selection.ipynb      -->  Build model with ANN and Variance method.
 * 6- BNN.ipynb                             -->  Build model with BNN.
 * 7- BNN with feature selection.ipynb      -->  Build model with BNN and Variance method. 






