# Real-Estate-Price-Prediction
![Demo Image](demo_image.png)

# About
Real Estate Price Prediction is a machine learning project that estimates real estate property prices based on user provided data. This model utilizes a home prices dataset and takes inputs such as area (per sq ft), BHK, number of bathrooms, and location to predict the home price for that locality. It's built using Sklearn and linear regression, achieving an accuracy of 82% in predicting price. 

The project features a Python Flask server for handling HTTP requests, enabling the model to serve predictions. A user friendly website interface, developed using HTML, CSS, and JavaScript, allows users to input property details.

A key highlight of this project is its deployment on AWS using an EC2 instance, making the model accessible in a production cloud environment, enhancing scalability and reliability.

## Table of Contents
- [Key Features](#key-features)
- [Technologies Used](#technologies-used)
- [Deployment on AWS EC2](#deployment-on-aws-ec2)

## Key Features
- **Price Prediction:** Estimates real estate property prices based on area, BHK, bathrooms, and location.
- **High Accuracy:** Achieves 82% accuracy using linear regression.
- **Web Interface:** User-friendly HTML/CSS/JavaScript interface for data input.
- **Flask Server:** Python Flask server for handling HTTP requests.
- **AWS Deployment:** Deployed on AWS EC2 for scalability and accessibility.

## Technologies Used
- **Python:** Core programming language for the model and server.
- **AWS (EC2):** Cloud platform for hosting the application.
- **Flask:** Python framework for creating the HTTP server.
- **Numpy & Pandas:** Data manipulation and cleaning.
- **Sklearn:** Machine learning library for building model. 
- **HTML/CSS/JavaScript:** Frontend development for the user interface.

## Deployment on AWS EC2

1.  **Create EC2 Instance:**
    * Use the AWS console to create an EC2 instance.
    * Configure the security group to allow incoming HTTP traffic on port 80.
2.  **Connect via SSH:**
    * Use the command line to connect to the EC2 instance using your SSH key.
3.  **Nginx Setup:**
    * **Install Nginx:**
        ```bash
        sudo apt-get update
        sudo apt-get install nginx
        ```
    * **Check Nginx Status:**
        ```bash
        sudo service nginx status
        ```
    * **Verify Nginx:**
        * Access the EC2 instance's public URL in your browser to confirm Nginx is running.
4.  **Transfer Files:**
    * Copy your local code to the EC2 instance using Cyberduck (for macOS) or WinSCP (for Windows).
5.  **Nginx Configuration:**
    * Create `/etc/nginx/sites-available/ml.conf` and add your configuration.
    * Create a symbolic link:
        ```bash
        sudo ln -v -s /etc/nginx/sites-available/ml.conf /etc/nginx/sites-enabled/ml.conf
        ```
    * Restart Nginx:
        ```bash
        sudo service nginx restart
        ```
6.  **Install Python Packages:**
    * Install required Python packages, either using a virtual environment and `requirements.txt` (present in client directory) or manually.
7.  **Run the Flask Server:**
    * Execute the server script:
        ```bash
        python3 /home/ubuntu/BHP/client/server.py
        ```
This will be fully functional website running in production cloud environment. 