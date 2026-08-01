# Identification and Classification of Threat Data in Cloud Platforms Using Machine Learning Techniques

A machine-learning-based cybersecurity project designed to identify anomalous network traffic and demonstrate an automated threat detection and response workflow for cloud-oriented environments.

---

## Project Information

| Field | Details |
|---|---|
| **Project Type** | B.Tech Project-I |
| **Institution** | Vellore Institute of Technology |
| **School** | School of Computer Science and Engineering |
| **Completed** | November 2024 |
| **Contributors** | Naveen Kumar J and Avishkar SP |
| **Project Supervisor** | Sivaprakash S |
| **Primary Domain** | Cloud Security and Machine Learning |
| **Project Areas** | Intrusion Detection, Network Traffic Analysis and Security Automation |

---

## Table of Contents

- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Project Objectives](#project-objectives)
- [System Architecture](#system-architecture)
- [Data Flow](#data-flow)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Machine-Learning Models](#machine-learning-models)
- [Technologies Used](#technologies-used)
- [Evaluation Metrics](#evaluation-metrics)
- [Experimental Results](#experimental-results)
- [Automated Threat Response](#automated-threat-response)
- [Model Comparison](#model-comparison)
- [Security Value](#security-value)
- [Limitations](#limitations)
- [Future Enhancements](#future-enhancements)
- [Repository Scope](#repository-scope)
- [Contributors](#contributors)
- [Disclaimer](#disclaimer)

---

## Project Overview

Cloud computing provides organizations with:

- Scalability
- Flexibility
- Remote accessibility
- Reduced infrastructure costs
- On-demand computing resources
- Support for large-scale applications

However, shared and distributed cloud infrastructure can also increase exposure to cybersecurity risks such as:

- Unauthorized access
- Data breaches
- Insider threats
- Distributed Denial-of-Service attacks
- Abnormal login activity
- Malicious network connections
- Compromised cloud resources

Traditional security systems often rely heavily on manual monitoring and predefined rules.

These approaches may struggle to process large volumes of cloud network traffic, identify evolving attack patterns and respond rapidly to newly detected threats.

This project proposes an automated threat detection and response system that uses machine-learning models to classify network traffic as:

- **Normal**
- **Anomalous**

The three main machine-learning models evaluated in the project are:

- Random Forest
- Decision Tree
- Support Vector Machine

When anomalous traffic is detected, the prototype initiates an automated response workflow representing actions such as:

- Generating a security alert
- Blocking suspicious traffic
- Terminating a malicious session
- Isolating an affected resource
- Recording the detected threat
- Informing a system administrator

---

## Problem Statement

The growing use of cloud platforms has increased the volume and complexity of network activity that security teams must monitor.

Traditional manual and semi-automated security approaches may face several difficulties:

- High volumes of network traffic
- Slow threat-identification processes
- Dependence on human monitoring
- Delayed incident response
- High false-positive rates
- Limited ability to identify previously unseen threats
- Difficulty scaling across different cloud environments

The project addresses the need for an automated system capable of:

- Processing network-traffic data
- Identifying abnormal behaviour
- Classifying potential threats
- Reducing manual intervention
- Initiating rapid threat-response actions
- Supporting future deployment across cloud environments

---

## Project Objectives

The main objectives of the project are:

- Automatically detect anomalous network traffic.
- Distinguish legitimate activity from potentially malicious activity.
- Reduce dependence on continuous manual monitoring.
- Compare multiple machine-learning classification models.
- Evaluate Random Forest, Decision Tree and Support Vector Machine.
- Improve the speed of threat identification.
- Demonstrate an automated threat-response workflow.
- Minimize false-positive and false-negative classifications.
- Design a scalable architecture for cloud security.
- Support future deployment in public, private and hybrid cloud environments.
- Provide a foundation for integration with enterprise security tools.

---

## System Architecture

The proposed architecture connects cloud infrastructure, network-data collection, preprocessing, machine-learning-based threat detection, system monitoring, logging and automated response components.

<p align="center">
  <img src="images/system-architecture.png" alt="System architecture for automated cloud threat detection and response" width="900">
</p>

### Architecture Components

#### 1. Cloud Environment

The cloud environment represents:

- Infrastructure as a Service resources
- Platform as a Service resources
- Software as a Service resources
- Compute systems
- Storage services
- Network infrastructure
- Multi-cloud integrations

#### 2. Data Collection Layer

The data collection layer is responsible for:

- Monitoring network traffic
- Collecting security logs
- Receiving cloud activity data
- Processing incoming data
- Preparing information for analysis

#### 3. Threat Detection Layer

The threat detection layer performs:

- Machine-learning model training
- Network-traffic classification
- Anomaly detection
- Threat identification
- Normal-versus-anomalous classification

The primary models used are:

- Random Forest
- Decision Tree
- Support Vector Machine

#### 4. Threat Response Layer

The threat response layer represents actions such as:

- Blocking suspicious IP addresses
- Terminating suspicious sessions
- Isolating affected resources
- Generating security alerts
- Initiating automated response actions

#### 5. System Monitoring and Logging

This component supports:

- Threat reports
- Security alerts
- Response-action logs
- Detection records
- Administrator notifications

#### 6. Cloud Security Management

This component includes:

- Threat-intelligence integration
- Policy enforcement
- Configuration management
- Security-control coordination

#### 7. Administration and Integration

The architecture can support:

- Administrator dashboards
- REST APIs
- Cloud-provider integrations
- Manual intervention when required
- Monitoring and reporting interfaces

---

## Data Flow

The system begins by collecting network data from a cloud environment.

The collected information is cleaned, transformed and normalized before being processed by the machine-learning models.

Each model then classifies the network record as normal or anomalous.

<p align="center">
  <img src="images/data-flow-diagram.png" alt="Data flow diagram for the cloud threat detection system" width="950">
</p>

### Processing Workflow

```text
Cloud Network Traffic
        ↓
Data Collection
        ↓
Data Cleaning
        ↓
Missing-Value Handling
        ↓
Categorical Encoding
        ↓
Feature Selection
        ↓
Feature Normalization
        ↓
Train-Test Split
        ↓
Machine-Learning Model Training
        ↓
Network-Traffic Classification
        ↓
Normal Traffic or Anomalous Traffic
        ↓
Security Logging and Alert Generation
        ↓
Automated Threat Response
```

---

## Dataset

The project uses a network-intrusion dataset derived from a simulated virtual LAN environment containing different types of cyberattack traffic.

Each network connection contains several characteristics that describe the behaviour of the connection.

The records are labelled as:

- **Normal**
- **Anomalous**

### Dataset Characteristics

- **Input attributes:** 41 TCP/IP connection features
- **Target classes:** Normal and anomalous
- **Training records:** 25,192
- **Test records:** 22,544
- **Training columns:** 42, including the target class
- **Test attributes:** 41 network-traffic parameters
- **Training and testing strategy:** 70% training and 30% testing

The test dataset contains 22,544 records with 41 parameters, while the training dataset contains 25,192 records and a target-class field.

### Example Network Features

The dataset includes features such as:

- Connection duration
- Protocol type
- Network service
- Connection-status flag
- Source bytes
- Destination bytes
- Incorrect packet fragments
- Urgent packet count
- Failed login attempts
- Successful login status
- Number of compromised systems
- Root-shell access
- Superuser attempts
- Number of root accesses
- File-creation attempts
- Shell-access activity
- File-access attempts
- Outbound-command activity
- Host-login status
- Guest-login status
- Number of recent connections
- Number of service connections
- SYN error rate
- Service-related SYN error rate
- Reset error rate
- Service-related reset error rate
- Same-service connection rate
- Different-service connection rate
- Destination-host connection count
- Destination-host service count
- Source-port activity
- Destination-host error statistics

---

## Methodology

The project follows a structured machine-learning workflow.

### 1. Dataset Collection

The dataset was obtained from a simulated virtual network environment containing normal network behaviour and different types of malicious activity.

Each record was labelled to support supervised machine-learning classification.

### 2. Train-Test Split

The dataset was divided into:

- **70% training data**
- **30% testing data**

The training subset was used to train the machine-learning models.

The testing subset was used to evaluate how effectively the models classified previously unseen network records.

### 3. Data Cleaning

Missing or incomplete values were handled through:

- Removing incomplete records
- Applying data-imputation techniques
- Checking dataset consistency
- Removing unusable values

### 4. Feature Selection

The project discusses the use of:

- Principal Component Analysis
- Recursive Feature Elimination

These techniques help:

- Reduce unnecessary attributes
- Lower computational requirements
- Retain important security-related features
- Improve model efficiency

### 5. Categorical Encoding

Categorical variables such as protocol type and network service were converted into numerical values.

The project used encoding techniques to make these attributes suitable for machine-learning algorithms.

### 6. Feature Normalization

Numerical features were placed on a consistent scale.

Normalization is particularly important for Support Vector Machine because large differences between feature values may affect classification performance.

### 7. Model Training

The processed dataset was used to train:

- Random Forest
- Decision Tree
- Support Vector Machine

### 8. Model Testing

Each model was tested separately using the testing dataset.

The model predictions were compared with the actual labels to determine classification performance.

### 9. Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix
- ROC curve
- AUC-ROC
- Precision-recall curve

### 10. Automated Response

When a network record was classified as anomalous, the prototype generated a response message indicating that a threat had been detected and a response was being initiated.

---

## Machine-Learning Models

### Random Forest

Random Forest is an ensemble-learning algorithm that combines predictions from multiple decision trees.

It was selected because it:

- Handles high-dimensional datasets.
- Reduces overfitting through ensemble learning.
- Produces stable classification results.
- Handles complex network-security data.
- Works effectively with large feature sets.
- Provides strong classification performance.

#### Strengths

- Robust against overfitting
- Suitable for complex datasets
- Handles many input features
- Provides stable predictions
- Can process large datasets

#### Limitations

- Can require significant computational resources
- Is less interpretable than a single Decision Tree
- May take longer to train with many trees

---

### Decision Tree

Decision Tree classifies network records by recursively dividing the data according to selected feature values.

Each internal node represents a decision rule, while each leaf node represents a final class.

It was selected because it:

- Provides understandable decision rules.
- Is computationally lightweight.
- Is easy to interpret.
- Supports rapid classification.
- Handles categorical and numerical data.

#### Strengths

- Easy to understand
- Fast classification
- Clear decision-making process
- Low computational requirements
- Suitable for real-time classification prototypes

#### Limitations

- May overfit training data
- Can become unstable when data changes
- May perform less effectively than ensemble models on complex datasets

---

### Support Vector Machine

Support Vector Machine separates normal and anomalous records by identifying a decision boundary between classes.

The project uses a Radial Basis Function kernel to support nonlinear classification.

It was selected because it:

- Handles high-dimensional data.
- Works effectively for binary classification.
- Distinguishes normal and anomalous traffic.
- Identifies subtle differences in network behaviour.
- Supports nonlinear classification.

#### Strengths

- Strong classification capability
- Effective with high-dimensional data
- Suitable for anomaly detection
- Supports nonlinear data using kernel functions
- Can produce high precision and recall

#### Limitations

- Can be computationally expensive for large datasets
- Requires careful parameter tuning
- Is less interpretable than Decision Tree
- May take longer to train on large datasets

---

## Technologies Used

### Programming and Development

- Python
- Google Colab

### Machine Learning and Data Processing

- scikit-learn
- TensorFlow
- Pandas
- NumPy

### Data Visualization

- Matplotlib
- Seaborn

### Machine-Learning Algorithms

- Random Forest
- Decision Tree
- Support Vector Machine

### Data-Preparation Techniques

- Missing-value handling
- Data cleaning
- Label encoding
- One-hot encoding
- Feature scaling
- Min-Max scaling
- Principal Component Analysis
- Recursive Feature Elimination
- Train-test splitting

### Cybersecurity Concepts

- Cloud Security
- Intrusion Detection
- Anomaly Detection
- Network Traffic Analysis
- Automated Threat Response
- Security Monitoring
- Threat Classification
- TCP/IP Analysis
- Security Logging
- Incident Response Automation

---

## Evaluation Metrics

### Accuracy

Accuracy measures the overall percentage of correctly classified normal and anomalous network records.

```text
Accuracy = Correct Predictions / Total Predictions
```

### Precision

Precision measures how many records classified as threats were actually anomalous.

High precision helps reduce false-positive security alerts.

```text
Precision = True Positives / (True Positives + False Positives)
```

### Recall

Recall measures how many genuine anomalous records were successfully detected.

```text
Recall = True Positives / (True Positives + False Negatives)
```

### F1-Score

F1-score provides a balanced measurement combining precision and recall.

```text
F1-Score = 2 × (Precision × Recall) / (Precision + Recall)
```

### Confusion Matrix

A confusion matrix displays:

- True positives
- True negatives
- False positives
- False negatives

### ROC Curve

The Receiver Operating Characteristic curve compares:

- True-positive rate
- False-positive rate

### AUC-ROC

AUC-ROC measures the model’s ability to distinguish normal traffic from anomalous traffic across different classification thresholds.

### Precision-Recall Curve

A precision-recall curve shows the relationship between:

- Precision
- Recall

This measurement is especially useful when evaluating threat-detection models.

---

## Experimental Results

The controlled academic evaluation reported strong classification performance for:

- Random Forest
- Decision Tree
- Support Vector Machine

The classification reports and evaluation graphs indicated that the models were able to distinguish normal and anomalous traffic in the project dataset.

### Random Forest Performance

The Random Forest classification report produced precision, recall and F1-score values of `1.00` for both normal and anomalous classes within the controlled dataset.

<p align="center">
  <img src="images/random-forest-classification-report.png" alt="Random Forest classifier performance evaluation" width="650">
</p>

### Reported Random Forest Results

| Metric | Normal Class | Anomalous Class |
|---|---:|---:|
| Precision | 1.00 | 1.00 |
| Recall | 1.00 | 1.00 |
| F1-score | 1.00 | 1.00 |

> These results were obtained using the controlled academic dataset and experimental conditions described in the project report.

---

## Automated Threat Response

After a network record was classified as anomalous, the prototype generated an automated response message.

<p align="center">
  <img src="images/automated-threat-response.png" alt="Automated response initiated after detecting anomalous network records" width="700">
</p>

The prototype demonstrated the connection between:

```text
Threat Detection
        ↓
Threat Classification
        ↓
Alert Generation
        ↓
Automated Response Initiation
```

A future production implementation could connect this response stage to cloud-security controls capable of:

- Blocking a malicious IP address
- Terminating a suspicious network session
- Isolating an affected cloud instance
- Quarantining a compromised host
- Generating a real-time security alert
- Informing a security administrator
- Recording the incident in a SIEM platform
- Triggering an incident-response workflow
- Creating an incident ticket
- Collecting forensic evidence

---

## Model Comparison

The comparison chart shows that Decision Tree, Random Forest and Support Vector Machine each detected 142 anomalous records in the reported evaluation.

<p align="center">
  <img src="images/model-threat-detection-comparison.png" alt="Threats detected by Decision Tree, Random Forest and Support Vector Machine" width="800">
</p>

| Model | Threat Records Detected |
|---|---:|
| Decision Tree | 142 |
| Random Forest | 142 |
| Support Vector Machine | 142 |

The report also presents ROC-AUC values of `1.00` for the evaluated models.

> **Important:** These results were produced using a controlled and comparatively balanced academic dataset. They should not be interpreted as validated production performance in a live enterprise cloud environment.

---

## Security Value

The project demonstrates how machine learning can support cloud-security operations by:

- Automatically processing network datasets
- Distinguishing normal traffic from anomalous traffic
- Reducing dependence on continuous manual monitoring
- Supporting faster threat identification
- Initiating automated response actions
- Improving visibility into abnormal network activity
- Providing a foundation for SIEM integration
- Providing a foundation for IDS integration
- Supporting future multi-cloud deployment
- Demonstrating security automation concepts
- Supporting proactive threat monitoring

---

## Limitations

The project has several important limitations:

- The evaluation was conducted in a controlled academic environment.
- The dataset may not represent the unpredictability of live cloud traffic.
- Real-world cloud datasets are often highly imbalanced.
- The controlled dataset produced unusually high classification results.
- Perfect evaluation results may not be repeated in production environments.
- The automated response was demonstrated as a prototype.
- The system was not integrated with a live cloud-security service.
- The project did not process continuous live cloud traffic.
- Large-scale real-time deployment would require additional latency testing.
- The models would require regular retraining.
- False-positive performance must be validated using more varied datasets.
- Decision Tree may overfit controlled datasets.
- Support Vector Machine may become computationally expensive.
- Production deployment would require access to cloud logs and network telemetry.
- Security controls would require platform-specific configuration.
- Automated blocking actions would require additional validation and safeguards.

---

## Future Enhancements

### Real-Time Data Processing

Future versions could integrate stream-processing platforms such as:

- Apache Kafka
- Apache Flink

These platforms could support:

- Continuous network-data processing
- Real-time alert generation
- Faster threat classification
- Reduced detection latency

### Cloud Security Integration

The system could be integrated with:

- AWS GuardDuty
- Microsoft Azure security services
- Google Cloud security services
- Intrusion Detection Systems
- Intrusion Prevention Systems
- Security Information and Event Management platforms

### Model Explainability

Explainable-AI techniques could be added, including:

- SHAP
- LIME

These techniques could help security analysts understand why individual network records were classified as threats.

### Imbalanced Dataset Handling

Future versions could use:

- Synthetic Minority Oversampling Technique
- Cost-sensitive learning
- Class weighting
- Improved sampling strategies
- Additional real-world datasets

### Scalable Deployment

The system could be deployed using:

- Docker
- Kubernetes
- Cloud-native APIs
- Distributed data processing
- Containerized machine-learning services
- Horizontal resource scaling

### Continuous Learning

The models could be retrained periodically using newly collected network-traffic data.

Continuous learning could help the system adapt to:

- New attack patterns
- Emerging threats
- Zero-day vulnerabilities
- Changes in legitimate network behaviour
- New cloud services and configurations

### Advanced Machine-Learning Models

Future research could evaluate:

- Convolutional Neural Networks
- Recurrent Neural Networks
- Autoencoders
- Online-learning algorithms
- Reinforcement learning
- Deep-learning models
- Hybrid anomaly and signature-based detection

### Security-Orchestration Integration

Threat detection could be connected to incident-response playbooks for:

- IP blocking
- Resource isolation
- Credential disabling
- Administrator notification
- Evidence collection
- Incident-ticket creation
- Session termination
- Host quarantine
- Security-log preservation

### Monitoring Dashboard

A future dashboard could display:

- Real-time security alerts
- Detected threat categories
- Model confidence scores
- Response actions
- Security logs
- Model-performance metrics
- Network-traffic trends
- Detection history
- System-health information

### Threat-Intelligence Integration

External threat-intelligence feeds could provide:

- Known malicious IP addresses
- Newly discovered vulnerabilities
- Malware indicators
- Attack-pattern information
- Threat-severity information

### Model Maintenance

Long-term maintenance could include:

- Periodic model retraining
- Dataset updates
- Performance monitoring
- Detection-rule tuning
- Cloud-integration updates
- Security-patch management

---

## Repository Scope

This repository is a public academic project showcase.

It contains:

- A technical project summary
- Selected system-design diagrams
- Model-evaluation evidence
- An automated-response demonstration
- The project methodology
- Technologies used
- Limitations
- Future enhancements

The following items are not included in this public repository:

- Complete academic report
- Source dataset
- Full implementation code
- Private university documents
- Student identification numbers
- Personal signatures
- Confidential information
- Cloud-account credentials

---

## Contributors

### Naveen Kumar J

B.Tech Project Contributor  
Vellore Institute of Technology

### Avishkar SP

B.Tech Project Contributor  
Vellore Institute of Technology

### Project Supervisor

**Sivaprakash S**  
Assistant Professor Senior  
School of Computer Science and Engineering  
Vellore Institute of Technology

---

## Disclaimer

This repository documents an academic prototype developed for educational and research purposes.

It is not a production security product and has not been validated for deployment in a live enterprise cloud environment.

The reported model performance reflects the academic dataset, implementation and experimental conditions described in the original project report.
