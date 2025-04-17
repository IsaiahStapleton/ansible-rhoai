# Ansible RHOAI

## Purpose

The purpose of this repo is to be able to automate the installation and configuration of all the components required to do model serving and run AI workloads on Red Hat OpenShift AI.  


## How to Use

There are different playbooks, the two that are used are:
- **deploy-everything:** Will install and deploy everything needed for doing model serving and running AI workloads in the cluster.
- **uninstall-everything:** Uninstalls everything that was installed and deployed in the deploy-everything playbook.

### Prerequisites

You will need to have the `kubernetes` and `ansible` packages installed. You can do this by running the following command from the root directory:

```
pip install -r requirements.txt
```

### deploy-everything

Navigate to `ansible-rhoai/kustomize/cluster-scope/overlays/albany` and run the following command:

```
ansible-playbook playbooks/deploy-everything.yaml
```

### uninstall-everything

Navigate to `ansible-rhoai/kustomize/cluster-scope/overlays/albany` and run the following command:

```
ansible-playbook playbooks/uninstall-everything.yaml
```