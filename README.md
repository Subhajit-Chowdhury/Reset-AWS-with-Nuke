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

AWS Nuke is an open-source tool designed to delete all resources in an AWS account, restoring it to a clean slate. This is particularly useful for testing, development, or compliance purposes.

For detailed documentation, visit the [AWS Nuke GitHub Repository](https://github.com/rebuy-de/aws-nuke).

---

## 🛠 Prerequisites

Before you begin, ensure the following:

1. **AWS CLI Installed**: Install or update the AWS CLI by following [this guide](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).
2. **AWS Account Access**: Ensure you have administrative access to the AWS account you want to reset.
3. **AWS Nuke Installed**: Install AWS Nuke using the instructions below.

---

## 📦 Installation Steps

### 1️⃣ Install AWS CLI

Follow the official guide to install the AWS CLI:  
🔗 [AWS CLI Installation Guide](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

**Check AWS CLI version:**
```bash
aws --version
```
![AWS CLI Version](screenshots/aws-v.png)  
*Verify that the AWS CLI is installed correctly.*

### 2️⃣ Configure AWS CLI

Run the following command to configure your AWS CLI:
```bash
aws configure
```
Provide your AWS access key, secret key, region, and output format.

![AWS Configure](screenshots/aws-config.png)  
*Configure your AWS CLI with your credentials and default region.*

### 3️⃣ Install AWS Nuke

Install AWS Nuke based on your operating system:

- **macOS**:  
  ```bash
  brew install cloud-nuke
  ```
- **Linux**:  
  ```bash
  brew install cloud-nuke
  ```
- **Windows**:  
  ```bash
  winget install cloud-nuke
  ```

*Choose the installation command based on your OS.*

---

## 🔧 Usage Instructions

### Step-by-Step Commands:

1. **Verify AWS CLI Installation**  
   ```bash
   aws --version
   ```
   ![AWS CLI Version](screenshots/aws-v.png)  
   *Ensure the AWS CLI is working before proceeding.*

2. **List S3 Buckets (Optional)**  
   ```bash
   aws s3 ls
   ```
   ![AWS S3 List](screenshots/aws-test.png)  
   *Optionally, list your S3 buckets to see what resources exist before nuking.*

3. **Check AWS Nuke Help**  
   ```bash
   cloud-nuke -h
   ```
   ![Cloud Nuke Help](screenshots/cloud-nuke-h.png)  
   *Display the help menu for AWS Nuke.*

4. **Inspect AWS Resources**  
   ```bash
   cloud-nuke inspect-aws --region ap-south-1
   ```
   ![Inspect AWS Resources](screenshots/cloud-nuke-inspect.png)  
   *Scan your AWS account for all resources in the specified region.*

   ![Inspect Result](screenshots/cloud-nuke-inspect-result.png)  
   *Detailed output of resources found during inspection.*

   ### 🎬 Video Walkthrough: Inspect Command
   [![Watch the Inspect Command Demo](screenshots/aws-inspect-command-thumbnail.png)](screenshots/Administrator_ Command Prompt - cloud-nuke  inspect-aws 2025-05-28 23-55-25.mp4)  
   *Click the image above to watch the video walkthrough of running the `inspect-aws` command.*

5. **List Resource Types**  
   ```bash
   cloud-nuke aws --list-resource-types
   ```
   ![List Resource Types](screenshots/cloud-nuke-aws-check.png)  
   *See all resource types that AWS Nuke can delete.*

6. **Perform a Dry Run**  
   ```bash
   cloud-nuke aws --resource-type ec2 --dry-run
   ```
   ![Dry Run](screenshots/Dry-Run.png)  
   *Simulate the deletion process to preview what will be removed.*

7. **Execute AWS Nuke**  
   ```bash
   cloud-nuke aws --region ap-south-1
   ```
   ![Nuke Confirmation](screenshots/aws-nuke-confirm.png)  
   *AWS Nuke will ask for confirmation before proceeding.*

   ![Final Nuke List and Confirmation](screenshots/final-nuke-list-and-confirmation.png)  
   *Final list of resources to be deleted.*

   ![Confirming Nuke](screenshots/confirming-nuke.png)  
   *Type 'yes' to confirm and start the nuke operation.*

   ![Nuke Done](screenshots/nuke-done.png)  
   *AWS Nuke has finished deleting resources.*

   ![After Nuke Check](screenshots/After-nuke-check-from-cmd.png)  
   *Verify that all resources have been deleted.*

---

## 🔒 Security Notice

**IMPORTANT**: When using this guide:

1. Never commit AWS credentials to GitHub.
2. Always use AWS best practices for credential management.
3. Use AWS IAM roles and temporary credentials where possible.
4. Remove sensitive information from screenshots.
5. Add credential files to `.gitignore`.

For detailed security practices, refer to [AWS Security Best Practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html).

---

## ⚠️ Important Notes

- **Dry Run**: Always perform a dry run before executing AWS Nuke.
- **Irreversible Action**: AWS Nuke deletes resources permanently. Double-check before proceeding.
- **Region-Specific**: Specify the region to target specific resources.

---

## 📚 Additional Resources

- **AWS Nuke GitHub Repository**:  
  🔗 [rebuy-de/aws-nuke](https://github.com/rebuy-de/aws-nuke)  
  🔗 [gruntwork-io/cloud-nuke](https://github.com/gruntwork-io/cloud-nuke)

---

## 🎯 Project Goals

This repository aims to:

1. Provide a clear and concise guide for resetting AWS accounts using AWS Nuke.
2. Document commands and resources for future reference.
3. Ensure safe and efficient usage of AWS Nuke.

---

## 🤝 Contributions

Feel free to contribute by improving documentation or adding new features. Open a pull request or raise an issue for suggestions.

---

## ❤️ Created With Love

This project was created with ❤️ by **Subhajit Chowdhury**.

### Connect With Me:  
- 🌐 [LinkedIn](https://www.linkedin.com/in/subhajitch0wdhury/)  
- 🐙 [GitHub](https://github.com/Subhajit-Chowdhury)  
- 📧 Email: er.subhajitchowdhury@gmail.com

---

## 📜 License

This project is licensed under the MIT License. See the LICENSE file for details.

---

## 🔗 References

- **AWS CLI Documentation**: [AWS CLI Guide](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
- **AWS Nuke GitHub Repository**: [rebuy-de/aws-nuke](https://github.com/rebuy-de/aws-nuke)

---

Thank you for visiting the **Nuke_AWS** project! 🌟  
Happy nuking! 💥