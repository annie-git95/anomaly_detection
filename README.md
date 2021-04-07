# anomaly_detection
Detect illegitimate connections in a computer network using an autoencoder

# Malignant-and-Benign-Mole-Classification

The goal of this notebook is to to detect illegitimate connections in a computer network using an autoencoder

**Data set description**
Data set for this project is from The Third International Knowledge Discovery and Data Mining Tools Competition at KDD-99, The Fifth International Conference on Knowledge Discovery and Data Mining. File kddCupTrain.csv with the data necessary for this project contains only one of multiple types of attacks (see below).

The competition task was building a network intrusion detector capable of distinguishing "bad" connections, called intrusions or attacks, from "good" normal connections. This database contains a variety of intrusions simulated in a military network environment.

The original KDD training dataset consists of approximately 4,900,000 single connection vectors each of which contains 41 features and is labeled as either normal or an attack, with exactly one specific attack type. The simulated attacks fall in one of the following four categories:

**Denial of Service Attack (DoS):** is an attack in which the attacker makes some computing or memory resource too busy or too full to handle legitimate requests, or denies legitimate users access to a machine.
**User to Root Attack (U2R):** is a class in which the attacker starts out with access to a normal user account on the system (perhaps gained by sniffing passwords, a dictionary attack, or social engineering) and is able to exploit some vulnerability to gain root access to the system.
**Remote to Local Attack (R2L):** occurs when an attacker who has the ability to send packets to a machine over a network but who does not have an account on that machine exploits some vulnerability to gain local access as a user of that machine.
**Probing Attack:** is an attempt to gather information about a network of computers for the apparent purpose of circumventing its security controls.

The attribute labeled 41 in the data set is the "Class" attribute which indicates whether a given instance is a normal connection instance or an attack.


This solution uses [Python 3.7.9](https://www.python.org/downloads/release/python-379/)


## Getting Started
In order to get started you need to complete the following steps:

Install Python 3.7.9

Have a running Tensorflow 2.3 instance

## Solution Design

This solution is broken down into 4 stages.

Stage 1 - Read data from zip folder. You will find the test and train .csv files inside 

Stage 2 - Remove the uninformative columns by inspecting the features

Stage 3 - Create the an autoencoder model containing fully connected layers with 14, 7, 14 and 29 neurons, respectively. The first two layers make encoder, the last two make decoder. Training is done with L1 regularization.

Stage 4 - Predict test data and evaluate classification report.
