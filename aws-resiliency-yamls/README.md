Copyright Sonatype, Inc., 2022, All Rights Reserved.

# Overview
You can use the sample YAML files in this section to help set up the YAMLs you will need for a resilient deployment. 
Ensure you have filled out the YAML files with appropriate information for your deployment.

> **Note** The YAML files in this section are just examples and cannot be copy-pasted and used as-is. You must fill them out with the appropriate information for your deployment to be able to use them.

# YAML Order

1. [Namespaces YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/aws-resiliency-yamls/aws-resiliency-namespaces.yaml)

2. [Storage Class YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/aws-resiliency-yamls/aws-resiliency-storage-class.yaml)

3. [Secrets YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/aws-resiliency-yamls/aws-resiliency-secrets.yaml)

4. [Fluent-bit YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/aws-resiliency-yamls/aws-resiliency-fluent-bit.yaml) (only required if using CloudWatch)

5. [Logback Tasklogfile Override YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/aws-resiliency-yamls/aws-resiliency-nxrm-logback-tasklogfile-override.yaml)

6. [Services YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/aws-resiliency-yamls/aws-resiliency-services.yaml)
   * Optional - [Ingress for Docker YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/aws-resiliency-yamls/aws-resiliency-ingress-for-docker-connector.yaml)
   * Optional - [Service for Docker YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/aws-resiliency-yamls/aws-resiliency-docker-services.yaml)

7. [Ingress YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/aws-resiliency-yamls/aws-resiliency-ingress.yaml)

8. [Service Accounts YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/aws-resiliency-yamls/aws-resiliency-service-accounts.yaml)

9. [StatefulSet YAML](https://github.com/sonatype/nxrm-sample-files-repo/blob/main/aws-resiliency-yamls/aws-resiliency-statefulset.yaml)

> **Note** The resources created by these YAMLs are not in the default namespace.
