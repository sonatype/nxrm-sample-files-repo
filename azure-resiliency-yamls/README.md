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
1. [Storage Class YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/azure-resiliency-yamls/azure-resiliency-storage-class.yaml)
2. [Secrets YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/azure-resiliency-yamls/azure-resiliency-secrets.yaml) **or** [License Configuration Mapping YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/azure-resiliency-yamls/azure-resiliency-license-configuration-mapping.yaml)
3. [Logback Tasklogfile Override YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/azure-resiliency-yamls/azure-resiliency-nxrm-logback-tasklogfile-override.yaml)
4. [Local Persistent Volume YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/azure-resiliency-yamls/azure-resiliency-local-persistent-volume.yaml)
> **Note** You should not use Dynamic EBS Volume Provisioning as it will cause scheduling problems if EKS provisions the Nexus Repository pod and the EBS volume in different AZs. The EBS volume used must be the local volume attached as illustrated in the sample persistent volume YAML file. 

5. [Local Persistent Volume Claim YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/azure-resiliency-yamls/azure-resiliency-local-persistent-volume-claim.yaml)
> **Note** You should not use Dynamic EBS Volume Provisioning as it will cause scheduling problems if EKS provisions the Nexus Repository pod and the EBS volume in different AZs. The EBS volume used must be the local volume attached as illustrated in the sample persistent volume YAML file. 

6. [Kustomize Deployment YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/azure-resiliency-yamls/azure-resiliency-kustomize-deployment.yaml) **or** [Secrets Store CSI Driver Deployment YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/azure-resiliency-yamls/azure-resiliency-secrets-store-CSI-deployment.yaml)
7. [Services YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/azure-resiliency-yamls/azure-resiliency-services.yaml)
   * Optional - [Ingress for Docker](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/azure-resiliency-yamls/azure-resiliency-ingress-for-docker.yaml)
   * Optional - [Nodeport for Docker](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/azure-resiliency-yamls/azure-resiliency-nodeport-for-Docker.yaml)

> **Note** The resources created by these YAMLs are not in the default namespace.
