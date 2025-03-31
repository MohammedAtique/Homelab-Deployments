# HomeLab Docker GitOps Deployment

This repository is designed to streamline the deployment and management of Docker containers in a HomeLab environment using GitOps principles. It provides a collection of Docker-based configurations and scripts, enabling automation and version control for containerized applications. The repository integrates seamlessly with GitOps tools, allowing for continuous deployment directly from the Git repository.

## Features

- Docker-based configurations for various applications and services.
- GitOps-powered automation and version control for deployments.
- Seamless integration with GitOps tools for continuous deployment.
- Simple process for managing and scaling containerized applications in a HomeLab.

## Repository Structure

The `template-branch`, serves as the source for new branches. The main configurations and templates are located in the root of the branches.

## Getting Started

To start using this repository, follow the steps below:

### 1. Clone the Repository

To clone the repository, run the following command:

```bash
git clone https://gitea.luffylab.com/luffylab03/homelab.git
cd homelab
```
### 2. Create a New Branch

To create a new branch for your HomeLab containerized application, use the `Template-Branch` as the source. The naming convention for the branch is as follows:

```yaml
servername-VMname-servicename
```

For example: `node1-proxy-nginx`


To create a new branch, use the following commands:

```bash
git checkout template-branch
git checkout -b servername-VMname-servicename
```

### 3. Make Changes and Commit

Once you've created your new branch, you can modify or add Docker configurations, scripts, or services as needed. After making changes, commit them to your branch:

1. Stage the changes:

    ```bash
    git add .
    ```

2. Commit your changes with a descriptive message:

    ```bash
    git commit -m "Your commit message"
    ```

### 4. Push Your Branch

Push the newly created branch to the remote repository:

```bash
git push origin servername-VMname-servicename
```

### 5. Set Up Continuous Deployment

After pushing your branch, you can integrate with `Komodo` to set up continuous deployment. This ensures that any changes you make in the repository automatically trigger deployments.

#### Steps to Set Up Continuous Deployment:

1. **Choose a GitOps Tool**:  
   We are using [Komodo](https://komo.do/docs/intro) for GitOps Operations.

2. **Configure the Tool to Watch Your Repository**:  
   Set up your GitOps tool to monitor the repository for changes in branches. Each time a commit is pushed to a branch, the GitOps tool will automatically trigger the deployment process for that branch.
   [Setup Webook in Komodo](https://komo.do/docs/webhooks)

3. **Test Deployment**:  
   Once everything is set up, test the deployment by making a small change in your branch and pushing it. Verify that the GitOps tool picks up the change and deploys it as expected.

By setting up continuous deployment, your changes will be automatically deployed based on the configuration in the repository, making the process faster and more efficient.

## Template Branch

The `template-branch` is just an orphan git branch used to make new branches.

```bash
git checkout --orphan=template-branch
```

## Contributing

If you'd like to contribute to this repository:

1. Fork the repository.
2. Create a new branch from the `template-branch`.
3. Make your changes and commit them.
4. Push your branch to your forked repository.
5. Submit a pull request to the main repository.

Please ensure that your branch follows the naming convention: `servername-VMname-servicename`.



**THIS REPOSITORY IS ENCRYPTED. IF YOU’RE HERE, YOU’RE EITHER VERY BRAVE OR VERY LOST. EITHER WAY, GOOD LUCK!**
