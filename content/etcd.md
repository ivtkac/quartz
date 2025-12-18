---
title: etcd
created: 2025-12-18
tags:
  - k8s
aliases:
lang:
---
- distributed key-value store
- primary datastore of [[k8s]]
- stores and replicates all k8s states
- runs in high availability mode (3 of them):
	- requires a quorum for the following:
	- elect a new ETCD member
	- update the datastore