# ELK Stack Deployment on TryHackMe Lab
## Introduction
This project involves deploying and configuring the ELK Stack (Elasticsearch, Logstash, and Kibana) as part of the SOC Level 2 path on TryHackMe. The ELK Stack is a powerful set of tools for searching, analyzing, and visualizing log data in real-time, which is crucial for cybersecurity monitoring and incident response.

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
  <img width="1173" alt="KALI LIN DX" src="https://github.com/user-attachments/assets/44e98be6-c841-4ff8-8eb9-9905a81a84b9">

- **Changing Configuration Settings:**
  The configuration is set to check for changes in the log sources every 3 seconds.
  <img width="964" alt="File Actions" src="https://github.com/user-attachments/assets/a85f5fc5-0248-47aa-b058-98dca4ca4fbe">

- **Checking the Installed Version of Logstash:**
  <img width="828" alt="Pasted Graphic 25" src="https://github.com/user-attachments/assets/e865e756-c649-4954-b454-95d1973bc32f">

### 6. Installing and Configuring Kibana
Kibana provides the web interface for visualizing and interacting with the data stored in Elasticsearch.

- **Installing Kibana:**
<img width="780" alt="Preparing" src="https://github.com/user-attachments/assets/00c3e974-2f1c-48a6-b65c-ab14f13b360b">

- **Making the Kibana Service Persistent:**
  Run the following commands to ensure Kibana starts automatically:
  <img width="761" alt="Pasted Graphic 19" src="https://github.com/user-attachments/assets/00afdfd5-e0ed-42bf-bb07-1fe346b89792">

- **Checking Kibana Status:**
 <img width="837" alt="Pasted Graphic 21" src="https://github.com/user-attachments/assets/6585d895-10b1-47d7-ad34-527003b27119">

### 7. Accessing the Kibana Interface
Log in to the Kibana interface using your browser.

- **Logging into Kibana:**
 <img width="1508" alt="Configure Elastic to get started" src="https://github.com/user-attachments/assets/0e73c260-abdd-4048-8e26-4bf50b2b6099">


### 8. Creating an Enrollment Token
The enrollment token is required to connect Kibana to Elasticsearch.

- **Creating and Using the Enrollment Token:**
  <img width="911" alt="File Actions Edit View Help" src="https://github.com/user-attachments/assets/b8c26cf9-abd1-4c6a-946c-210518108b8e">
- **Pasting the token into the website:**
  <img width="1244" alt="Configure Elastic to get started" src="https://github.com/user-attachments/assets/6f77043a-a89b-4ce3-bbcf-109ab872e704">



### 9. Verification Code Required
Elasticsearch requires a verification code to complete the setup.
<img width="1017" alt="Verification required" src="https://github.com/user-attachments/assets/dccbf74d-e904-4f2e-be4d-10be092fa6a0">

- **Getting the Verification Code from the Terminal:**
  <img width="979" alt="Pasted Graphic 33" src="https://github.com/user-attachments/assets/17b95703-3794-459d-ab4e-989069518ce3">

```
