Copyright Sonatype, Inc., 2022, All Rights Reserved.

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
1. [Persistent Volume YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/on-prem-resiliency-yamls/on-prem-resiliency-nfs-persistent-volume.yaml)
2. [Persistent Volume Claim YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/on-prem-resiliency-yamls/on-prem-resiliency-nfs-persistent-volume-claim.yaml)
3. [License Configuration Mapping YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/on-prem-resiliency-yamls/on-prem-resiliency-license-config-mapping.yaml)
4. [Deployment YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/on-prem-resiliency-yamls/on-prem-resiliency-deployment.yaml)
5. [Services YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/on-prem-resiliency-yamls/on-prem-resiliency-services.yaml)
   * Optional - [Ingress for Docker YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/on-prem-resiliency-yamls/on-prem-resiliency-ingress-for-docker-connector.yaml)
   * Optional - [Nodeport for Docker YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/on-prem-resiliency-yamls/on-prem-resiliency-nodeport-for-docker-connector.yaml)
   
> **Note** The resources created by these YAMLs are not in the default namespace.
