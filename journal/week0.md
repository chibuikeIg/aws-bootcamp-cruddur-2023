# Week 0 — Billing and Architecture

## Tasks Completed In Week 0

1. Create New Repository From Template
    - Template to create repository from [Repo Template](https://github.com/ExamProCo/aws-bootcamp-cruddur-2023)

2. Login to your aws console and create IAM user and grant administrator permission. Generate Access & Secret key. 

3. Install AWS CLI on gitpod workspace.
   - Installation [Guide]()
        `curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
        unzip awscliv2.zip
        sudo ./aws/install`

4. Configure Gitpod Workspace
Configure gitpod workspace/environment to automatically bootstrap AWS CLI and project configuration during launch.
    - Configuration guide:
        `tasks:
            - name: aws-cli
              env:
                AWS_CLI_AUTO_PROMPT: on-partial
              init: |
                cd /workspace
                curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
                unzip awscliv2.zip
                sudo ./aws/install
                cd $THEIA_WORKSPACE_ROOT`

