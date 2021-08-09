# Defining the base image
FROM python:3.9-slim

# Updating and installing the python essentials
# RUN apt update && apt -y install build-essential

# Setting the container work directory
WORKDIR /app

# Copying the Source code to Container work dir
COPY . .

# Installing the packages
RUN pip install -r requirements.txt

# Command to start the streamlit application
CMD ["streamlit", "run", "app.py", "host=0.0.0.0"]
