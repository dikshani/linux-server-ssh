# Linux Server SSH Setup

## Objective

Setup a remote Linux server and configure SSH access using two SSH key pairs.

## Server Details

Provider: AWS
OS: Ubuntu

## Steps Performed

### 1. Created Remote Server

Created Ubuntu Linux server and noted public IP.

### 2. Generated SSH Keys

Generated two SSH key pairs locally:

```bash
ssh-keygen -t rsa -b 4096 -f ~/.ssh/server_key_1
ssh-keygen -t rsa -b 4096 -f ~/.ssh/server_key_2
```

Generated:

```text
server_key_1
server_key_1.pub
server_key_2
server_key_2.pub
```

### 3. Added Public Keys to Server

Connected to server and added public keys:

```bash
vim ~/.ssh/authorized_keys
```

Updated permissions:

```bash
chmod 700 ~/.ssh
chmod 600 ~/.ssh/authorized_keys
```

### 4. Verified SSH Access

Connected using:

```bash
ssh -i ~/.ssh/server_key_1 ubuntu@SERVER_IP
```

and

```bash
ssh -i ~/.ssh/server_key_2 ubuntu@SERVER_IP
```


Connected using:

```bash
ssh nginx-diksha
```

## Project URL

https://roadmap.sh/projects/ssh-remote-server-setup
