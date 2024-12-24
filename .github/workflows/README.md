
# Project Name

![License](https://img.shields.io/badge/license-MIT-green)
![Build Status](https://img.shields.io/github/actions/workflow/status/your-repo-name/your-workflow.yml)

## 📖 Description
Provide a brief overview of your project or action.  
**Example**:  
"This is a GitHub composite action t# Keyfactor Container Signing  using Composit Action

## Description

*This is the fork of existing container signing pricess.* If you want to know more about the process detailed information can be found [here]().

This is a reusable composite action that facilitates the process of container signing using the Keyfactor Container Signing service. It allows teams to easily integrate and automate the signing of container images within their CI/CD pipelines, ensuring secure and trusted container deployment. By leveraging this composite action, users can ensure that their container images are signed and verified, meeting security and compliance requirements.

---


## Features
- *Automated Container Signing*: Streamline container image security.
- *CI/CD Integration*: Easy to integrate into GitHub workflows.
- *Reusability*: Designed for use across multiple repositories.

---

## Purpose and Usability:
The `Keyfactor Container Signing` process ensures that your container images are `cryptographically signed`, providing confidence in the authenticity and integrity of the images being deployed. This composite action simplifies the integration of container signing into your workflows, enabling teams to focus on their core development tasks while ensuring that security best practices are followed.

This composite action is designed to be easily reusable across multiple projects or teams within organization. It integrates seamlessly with existing CI/CD systems, and automates the signing process with minimal setup.

---

## These are the variables that :
*Note: All inputs mentioned below we necessary for this action to work*
| Input Name              | Description|
|-------------------------|-------------------------------------------------------------------------------------------------------|
| `image_name`                 | The name of the container image that you want to sign (e.g., `your-image-name:latest`).              |
| `repo`| This is the repository name where the build file is |
|  `password`| This is the access which required to login into   |
| `SIGNUM_CLIENTID` | Signum client id| 
| `SIGNUM_PASSWORD` | Signum password|


---





## Example 
1. *Include in Your Workflow*:  
   Add the following YAML to your workflow:

   ```yaml
   "Keyfactor_Signum":
    runs-on: ubuntu-latest-2-8 #use any runner of your choice
    steps:
    - name: "Container Signing"
      uses: Repository url to the action
      with:
             image_name: "image name of the signed container"
             repo: "ghcr.io"
             SIGNUM_CLIENTID: ${{ secrets.SIGNUM_CLIENTID }}
             SIGNUM_PASSWORD: ${{ secrets.SIGNUM_PASSWORD }}
             password: ${{ secrets.KEY }}

             
             

o facilitate secure container signing using Keyfactor services."

---

## 🚀 Features
- **Automated Container Signing**: Streamline container image security.
- **CI/CD Integration**: Easy to integrate into GitHub workflows.
- **Reusability**: Designed for use across multiple repositories.

---

## 🛠️ Usage
1. **Include in Your Workflow**:  
   Add the following YAML to your workflow:

   ```yaml
   name: Keyfactor Container Signing

   on:
     push:
       branches:
         - main

   jobs:
     sign-container:
       runs-on: ubuntu-latest
       steps:
         - name: Checkout Repository
           uses: actions/checkout@v3

         - name: Keyfactor Signing
           uses: your-org/your-action@v1
           with:
             image_name: "your-image-name:tag"
             SIGNUM_CLIENTID: ${{ secrets.SIGNUM_CLIENTID }}
             SIGNUM_PASSWORD: ${{ secrets.SIGNUM_PASSWORD }}
