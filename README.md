Here’s a well-structured and professional Git README template based on your request:

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

## Installation

1. Step 1 for installing the project.
2. Step 2 for installing the project.
3. Step 3 for installation.

---

## Usage

Provide instructions and examples for using the project.

---

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-name`).
5. Create a new Pull Request.

---

## License

Include your license information here.

---

