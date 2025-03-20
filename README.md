## Real-Estate-Price-Prediction
![Demo Image](demo_image.png)


# About
This machine learning model takes in a home prices dataset and takes Area (per sqrt), BHK, Bath and location from the user and estimates the price of the real estate property. The model is built using Sklearn and linear regression achieving an accuracy of 82% at predicting prices. A python Flask server has been created that uses the saved model to server http requests. A website component has been built in html, css and javascript that allows user to enter home square ft. area, bedress etc. 

The coolest part of this project is that model is deplowed on AWS using an EC2 instance which runs the model in production cloud environment and makes the model more scalable.

# Technologies Used
1) Python
2) AWS for model hosting
3) Python Flask server for http server
4) Numpy and Pandas for data cleaning
5) Sklearn for model building
6) HTML/CSS/Javascript for UI

# Deploy this app to Cloud (AWS EC2)
1) Create an EC2 instance using amazon console, also in security group add a rule to allow HTTP incoming traffic.
2) Connect the instance to the ssh key using a command line. 
3) Nginx setup 
    i. Install nginx on EC2 instance using these commands :- 
    ```
    sudo apt-get update 
    sudo apt-get install nginx 
    ```

    ii. Above will install nginx as well as run it. Check status of nginx using :- 
    ```sudo service nginx status```

    iii. Now load the cloud url in browser and you will see the Nginx server running!
4) Copy all your local code to the EC2 instance. This can be done using Cyberduck for Mac users or Winscp for windows users. 
5) Now our goal is to point Nginx to load our website properly. Create /etc/nginx/sites-available/ml.conf file. Add the content. 
6) Create a symlink using this command :- 
    ``` sudo ln -v -s /etc/nginx/sites-available/ml.conf ``` 
7) Restart nginx :- 
    ```sudo service nginx restart```
8) Now install python packages in the root directory which can be done either by creating a virtual enviornment and using reqirements.txt file or can be done manually. 
9) Run the following command to :- 
    ```python3 /home/ubuntu/BangloreHomePrices/client/server.py```

This will be a fully functional website running in a production cloud environment. 

