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



