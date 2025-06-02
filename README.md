# AWS Account Reset Using AWS Nuke 🚀

<p align="center">
  <img src="https://img.shields.io/badge/AWS%20Nuke-Automated%20Account%20Cleanup-orange?style=for-the-badge&logo=amazonaws&logoColor=white" alt="AWS Nuke Banner"/>
  <img src="https://img.shields.io/badge/Platform-AWS-blue?style=for-the-badge&logo=amazonaws&logoColor=white" alt="Platform AWS"/>
  <img src="https://img.shields.io/badge/Status-Production-green?style=for-the-badge&logo=checkmarx&logoColor=white" alt="Production Status"/>
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge" alt="MIT License"/>
</p>

![AWS Nuke Banner](screenshots/aws-resources-before.png)  
*Initial state of AWS resources before running AWS Nuke.*

---

## 📖 What is AWS Nuke?

AWS Nuke is an open-source tool to delete all resources in an AWS account, restoring it to a clean slate.  
For full documentation, see the [AWS Nuke GitHub Repository](https://github.com/rebuy-de/aws-nuke).

---

## 🛠 Prerequisites

1. **AWS CLI**: [Install or update](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
2. **AWS Account Access**: Admin access required.
3. **AWS Nuke**: See install steps below.

---

## 📦 Installation Steps

### 1️⃣ Install AWS CLI

[Official Guide](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

```bash
aws --version
```
![AWS CLI Version](screenshots/aws-v.png)  
*Check AWS CLI installation.*

### 2️⃣ Configure AWS CLI

```bash
aws configure
```
![AWS Configure](screenshots/aws-config.png)  
*Set up your AWS credentials and region.*

### 3️⃣ Install AWS Nuke

- **macOS/Linux**:  
  ```bash
  brew install cloud-nuke
  ```
- **Windows**:  
  ```bash
  winget install cloud-nuke
  ```

---

## 🔧 Usage Instructions

### 1. Verify AWS CLI

```bash
aws --version
```
![AWS CLI Version](screenshots/aws-v.png)

### 2. (Optional) List S3 Buckets

```bash
aws s3 ls
```
![AWS S3 List](screenshots/aws-test.png)

### 3. AWS Nuke Help

```bash
cloud-nuke -h
```
![Cloud Nuke Help](screenshots/cloud-nuke-h.png)

### 4. Inspect AWS Resources

```bash
cloud-nuke inspect-aws --region ap-south-1
```
![Inspect AWS Resources](screenshots/cloud-nuke-inspect.png)  
![Inspect Result](screenshots/cloud-nuke-inspect-result.png)

#### 🎬 Video: Inspect Command Demo
[![Watch the Inspect Command Demo](screenshots/aws-inspect-command-thumbnail.png)](screenshots/Administrator_Command_Prompt-cloud-nuke-inspect-aws-2025-05-28-23-55-25.mp4)  
*See how to inspect resources before deletion.*

### 5. List Resource Types

```bash
cloud-nuke aws --list-resource-types
```
![List Resource Types](screenshots/cloud-nuke-aws-check.png)

### 6. Dry Run

```bash
cloud-nuke aws --resource-type ec2 --dry-run
```
![Dry Run](screenshots/Dry-Run.png)

### 7. Execute AWS Nuke

```bash
cloud-nuke aws --region ap-south-1
```
![Nuke Confirmation](screenshots/aws-nuke-confirm.png)  
![Final Nuke List](screenshots/final-nuke-list-and-confirmation.png)  
![Confirming Nuke](screenshots/confirming-nuke.png)  
![Nuke Done](screenshots/nuke-done.png)  
![After Nuke Check](screenshots/After-nuke-check-from-cmd.png)

---

## 🔒 Security Notice

- Never commit AWS credentials to GitHub.
- Use IAM roles and temporary credentials.
- Remove sensitive info from screenshots.
- Add credential files to `.gitignore`.

[Best Practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)

---

## ⚠️ Important Notes

- Always perform a dry run before nuking.
- Deletion is permanent.
- Specify the region as needed.

---

## 📚 Additional Resources

- [AWS Nuke GitHub](https://github.com/rebuy-de/aws-nuke)  
- [Cloud Nuke (Gruntwork)](https://github.com/gruntwork-io/cloud-nuke)
- [YouTube: AWS Nuke Guide](https://youtu.be/odk_NuQNJTc?si=wypMlFZcLFyxkEd9)

---

## 🎯 Project Goals

- Provide a clear guide for resetting AWS accounts with AWS Nuke.
- Document commands and resources for reference.
- Ensure safe and efficient usage.

---

## 🤝 Contributions

Contributions welcome. Open a pull request or issue.

---

## ❤️ Created By

**Subhajit Chowdhury**  
[LinkedIn](https://www.linkedin.com/in/subhajitch0wdhury/) | [GitHub](https://github.com/Subhajit-Chowdhury) | er.subhajitchowdhury@gmail.com

---

## 📜 License

MIT License. See LICENSE file.

---

## 🔗 References

- [AWS CLI Guide](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
- [AWS Nuke GitHub](https://github.com/rebuy-de/aws-nuke)

---

Thank you for visiting the **Nuke_AWS** project!  
Happy nuking! 💥