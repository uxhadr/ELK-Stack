# ELK Stack Deployment on TryHackMe Lab
## Introduction
This project involves deploying and configuring the ELK Stack (Elasticsearch, Logstash, and Kibana) as part of the SOC Level 2 path on TryHackMe. The ELK Stack is a powerful set of tools used for searching, analyzing, and visualizing log data in real-time, which is crucial for cybersecurity monitoring and incident response.

## Setup and Installation
### 1. SSH into the TryHackMe Room
First, SSH into the room using the provided credentials.
<img width="1162" alt="image" src="https://github.com/user-attachments/assets/533b6b0c-0739-42d4-9499-6096bb3ace86">
### Step 2: Installing Elasticsearch
Elasticsearch is the core of the ELK stack, providing a scalable search and analytics engine. The installation process involves downloading the package and setting it up to run as a service, ensuring it starts automatically with the system.
- **Command to Install Elasticsearch:**
  ```bash
  dpkg -i elasticsearch.deb

### 3. Making the service persistent
```bash
systemctl enable elasticsearch.service
systemctl start elasticsearch.service
```

### 4. Configuring Elasticsearch
I modified the `elasticsearch.yml` file to set the network host and HTTP port, ensuring Elasticsearch is accessible on the network.

![Configuring Elasticsearch](https://github.com/user-attachments/assets/6c465e82-6e28-403a-b348-3700baa910be)

### 5. Installing Logstash
Logstash is responsible for handling log ingestion. Below is the process for installing and configuring Logstash.

- **Installing Logstash:**
  ![Installing Logstash](picture_below)

- **Changing Configuration Settings:**
  The configuration is set to check for changes in the log sources every 3 seconds.
  ![Changing Configuration Settings](picture_below)

- **Checking the Installed Version of Logstash:**
  ![Checking Installed Version](picture_below)

### 6. Installing and Configuring Kibana
Kibana provides the web interface for visualizing and interacting with the data stored in Elasticsearch.

- **Installing Kibana:**
  ![Installing Kibana](picture_below)

- **Making the Kibana Service Persistent:**
  Run the following commands to ensure Kibana starts automatically:
  ![Making Kibana Service Persistent](picture_below)

- **Checking Kibana Status:**
  ![Checking Kibana Status](picture_below)

### 7. Accessing the Kibana Interface
Log in to the Kibana interface using your browser.

- **Logging into Kibana:**
  ![Logging into Kibana](picture_below)

### 8. Creating an Enrollment Token
The enrollment token is required to connect Kibana to Elasticsearch.

- **Creating and Using the Enrollment Token:**
  ![Creating Enrollment Token](picture_below)

### 9. Verification Code Required
Elasticsearch requires a verification code to complete the setup.

- **Getting the Verification Code from the Terminal:**
  ![Getting Verification Code](picture_below)
```
