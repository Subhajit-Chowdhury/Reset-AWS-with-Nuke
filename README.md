# AWS Account Reset Using AWS Nuke 🚀

<p align="center">
  <img src="screenshots/project-banner.png" alt="AWS Nuke Project Banner" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/AWS%20Nuke-Automated%20Account%20Cleanup-orange?style=for-the-badge&logo=amazonaws&logoColor=white"/>
  <img src="https://img.shields.io/badge/Platform-AWS-blue?style=for-the-badge&logo=amazonaws&logoColor=white"/>
  <img src="https://img.shields.io/badge/Status-Production-green?style=for-the-badge&logo=checkmarx&logoColor=white"/>
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge"/>
</p>

<br/>

![AWS account before running AWS Nuke](https://github.com/Subhajit-Chowdhury/Reset-AWS-with-Nuke/blob/main/aws%20resources%20before.png)  
*Shows the AWS account with resources before cleanup.*

---

<p align="center">
  <img src="https://img.shields.io/badge/Section-Overview-blueviolet?style=for-the-badge"/>
</p>

## Overview

AWS Nuke is an open-source tool to delete all resources in an AWS account, restoring it to a clean state.  
[Full documentation →](https://github.com/rebuy-de/aws-nuke)

---

<p align="center">
  <img src="https://img.shields.io/badge/Section-Quick%20Links-blue?style=for-the-badge"/>
</p>

## Quick Links

- [AWS CLI Install/Update](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
- [AWS Nuke GitHub](https://github.com/rebuy-de/aws-nuke)
- [Cloud Nuke (Gruntwork)](https://github.com/gruntwork-io/cloud-nuke)
- [YouTube Guide Tutorial](https://youtu.be/odk_NuQNJTc?si=wypMlFZcLFyxkEd9)

---

<p align="center">
  <img src="https://img.shields.io/badge/Section-Prerequisites-9cf?style=for-the-badge"/>
</p>

## Prerequisites

- AWS CLI installed and configured  
- Admin access to your AWS account  
- AWS Nuke installed (`cloud-nuke` or `cloud-nuke.exe` for Windows)  

---

<p align="center">
  <img src="https://img.shields.io/badge/Section-Installation-success?style=for-the-badge"/>
</p>

## Installation

**1. Install or update AWS CLI**

```bash
aws --version
```
![AWS CLI Version](aws-v.png)  
*Verifies AWS CLI is installed and accessible.*

<br/>

**2. Configure AWS CLI**

```bash
aws configure
```
![AWS Configure](https://github.com/Subhajit-Chowdhury/Reset-AWS-with-Nuke/blob/main/aws%20config.png)  
*Configure your AWS credentials and default region.*

<br/>

**3. Install AWS Nuke**

- **macOS/Linux**:  
  ```bash
  brew install cloud-nuke
  ```
- **Windows**:  
  - Recommended:  
    ```bash
    winget install cloud-nuke
    ```
  - Or use the included `cloud-nuke.exe` in this repo:  
    - Download or copy `cloud-nuke.exe` to your working directory.  
    - Run commands as `cloud-nuke.exe ...`

---

<p align="center">
  <img src="https://img.shields.io/badge/Section-Usage-ff69b4?style=for-the-badge"/>
</p>

## Usage

**1. (Optional) List S3 Buckets**

```bash
aws s3 ls
```
![AWS S3 List](https://github.com/Subhajit-Chowdhury/Reset-AWS-with-Nuke/blob/main/aws%20test.png)  
*Displays all S3 buckets in your AWS account before cleanup.*

<br/>

**2. AWS Nuke Help**

```bash
cloud-nuke -h
```
![Cloud Nuke Help](https://github.com/Subhajit-Chowdhury/Reset-AWS-with-Nuke/blob/main/cloud-nuke%20--help.png)  
*Shows available commands and options for AWS Nuke.*

<br/>

**3. Inspect Resources (Preview what will be deleted)**

```bash
cloud-nuke inspect-aws --region ap-south-1
```
![Inspect AWS Resources](https://github.com/Subhajit-Chowdhury/Reset-AWS-with-Nuke/blob/main/cloud-nuke%20inspect.png)  
*Scans and lists all AWS resources in the specified region.*

![Inspect Result](https://github.com/Subhajit-Chowdhury/Reset-AWS-with-Nuke/blob/main/cloud-nuke%20inspect%20result.png)  
*Detailed output of resources found during inspection.*

<br/>

**Video: Inspect Command Demo**  
[![Watch the Inspect Command Demo](https://github.com/Subhajit-Chowdhury/Reset-AWS-with-Nuke/blob/main/nuke%20inpected%20resources.png)](screenshots/administrator-command-prompt-cloud-nuke-inspect-aws-2025-05-28-23-55-25.mp4)  
*Video walkthrough of the inspect command in action.*

<br/>

**4. (Optional) List Resource Types**

```bash
cloud-nuke aws --list-resource-types
```
![List Resource Types](https://github.com/Subhajit-Chowdhury/Reset-AWS-with-Nuke/blob/main/nuke%20inpected%20resources.png)  
*Lists all AWS resource types that can be deleted by AWS Nuke.*

<br/>

**5. (Recommended) Dry Run**

```bash
cloud-nuke aws --resource-type ec2 --dry-run
```
![Dry Run](https://github.com/Subhajit-Chowdhury/Reset-AWS-with-Nuke/blob/main/Dry%20Run.png)  
*Simulates the deletion process to preview what will be removed.*

<br/>

**6. Nuke All Resources**

```bash
cloud-nuke aws --region ap-south-1
```
![Nuke Confirmation](https://github.com/Subhajit-Chowdhury/Reset-AWS-with-Nuke/blob/main/aws%20nuke-%20confirm.png)  
*AWS Nuke asks for confirmation before deleting resources.*

![Final Nuke List](https://github.com/Subhajit-Chowdhury/Reset-AWS-with-Nuke/blob/main/final%20nuke%20list%20and%20confirmation.png)  
*Final list of resources to be deleted.*

![Confirming Nuke](https://github.com/Subhajit-Chowdhury/Reset-AWS-with-Nuke/blob/main/confirming%20nuke%20.png)  
*Confirmation step before proceeding with deletion.*

![Nuke Done](https://github.com/Subhajit-Chowdhury/Reset-AWS-with-Nuke/blob/main/nuke%20done%20.png)  
*AWS Nuke has finished deleting resources.*

![After Nuke Check](https://github.com/Subhajit-Chowdhury/Reset-AWS-with-Nuke/blob/main/After%20nuke%20check%20from%20cmd.png)  
*Verifies that all resources have been deleted after running AWS Nuke.*

---

<p align="center">
  <img src="https://img.shields.io/badge/Section-Security-critical?style=for-the-badge"/>
</p>

## Security

- Never commit AWS credentials to GitHub.
- Use IAM roles and temporary credentials.
- Remove sensitive info from screenshots.
- Add credential files to `.gitignore`.

[Security Best Practices →](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)

---

<p align="center">
  <img src="https://img.shields.io/badge/Section-Resources-blue?style=for-the-badge"/>
</p>

## Additional Resources

- [Cloud Nuke (Gruntwork)](https://github.com/gruntwork-io/cloud-nuke)
- [YouTube: AWS Nuke Guide](https://youtu.be/odk_NuQNJTc?si=wypMlFZcLFyxkEd9)

---

<p align="center">
  <img src="https://img.shields.io/badge/Section-Acknowledgments-lightgrey?style=for-the-badge"/>
</p>

## Acknowledgments

Special thanks to [Sami Banerjee](https://github.com/TryToLearnProgramming) ([Medium](https://medium.com/@er.samibanerjee) | [LinkedIn](https://www.linkedin.com/in/devops-engineer-samibanerjee/))  
for guidance and support in helping me discover and successfully use AWS Nuke to reset my AWS account.

---

<p align="center">
  <img src="https://img.shields.io/badge/Section-Reference%20Video-yellow?style=for-the-badge"/>
</p>

## Reference Video

The following YouTube video was instrumental in completing this project:  
[YouTube: AWS Nuke Guide](https://youtu.be/odk_NuQNJTc?si=wypMlFZcLFyxkEd9)

---

<p align="center">
  <img src="https://img.shields.io/badge/Built%20With-Love-red?style=for-the-badge"/>
</p>

## Built With Love

This project was created with ❤️ by **Subhajit Chowdhury**.

**Connect with me:**  
- [LinkedIn](https://www.linkedin.com/in/subhajitch0wdhury/)
- [GitHub](https://github.com/Subhajit-Chowdhury)
- Email: er.subhajitchowdhury@gmail.com

---

MIT License. See LICENSE file.

---

Thank you for visiting the **Nuke_AWS** project.  
Happy nuking! 💥
