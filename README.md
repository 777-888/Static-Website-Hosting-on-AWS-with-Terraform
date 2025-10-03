# 🌍 Static Website Hosting on AWS with Terraform

This project provisions a **static website** on AWS using **S3 + CloudFront**, fully automated with Terraform.

## 🚀 Architecture
- **S3** – Stores static website files (HTML, CSS, JS).
- **CloudFront** – Global CDN for content delivery with HTTPS.
- **IAM & Bucket Policy** – Controls access to content.
- **Terraform** – Infrastructure as Code for repeatable deployments.

## 📂 Project Structure
terraform-s3-cloudfront-static-site/
├── main.tf # Core resources (S3, CloudFront, IAM policy)
├── variables.tf # Input variables
├── outputs.tf # Output values
├── index.html # Sample static website page
└── README.md # Documentation

## 🛠️ Usage

1. Clone this repo:
   ```bash
   git clone https://github.com/777-888/terraform-s3-cloudfront-static-site.git
   cd terraform-s3-cloudfront-static-site
2. Initialize Terraform:
terraform init
3. Plan & Apply:
terraform plan -var="bucket_name=my-terraform-static-site"
terraform apply -var="bucket_name=my-terraform-static-site"
4. Upload your own HTML/CSS/JS files into the bucket:
aws s3 cp ./site/ s3://my-terraform-static-site/ --recursive
5. After apply, Terraform outputs a CloudFront URL → open it in your browser 🌍
🖼️ Architecture Diagram
<!-- optional if you want to add one -->
🔒 Security
S3 bucket restricted to GetObject only.
CloudFront enforces HTTPS.
AWS IAM used for least-privilege access.
