# Overview
We can briefly define IoT as the internet of things. IoT represents smart devices that can connect to the internet, as it is briefly mentioned in the internet and in many articles. IDS is referred to as an intrusion detection system. In short, it is called systems that detect intrusions in network traffic. We can call it IoT-IDS for short in systems formed to detect attacks on IoT devices. Recently, we tried to test the success of the binary neural network (BNN) system, which is used in image datasets and is said to have a great advantage over other machine learning systems, in the IoT-IDS system using the dataset called IoTID20. We compared this with the artificial neural network (ANN) machine learning system.



# Dataset (IoTID20)

The exponential growth of the Internet of Things (IoT) devices provides a large attack surface for intruders to launch more destructive cyber-attacks. The intruder aimed to exhaust the target IoT network resources with malicious activity. New techniques and detection algorithms required a well-designed dataset for IoT networks. We proposed a new dataset, namely IoTID20, generated dataset from [1]. The new IoT botnet dataset has a more comprehensive network and flow-based features. The flow-based feature can be used to analyze and evaluate a flow-based intrusion detection system. Our proposed IoT botnet dataset will provide a reference point to identify anomalous activity across the IoT networks. The IoT Botnet dataset can be accessed from [2]. The new IoTID20 dataset will provide a foundation for the development of new intrusion detection techniques in IoT networks.

![Ekran Alıdfghjklşintısı](https://user-images.githubusercontent.com/59619952/128051463-77aee342-7d21-4df0-865d-c8f546a70ad5.PNG)

![image](https://user-images.githubusercontent.com/59619952/128054495-9bd612df-da5c-49f2-bcd8-ddaff23eee58.png)


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


# Hardwares on HPC



# Experiment Results
