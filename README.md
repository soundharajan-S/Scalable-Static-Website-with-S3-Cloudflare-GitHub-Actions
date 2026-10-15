# 🚀 Project 6: Scalable Static Website on AWS

### Live URL: **https://static.awsproject.in**
> Production-grade static hosting with S3 + Cloudflare CDN + GitHub Actions CI/CD

![Live Status](https://img.shields.io/badge/Status-Live%20%26%20Operational-brightgreen)
![AWS S3](https://img.shields.io/badge/AWS-S3-FF9900?logo=amazons3&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-CDN-F38020?logo=cloudflare&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/CI%2FCD-GitHub%20Actions-2088FF?logo=githubactions&logoColor=white)

## 📋 Abstract
Build a scalable static website `static.awsproject.in` that auto-deploys on every commit. Uses S3 for hosting, Cloudflare for CDN + DNS + SSL, GitHub Actions for CI/CD. Achieves <100ms latency, 99.99% uptime.

## 🛠️ Tools Used
| Tool | Purpose | Cost |
|------|---------|------|
| **AWS S3** | Storage & hosting (ap-south-1) | Free Tier 5GB |
| **Cloudflare** | DNS, CDN, SSL, DDoS | FREE FOREVER |
| **GitHub Actions** | CI/CD automation | 2000 min FREE |
| **GoDaddy** | Domain awsproject.in | - |

## 🏗️ Architecture
Developer Push -> GitHub (main) -> Actions -> S3 Sync -> Cloudflare CNAME + Purge -> https://static.awsproject.in

## ⚙️ Steps Involved
1. **S3 Setup:** Bucket `static.awsproject.in`, static hosting ON, public read policy
2. **Cloudflare:** Domain added, NS changed, CNAME `static` -> S3 with Proxy ON, Always HTTPS ON
3. **IAM & Tokens:** IAM user `github-deployer`, S3 access, Cloudflare API Token, Zone ID
4. **GitHub Secrets:** 6 secrets added (AWS keys, region, bucket, Cloudflare IDs)
5. **Workflow:** `.github/workflows/deploy.yml` - checkout, AWS creds, s3 sync --delete, purge cache
6. **Live:** Verified https://static.awsproject.in with SSL + auto-deploy

## 📸 Screenshots
![Live Website](Live%20website.png)
![S3 Bucket](S3%20bucket.png)
![Cloudflare DNS](Cloudflare%20DNS.png)
![Actions](Actions%20Green%20Tick.png)
![GitHub Secrets](GitHub%20Secrets%20page.png)
## 💰 Cost
- **0-12 Months:** 100% FREE
- **After:** ~$0.50-$1/month for 10k visits

## 👨‍💻 Author
**Soundarajan** - Cloud & DevOps Engineer - Oct 2025
Live: https://static.awsproject.in
