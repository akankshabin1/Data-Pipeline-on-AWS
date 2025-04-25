Data Pipeline on AWS
  AWS services used: 
    •	AWS Glue for creating pipeline
    •	Trigger AWS Glue using AWS Lambda Function
    •	Store data using amazon s3 
    •	Use AWS IAM for policy 
    •	Use AWS Cloudwatch for monitoring
  Lambda Function: Python
    import json
    import boto3
    glueClient = boto3.client('glue')
    def lambda_handler(event, context):
        glueClient.start_job_run(JobName="csvjson")
        return "Job started"
