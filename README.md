# Real-Estate-Price-Prediction  
![Demo Image](demo_image.png)

## Table of Contents  
- [About](#about)  
- [Technologies Used](#technologies-used)  
- [Deploy This App to Cloud (AWS EC2)](#deploy-this-app-to-cloud-aws-ec2)

## About  
This machine learning model predicts real estate prices based on user inputs such as:  
- **Area (per sqft)**  
- **Number of Bedrooms (BHK)**  
- **Number of Bathrooms**  
- **Location**  

The model is built using **Sklearn** and **Linear Regression**, achieving an **82% accuracy** in price prediction.  
A **Flask server** is used to handle HTTP requests, and a **web interface** is built using **HTML, CSS, and JavaScript** to allow users to input property details.  

A key highlight of this project is that the model is **deployed on AWS EC2**, making it **scalable** and **cloud-hosted** in a **production environment**.  

## Technologies Used  
- **Python** (Data Processing & Model Building)  
- **AWS EC2** (Cloud Hosting)  
- **Flask** (Backend HTTP Server)  
- **NumPy & Pandas** (Data Cleaning)  
- **Sklearn** (Model Training)  
- **HTML, CSS, JavaScript** (Frontend UI)  

## Deploy This App to Cloud (AWS EC2)

### 1) Create an EC2 Instance  
- Use the **Amazon Console** to create an **EC2 instance**.  
- In the **Security Group**, add a rule to **allow HTTP incoming traffic**.  

### 2) Connect to the Instance  
Connect using **SSH** with your private key:  
```sh
ssh -i "your-key.pem" ubuntu@your-ec2-instance-ip
