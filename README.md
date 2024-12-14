
---

# Project Title

A brief description of what this project does and its purpose.

---

## SSH Access Methods

This repository contains methods to access the server via SSH.

### Method 1: Using Public Key

To copy your SSH public key to the instance, run the following command:

```bash
ssh-copy-id -f "-o IdentityFile <PATH TO PEM FILE>" ubuntu@<INSTANCE-PUBLIC-IP>
```

**Note**: Replace `<PATH TO PEM FILE>` with the path to your PEM file, and `<INSTANCE-PUBLIC-IP>` with the public IP address of your instance.

### Method 2: Enabling Password Authentication

1. Open the SSH configuration file:

    ```bash
    sudo nano /etc/ssh/sshd_config.d/60-cloudimg-settings.conf
    ```

2. Update the following line to enable password authentication:

    ```bash
    PasswordAuthentication yes
    ```

3. Restart the SSH service to apply the changes:

    ```bash
    sudo systemctl restart ssh
    ```

---




---

