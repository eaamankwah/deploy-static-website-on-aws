# deploy-static-website-on-aws

# Table of Contents
* Overview
* Website
* AWS Cloud Services
## Project Deliverables
### S3 Bucket Creation
### S3 Bucket Configuration
### Website distribution through CloudFront
### Access website in web browser
## Project Files
## References

## Overview

This project is first of the Udacity Cloud DevOps Engineer Nanodegree.

The objective of the project is to deploy a static website that require no server-side processing on AWS.
The website will be accessed through three different links including, CloudFront domain name, S3 object URL, and website-endpoint.

## Website

The static websites that only include the following files:
* HTML
* CSS, and
* JavaScript files
The website displays information about travel blog search destinations, travel guide and connections with other travellers.

## AWS Cloud Services

The following AWS cloud services were employed to complete this project:

* Amazon Web Services S3: s3 provides resource hosting and deployments. S3 is an object storage system in the cloud. The product page
diagram of Amazon s3 is shown in the screenshot below:

![S3-product-page](https://github.com/eaamankwah/deploy-static-website-on-aws/blob/main/screenshots/s3-product-page.png)


* AWS CloudFront: provides content delivery network (CDN) services. CloudFront offers low latency and high transfer speeds during website rendering. CloudFront delivers its content through a worldwide network of data centers called edge locations. When a user requests content that you're serving with CloudFront, the request is routed to the edge location that provides the lowest latency (time delay), so that content is delivered with the best possible performance! [cloudfront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.htm). The product page
diagram of Amazon s3 is shown in the screenshot below:

![cf-product](https://github.com/eaamankwah/deploy-static-website-on-aws/blob/main/screenshots/cf-product.png)

## Project Deliverables

### S3 Bucket Creation

An AWS bucket was created with a unique name, and it was made public because static website hosting essentially requires a public bucket.
The image below indicates the successful creation of an s3 bucket:

![aws-bucket](https://github.com/eaamankwah/deploy-static-website-on-aws/blob/main/screenshots/aws-bucket.png)

The website files and were uploaded to the s3 buckets and can be identified on the screenshot below:

![bucket-content](https://github.com/eaamankwah/deploy-static-website-on-aws/blob/main/screenshots/bucket-uploads.png)

### S3 Bucket Configuration

A bucket policy written in json that allows access to objects stored in the bucket was created as shown below:

![bucket-policy](https://github.com/eaamankwah/deploy-static-website-on-aws/blob/main/screenshots/bucket-policy.png)

Permission that enables static website hosting was granted under the bucket's properties and thereby resulting which in
the generation of the following endpoint that make the website publicly accessible.
http://my-126016128427-bucket.s3-website.us-east-2.amazonaws.com

The screenshot below indicates the bucket configuration settings:

![bucket-config-settings](https://github.com/eaamankwah/deploy-static-website-on-aws/blob/main/screenshots/bucket-config.png)

The screenshot below indicates the successful creation of the bucket website endpoint:

![bucket-ws-endpoint](https://github.com/eaamankwah/deploy-static-website-on-aws/blob/main/screenshots/bucket-endpoint.png)

### Website distribution through CloudFront

An AWS CloudFront Distribution was created from the AWS services dashboard in order to speed up the distribution of the static html
web contents. The essential settings of CloudFront included the following:
* The origin path was set to indicate the root level
* A read permission was granted to update the bucket policy.
* The default cache behavior settings were set to redirect both HTTP to HTTPS.
* The default landing page, index.html was set as the default root object.

The following domain name was setup when CloudFront distribution was created : d2dfbe4ff56qly.cloudfront.net/

The screenshot below indicates the successful creation of the domain name of the CloudFront distribution:

![CloudFront-domain-name](https://github.com/eaamankwah/deploy-static-website-on-aws/blob/main/screenshots/domain-name-distribution.png)

### Access website in web browser
A google web browser was opened to access the static website through three different links:

1. CloudFront domain name - d2dfbe4ff56qly.cloudfront.net as shown in the screenshot below:

![CloudFront-dn-rending](https://github.com/eaamankwah/deploy-static-website-on-aws/blob/main/screenshots/cf-dn-rending.png)

2. S3 object URL - https://my-126016128427-bucket.s3.us-east-2.amazonaws.com/index.html as shown in the screenshot below:

![s3-url-rending](https://github.com/eaamankwah/deploy-static-website-on-aws/blob/main/screenshots/s3-object-url.png)

3. Website through website-endpoint - http://my-126016128427-bucket.s3-website.us-east-2.amazonaws.com/ as shown in the screenshot below:

![website-rending](https://github.com/eaamankwah/deploy-static-website-on-aws/blob/main/screenshots/ws-endpoint.png)

## Project Files

1. README.md - provides discussion on your project
2. Screenshot images - displays major steps from beginning to the end of the project.

# References

* [AWS CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html)

* [Udacity Q & A Platform](https://knowledge.udacity.com/?nanodegree=nd9991&page=1&project=616&rubric=2573)
