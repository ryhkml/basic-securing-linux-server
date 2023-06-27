#### Setting up default policies

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

#### Allowing SSH connections
```bash
sudo ufw limit in ssh comment 'Allow SSH connections limit in'
```

or

```bash
sudo ufw limit in <CUSTOM_SSH_PORT>/tcp comment 'Allow SSH connections limit in'
```

#### Allowing other connections (optional)

```text
sudo ufw allow http
sudo ufw allow https
sudo ufw allow 10000/tcp
sudo ufw allow 10000/udp
sudo ufw allow 10000:11000/tcp
sudo ufw allow from <IP or SUBNETS>
sudo ufw allow from <IP or SUBNETS> to any port <PORT>
```

#### Enabling UFW

```bash
sudo ufw enable
```