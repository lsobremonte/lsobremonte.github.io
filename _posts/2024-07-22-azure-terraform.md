---
title: Terraform
description: Deploy Infrastructure as Code (IaC)
date: 2024-07-22 15:00:00 -0600
categories: [Command-tool]
tags: [terraform, cmd, devops, azure]
image:
  path: /assets/images/covers/cover-terraform.png
  thumbnail: /assets/images/covers/cover-terraform.png
  alt: "Terraform - Deploy Infrastructure as Code (IaC)"
media_subpath: /assets/images/
---

## **What is Terraform ?**

Terraform is an open-source tool that lets you define and deploy Azure infrastructure using code for repeatable, automated provisioning.

---

# Terraform: Azure Quick Start

📘 [Official HashiCorp Guide](https://developer.hashicorp.com/terraform/tutorials/azure-get-started/azure-build)

Terraform is an open-source tool that lets you define and deploy Azure infrastructure using code for repeatable, automated provisioning.

---

## **✅ Step 1: Install Terraform (macOS)**

```bash
brew tap hashicorp/tap
brew install hashicorp/tap/terraform
```

---

## ** Step 2: Authenticate with Azure**

### A. Login to Azure

```bash
# List available subscriptions
az account list --output table

# Login using your Azure tenant ID
az login --tenant "<tenant_id>"

# Set the active subscription
az account set --subscription "<subscription_id>"

# Verify your current subscription context
az account show -o json
```

---

## **🧾 Step 3: Create & Assign Service Principal**

### A. Create a Service Principal

> ⚠️ **Important:** Document the generated secret immediately.

```bash
az ad sp create-for-rbac \
  --name "sp-terraform" \
  --role="Contributor" \
  --scopes="/subscriptions/<subscription_id>"
```

### B. Set Environment Variables

```bash
export ARM_CLIENT_ID="<APPID_VALUE>"
export ARM_CLIENT_SECRET="<PASSWORD_VALUE>"
export ARM_TENANT_ID="<TENANT_ID>"
export ARM_SUBSCRIPTION_ID="<SUBSCRIPTION_ID>"
```

---

## ** Step 4: Grant Management Group Permissions (Optional for Policy)**

### A. Check Current Role Assignment

```bash
az role assignment list \
  --assignee "<sp-app-id>" \
  --scope "/providers/Microsoft.Management/managementGroups/PROD"
```

### B. Assign Role for Policy Management

> 🎯 Grants access to manage Azure Policies at the management group level.

```bash
az role assignment create \
  --assignee "<sp-app-id>" \
  --role "Resource Policy Contributor" \
  --scope "/providers/Microsoft.Management/managementGroups/PROD"
```

---

## ** Step 5: View Custom Policies (Optional)**

```bash
az policy definition list \
  --management-group PROD \
  --query "[?policyType=='Custom'].{Name:name, DisplayName:displayName}" \
  -o table
```

---

## ** Step 6: Core Terraform Commands**

| Command                         | Description                                                             |
| ------------------------------- | ----------------------------------------------------------------------- |
| `terraform init`                | Initialize the working directory (downloads providers, sets up backend) |
| `terraform plan`                | Preview changes Terraform will make to match the desired state          |
| `terraform apply`               | Apply the planned changes (with confirmation prompt)                    |
| `terraform apply -auto-approve` | Apply changes **without** a prompt (use with caution)                   |
| `terraform destroy`             | Destroy all resources managed by Terraform                              |

---

### **Basic Commands**

| Purpose           | Command               |
| ----------------- | --------------------- |
| Check version     | `terraform version`   |
| Format config     | `terraform fmt`       |
| Validate syntax   | `terraform validate`  |
| Inspect providers | `terraform providers` |

---

### **Execution (Plan & Apply)**

| Purpose                 | Command                              |
| ----------------------- | ------------------------------------ |
| Preview changes         | `terraform plan`                     |
| Save plan to file       | `terraform plan -out=<file>`         |
| Apply changes           | `terraform apply`                    |
| Apply saved plan        | `terraform apply <file>`             |
| Apply specific resource | `terraform apply -target=<resource>` |
| Pass inline variable    | `terraform apply -var='key=value'`   |
| Plan for destruction    | `terraform plan -destroy`            |

---

### **State Management**

| Purpose            | Command                           |
| ------------------ | --------------------------------- |
| Show current state | `terraform show`                  |
| List all resources | `terraform state list`            |
| Show one resource  | `terraform state show <resource>` |

---

### **Optional Directory Context**

Use `-chdir=<path>` if working outside the current directory:

`terraform -chdir=./path plan`
