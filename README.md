# docker-fastapi-sample
Create a sample Python-based fastapi application (taken from https://fastapi.tiangolo.com/) &amp; dockerize the same
Libraries used: FastAPI, uvicorn

# Steps to deploy fastAPI application in Docker
- Create main.py file containing the sample fastAPI application
- Create requirements.txt file for dependencies (pip freeze > requirements.txt)
- Create virtual environment in Python and install dependencies: fastapi, uvicorn (web server) within it , activate the environment
- Create docker file (create working directory inside the container). We will run the container using the files copied (in the docker file) into the container
- 

