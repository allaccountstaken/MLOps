# MLOps


MLOps Project Guideline
1.  Project

   Objective: Deploy the term 1 DL project in a production-like environment

   Models: Could be any ML/DL projects that you implemented in the past or in term

   Infrastructure: Consider using some of these services in your project. You can use them all or choose the ones that fit
        
        AWS cloud - Launch the infrastructure using AWS CLI or Boto3 - Bonus point: CloudFormation templates (a lab will be introduced later)
        Compute - EC2 instance -> consider using EC2 for model serving, training, etc. - Lambda -> You can consider using serverless functions in your project
        Storage - S3 -> storing training data, model artifact, features - Databases (RDS, DynamoDB) -> Storing offline, online features
        Managed services - Sagemaker -> training, serving, feature store, pipeline, etc. - EKS -> kubernetes (will cover soon) - API Gateway -> serving, endpoints - Elastic Beanstalk -> deploying application
        
        MLOps workflow
            ML training
                Option 1: Sagemaker
                Option 2: Notebooks running on EC2
                Option 3: Notebooks running locally and then python scripts deployed in container 
            Experimentation
                MLFlow for tracking 
            Model registry
                Sagemaker registry, mlflow, DVC, or simply S3 
            Model Serving
                FastAPI deployed in docker container
                Sagemaker serving
                Kubeflow (introduced later) or Seldon
                API Gateway + Lambda (introduced in previous labs) 
            Model Deployment
                CI/CD with Github action
                CI/CD with AWS Codedeploy 
            Model Monitoring
                Prometheus + Grafana (introduced later)
                Evidently (introduced later) 
        
        
    Presentation/Visualization - Streamlit (will cover in a lab soon) - Custom frontend (if you’re capable and familiar with frontend) 
