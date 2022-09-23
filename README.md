# docker-fastapi-sample
Create a sample Python-based fastapi application (taken from https://fastapi.tiangolo.com/) &amp; dockerize the same
Libraries used: FastAPI, uvicorn

# Steps to deploy fastAPI application in Docker
- Create main.py file containing the sample fastAPI application
- Create requirements.txt file for dependencies (pip freeze > requirements.txt)
- Create virtual environment in Python and install dependencies: fastapi, uvicorn (web server) within it , activate the environment
use the command "virtual_env_name\Scripts\activate" to activate

![image](https://user-images.githubusercontent.com/56335301/191937343-1c0a8cf4-1a0f-42d5-926f-6695ae8e57b8.png)

- Create docker file (create working directory inside the container). We will run the container using the files copied (in the docker file) into the container
- Build the docker image 

![image](https://user-images.githubusercontent.com/56335301/191937712-c05e85a8-91c6-4014-b2c1-e63476fce727.png)

![image](https://user-images.githubusercontent.com/56335301/191938443-ab596abf-9542-4b1b-a7b5-71f57e738b53.png)


- Run the container containing the image

![image](https://user-images.githubusercontent.com/56335301/191937890-e45067b9-7891-4379-83dd-3438119b7570.png)

- And we get below issue

![image](https://user-images.githubusercontent.com/56335301/191937999-5527cad0-744d-42dd-92b6-ae4906882b51.png)

- To resolve this, we need to map the port number of system to the Docker port like below, both in cmd prompt and also in the app.py
![image](https://user-images.githubusercontent.com/56335301/191938641-435c3a16-9b67-44fa-90eb-7fa70e783cab.png)

![image](https://user-images.githubusercontent.com/56335301/191939712-324a23f2-d34d-4c8a-b296-6419c6564f4a.png)

** NOTE:**
![image](https://user-images.githubusercontent.com/56335301/191941524-1c217f92-4600-4006-9b24-d0e15fac007a.png)


- Use "http://127.0.0.1:8000" to view the output


![image](https://user-images.githubusercontent.com/56335301/191940785-f4904139-6844-40d0-a559-1dbbe5b6f0fb.png)

- Also check the output on another route/API

![image](https://user-images.githubusercontent.com/56335301/191940909-c3704429-ea0e-41a3-b864-cde9924c168f.png)

- We can also observe all these results on Docker desktop, along with some other interesting stuff related to container details

![image](https://user-images.githubusercontent.com/56335301/191941097-8810c955-a3d8-4e04-a535-aba3fb7224a7.png)

- In the cmd prompt of windows, type: docker ps & fetch the container ID

![image](https://user-images.githubusercontent.com/56335301/191942442-153653ae-0a62-4d93-9beb-567458f2c8ce.png)

 - When the command docker exec -it container_ID is executed, we get SHELL inside this container like below
 ![image](https://user-images.githubusercontent.com/56335301/191942786-6f2314c9-e4e7-47fd-aaf0-af3c32868f03.png)

- And, when we execute ls against this container, we get the files which we moved inside the container (app, requirements.txt)
![image](https://user-images.githubusercontent.com/56335301/191942939-d95bf764-5e25-4f12-9486-762d0ac98cb4.png)

- We can also go 2 levels up and see the main working directory (fastapi-app) which we created inside the container as part of dockerfile
![image](https://user-images.githubusercontent.com/56335301/191943159-ea05ef4f-70f2-46ce-8484-b86627df28e9.png)

- And view the contents once again inside this fastapi-app
![image](https://user-images.githubusercontent.com/56335301/191943286-95901b45-37f0-41c7-bcfe-57355147a6b5.png)


# Creating virtual environment on Windows
![image](https://user-images.githubusercontent.com/56335301/191947886-cfbc225e-4c1a-4bf1-8476-a37cb7904b7f.png)
![image](https://user-images.githubusercontent.com/56335301/191948101-0922fe22-def8-4705-a6f6-e50e160b3caa.png)

