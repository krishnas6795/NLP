# Installations

pip install venv

mkdir summarizer_app
cd summarizer_app
python -m venv .
Scripts\activate.bat

pip install streamlit gensim==3.8.3 sumy gensim_sum_ext pandas altair seaborn rouge

## Running:

Streamlit run app.py

## Dockerfile
# Defining the base image
FROM python:3.9-slim

# Updating and installing the python essentials
RUN apt update && apt -y install build-essential

# Setting the container work directory
WORKDIR /app

# Installing the packages
RUN pip install -r requirements.txt

# Copying the Source code to Container work dir
COPY . .

# Command to start the streamlit application
CMD ["streamlit", "run", "app.py", "host=0.0.0.0"]

# dockerignore file

### Folders to be ignored
Include/
Lib/
Scripts/
etc/
share/

### Files to be ignored
.gitignore
pyvenv.cfg