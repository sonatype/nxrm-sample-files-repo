# Overview
You can use the sample YAML files in this section to help set up the YAMLs you will need for a resilient deployment. 
Ensure you have filled out the YAML files with appropriate information for your deployment.

> **Note** The YAML files in this section are just examples and cannot be copy-pasted and used as-is. You must fill them out with the appropriate information for your deployment to be able to use them.

# Create Namespace
Before running the YAML files in this section, you must first create a namespace. 
To create a namespace, use a command like the following with the kubectl command-line tool:
```kubectl create namespace <namespace>```

# YAML Order
After creating the namespace, **you must run your YAML files in the order below:**
1. [Storage Class YAML]
2. [Secrets YAML] **or** [License Configuration Mapping YAML]
3. [Logback Tasklogfile Override YAML]
4. [Local Persistent Volume YAML]
5. [Local Persistent Volume Claim YAML]
6. [Kustomize Deployment YAML] **or** [Secrets Store CSI Driver Deployment YAML]
7. [Services YAML]
  * Optional - [Ingress for Docker]
  * Optional - [Nodeport for Docker]
