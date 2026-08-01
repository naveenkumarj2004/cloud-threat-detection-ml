**Identification and Classification of Threat Data in Cloud Platforms Using Machine Learning**

A machine-learning-based cybersecurity project designed to identify anomalous network traffic and demonstrate automated threat detection and response for cloud environments.

**Project Overview**

Cloud computing provides scalability, flexibility and cost efficiency. However, its shared and distributed infrastructure can also increase exposure to threats such as unauthorized access, data breaches, insider activity and denial-of-service attacks.

This project develops an automated system that uses machine-learning models to classify cloud-oriented network traffic as:

► Normal

► Anomalous

**The three primary models evaluated were:**

► Random Forest

► Decision Tree

► Support Vector Machine

When anomalous traffic is identified, the prototype initiates an automated response workflow representing actions such as generating an alert, blocking suspicious traffic, terminating a malicious session or isolating an affected resource.


**Project Objectives**

► Automatically detect anomalous network traffic.

► Reduce dependence on continuous manual monitoring.

► Compare Random Forest, Decision Tree and Support Vector Machine.

► Evaluate models using accuracy, precision, recall, F1-score and ROC-AUC.

► Demonstrate an automated threat-response workflow.

► Reduce false-positive security alerts.

► Design a scalable architecture for cloud environments.

► Support future integration with public, private, hybrid and multi-cloud platforms.

**System Architecture**

The proposed architecture connects cloud infrastructure, network-data collection, preprocessing, machine-learning-based threat detection, security monitoring, logging and automated response components.

<img width="557" height="337" alt="image" src="https://github.com/user-attachments/assets/0fcdcd48-44c0-4da2-a905-d9939ac6bd0d" />

**The architecture contains the following components:**

Cloud Environment

**The cloud environment represents:**

► IaaS, PaaS and SaaS resources


► Compute systems

► Storage services

► Network infrastructure

► Multi-cloud integrations

► Data Collection Layer


**This layer performs:**

►Network-traffic monitoring

►Real-time data collection

►Security-log collection

►Data processing

►Threat Detection Layer

**This layer performs:**

►Machine-learning model training

►Network-traffic classification

►Anomaly detection

►Threat identification using Random Forest, Decision Tree and SVM

►Threat Response Layer

**This layer represents actions such as:**

►Blocking suspicious IP addresses

►Terminating malicious sessions

►Isolating affected resources

►Initiating security-response actions

►System Monitoring and Logging

**This component supports:**

►Threat reports

►Security alerts

►Response-action logs

►Administrator notifications

►Cloud Security Management

**This component includes:**

►Threat-intelligence integration

►Policy enforcement

►Configuration management

►Administration and Integrations

**The architecture also supports:**

►Administrator dashboards

►REST APIs

►Cloud-provider integrations

The report describes the architecture as a sequence of data ingestion, preprocessing, anomaly detection and automated response execution.

**Data Flow**

The system begins by collecting network data from a cloud environment.

The collected information is cleaned, transformed and normalized before being processed by the machine-learning models. The models then classify each record as normal or anomalous.

<img width="1275" height="634" alt="image" src="https://github.com/user-attachments/assets/0fe91208-7083-4020-ad2d-f4ef281a5755" />


Cloud Network Traffic

        ↓
Data Collection

        ↓
Data Cleaning and Preprocessing

        ↓
Categorical Encoding
        
        ↓
Feature Normalization
        
        ↓
Machine-Learning Classification
        
        ↓
Normal Traffic or Anomalous Traffic
        
        ↓
Security Logging and Alert Generation
        
        ↓
Automated Threat Response

