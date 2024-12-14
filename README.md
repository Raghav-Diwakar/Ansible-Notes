---

# SSH Access Methods

## Method 1: Using Public Key

To copy your SSH public key to the instance, run the following command:

```bash
ssh-copy-id -f "-o IdentityFile <PATH TO PEM FILE>" ubuntu@<INSTANCE-PUBLIC-IP>
```

## Method 2: Enabling Password Authentication

1. Open the file `/etc/ssh/sshd_config.d/60-cloudimg-settings.conf`
2. Update the following line:

```bash
PasswordAuthentication yes
```

3. Restart SSH:

```bash
sudo systemctl restart ssh
```

---


