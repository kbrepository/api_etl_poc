# api_etl_poc
This repository consists of various POC's for understanding fundamentals utilities, such as docker, aws services, jenkins and cicd ., etc.
Description:

In this POC ...


Creating content for AWS Lambda Layer

### Create folder
- mkdir <Folder_Name>
- cd <Folder_Name>
### Create requirements file
- cat > requirements.txt << EOF
boto3==1.26.84
botocore==1.29.84
certifi==2022.12.7
charset-normalizer==3.0.1
idna==3.4
jmespath==1.0.1
python-dateutil==2.8.2
requests==2.28.2
s3transfer==0.6.0
six==1.16.0
urllib3==1.26.14
EOF
### Install requirede dependancies/libraries
- pip3 install -r requirements.txt -t ./
- cd ..
### Zip the content
- zip -r python_modules.zip .

### OPTIONAL move the zip file to s3 bucket
aws s3 cp /home/ec2-user/python_modules.zip s3://<bucket_name>/


## AWS Console - Create Layer

To create a layer (console)
1. Open the Layers page - https://console.aws.amazon.com/lambda/home#/layers of the Lambda console.
2. Choose Create layer.
3. Under Layer configuration, for Name, enter a name for your layer.
4. (Optional) For Description, enter a description for your layer.
5. To upload your layer code, do one of the following:
    - To upload a .zip file from your computer, choose Upload a .zip file. Then, choose Upload to select your local .zip file.
    - To upload a file from Amazon S3, choose Upload a file from Amazon S3. Then, for Amazon S3 link URL, enter a link to the file.

6. (Optional) For Compatible instruction set architectures, choose one value or both values.
7. (Optional) For Compatible runtimes, choose up to 15 runtimes.
8. (Optional) For License, enter any necessary license information.
9. Choose Create.
