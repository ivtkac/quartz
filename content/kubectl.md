---
title: kubectl
created: 2025-12-18
tags:
  - man
  - k8s
aliases:
lang:
links:
  - "[[man]]"
---
- [[CLI]] for [[k8s]] clusters
- **kubeconfig file**
	- allows kubectl to find and access a K8s cluster

```yml
apiVersion: v1
clusters:
- cluster:
  certificate-authority: fake-ca-file
  server: https://1.2.3.4
contexts:
- context:
   cluster: development
   namespace: frontend
   user: developer
  name: dev-frontend 
current-context: dev-frontend
kind: Config
prefrences: {}
users:
- name: developer
  user:
    client-certificate: fake-cert-file
    client-key: fake-key-file
```