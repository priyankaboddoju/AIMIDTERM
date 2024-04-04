# AIMIDTERM

## Introduction:
This project showcases the process of training, testing, and deploying an SKLearn model on AWS SageMaker. It also illustrates accessing the deployed model from anywhere using a web application client.

## Model and Data:
This code is from Lab 5.4 where we are provided with all training code and dataset(Labeled PE files). The model used in this lab is RandomForestClassifier.

## Deployment:
The models generated in Lab 5.4 are exported and imported using the Joblib library. Subsequently, an inference script is developed, which will be utilized on an AWS SageMaker endpoint to handle input (PE features) received from the client application. All necessary dependencies are documented in the requirements.txt file, which SageMaker will detect and install any missing dependencies. These components are then compressed into a model.tar.gz file, which is uploaded to an S3 bucket for deployment purposes. Following this, an endpoint is established using the compressed file.

## Client:
I've developed a client-side web application using Streamlit in Python, which is run on Google Colab. Users have the capability to upload a .exe file into the application. The backend code extracts PE features from the uploaded file, packages them into JSON format, and sends them to the endpoint for prediction. The application then records the response from the endpoint and displays the classification of the uploaded .exe file.

Thank you
