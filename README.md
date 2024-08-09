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

### Making the service persistent
```bash
systemctl enable elasticsearch.service
systemctl start elasticsearch.service

### I modified the elasticsearch.yml file to set the network host and HTTP port, which ensures Elasticsearch is accessible on the network
(insert picture of open the elastic search configuration)

### Installing logstash to handle log ingestion.
(pic below)
Installing log stash  (picture below)
Change configuration settings to look at the configuration files every 3s to see if there are any changes to the log sources which are being ingested  (picture below)
Checking to see which version of logstash I installed  (picture below)
Installing and configuring kibana  (picture below)
The following commands to make the kibana service persistent  (picture below)
Checking on the status of kibana  (picture below)
Logging in on the Kibana interface  (picture below)
Creating an enrollment token  (picture below)
Pasted the token into elastic search website  (picture below)
Verification code required  (picture below)
Getting the code from the terminal  (picture below)
