# Deploying-Static-Website-Over-S3
This repo is created for the demonstration of deployment of static website over S3 bucket and accessible by anyone over the internet.

Steps for the demo
1) Created a S3 bucket.
2) Went to the permision tab, chnaged **Block public access (bucket settings)** from block to allow.
3) Went to property tab and enabled **Static website hosting**.
4) one final task is to write a script in **Bucket policy**
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "allowallpermision",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::bucket_name/*"
        }
    ]
}
