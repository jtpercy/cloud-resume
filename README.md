# Joel Percy's Cloud Resume
Welcome to Joel Percy's Cloud Resume GitHub project. This project was created to demonstrate my Cloud and DevOps related skills.

## Architecture

![AWS Resources](/diagrams/jtpercy_architectureg.png)

A simple architecture pattern was followed to create this website. I use S3 buckets to host static web files, CloudFront distributions for security and caching with Route53 and Certificate manager for DNS hosting and SSL. 

## Deployment
GitHub Actions have been configured for Continuous Deployment. A `storage-deploy.yml` pipeline is triggered on updates to the `frontend` directory. The pipeline authenticates to AWS using Secret Pipeline variables and performs an S3 sync to each bucket. 
