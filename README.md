# GPU Rental Guide

After following this guide, you will learn how to rent GPUs on Vast.AI for your specific node requirements and connect them to your computer

## Table of Contents

1. [Description](#description)
2. [Creating a Vast.AI Account](#creating-a-vastai-account)
3. [SSH Key Setup Guide](#ssh-key-setup-guide)
4. [Adding SSH Key to Vast.AI](#adding-ssh-key-to-vastai)
5. [Selecting the Right Instance](#selecting-the-right-instance)
6. [Connecting to Your Instance](#connecting-to-your-instance)
7. [Terminating Your Instance](#terminating-your-instance)

## Description

Different blockchain projects require different hardware specifications and operating systems. This guide will walk you through selecting the right instance (remote computer) for your node

I'll be demonstrating with Vast.AI as it's more affordable and accepts cryptocurrency payments, but these principles apply to any cloud GPU provider. Throughout this guide, "instance" refers to the remote computer you'll be renting

## Creating a Vast.AI Account

1. Visit [Vast.ai](https://cloud.vast.ai/) and create an account
2. Navigate to the billing section and click "Add Credit" to choose your preferred payment method
3. Once you've added credit, you can rent an instance. First, you'll need to generate an SSH key to connect the instance to your computer

## SSH Key Setup Guide

To generate an SSH key, open **Windows PowerShell** and run:
```powershell
ssh-keygen -t ed25519
```

- Press `Enter` to confirm the default location
- Press `Enter` again (leave passphrase empty for simplicity - this generates the keys)
- Copy the path to your keys and open the public key file in Notepad:
```powershell
notepad Public_Key_Path
```

### SSH Key Generation Example
<img width="1281" height="732" alt="SSH Key Generation" src="https://github.com/user-attachments/assets/f236bf0a-3a1e-4aba-9fc3-fc7bcb530d6d" />

## Adding SSH Key to Vast.AI

- Copy the entire public key content from the Notepad file
- In Vast.AI, navigate to the SSH Keys section
- Click "Add New" and paste your public key

### Adding SSH Key Interface
<img width="1666" height="770" alt="Adding SSH Key" src="https://github.com/user-attachments/assets/6aa3177b-f9c9-47e5-901a-7059c3987abe" />

## Selecting the Right Instance

Every cryptocurrency node has specific hardware requirements:

**Key Specifications to Consider:**
- **GPU**: Graphics processing power
- **RAM**: System memory
- **Storage**: Disk space (preferably SSD)
- **Bandwidth**: Upload and download speeds
- **Operating System**: Click "Change Template" to select the appropriate OS for your node (e.g., Ubuntu, PyTorch, etc.)

### Choose based on your node requirements and budget
<img width="1390" height="334" alt="Instance Selection" src="https://github.com/user-attachments/assets/e0ca2253-78c5-4a6f-9f24-d22f425d2be8" />

## Connecting to Your Instance

1. After configuring your instance specifications, click "Rent" to deploy it
2. Go to your "Instances" dashboard - your instance will be activated within a few minutes
3. Once activated, click "Connect" and copy the SSH command

### Instance Connection Interface
<img width="1920" height="911" alt="Instance Connection" src="https://github.com/user-attachments/assets/18deb9e6-0fb7-4802-9da5-fbe0e1ad9625" />

4. Paste the SSH command into PowerShell and press Enter
5. Write ``yes`` and `Enter` to add to the list of known hosts
6. It will ask for Passpharse, Just ``Enter`` again
7. You'll see a connection confirmation, indicating successful access to your remote instance
### Connection confirmation
   <img width="1113" height="626" alt="image" src="https://github.com/user-attachments/assets/9c09a1d5-b735-4234-8926-4b6b0eca4883" />

   
   

## Terminating Your Instance

When you're finished with your instance:
- Click the recycle bin (destroy) button in your Vast.AI dashboard
- This immediately stops billing and destroys the instance

**Important:** Make sure to save any important work before destroying the instance, as all data will be permanently lost

**That's how you can rent instance and run node, after running node you can then terminate the instance to stop billing**

---

*Hope this guide was helpful! If you found it useful, please follow me on X and GitHub*
