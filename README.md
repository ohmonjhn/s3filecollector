# s3filecollector.py

`s3filecollector.py` is a Python script designed to securely and easily download files with a specific extension from a specified folder within an AWS S3 bucket to your local computer. 

## How It Works

This script will look inside a specific folder in an S3 bucket and download all files with the extension you choose (like `.csv`, `.txt`, etc.) to a folder on your computer. It works by going through all the subfolders inside the folder you specify and finding the files you want.

**Important:** S3 paths are case-sensitive. This means that if your folder name is `Reports`, but you specify `reports`, the script will not find the files.

## Requirements

Before you start, make sure you have:

1. **Python 3.6 or Higher**: You need Python 3.6 or higher installed on your computer.

2. **AWS CLI Installed and Configured**: If you haven't already, install the AWS CLI. This tool lets your computer talk to AWS.

   - **Install AWS CLI**:

     On macOS, you can install it with Homebrew:

     ```bash
     brew install awscli
     ```

     On Windows, follow the official [AWS CLI Installation Guide](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html).

   - **Configure AWS CLI**:

     After installing, set it up by entering your AWS credentials:

     ```bash
     aws configure
     ```

3. **Boto3 Library Installed**: This script uses Boto3 to interact with AWS. You can install it by running:

   ```bash
   pip install boto3
