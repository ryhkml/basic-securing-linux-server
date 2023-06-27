### Make a backup of crowdsec defaults config

```bash
sudo cp /etc/crowdsec/config.yaml /etc/crowdsec/config-BACKUP.yaml
sudo cp /etc/crowdsec/profiles.yaml /etc/crowdsec/profiles-BACKUP.yaml
```

then, add new config `use_wal: true` in `/etc/crowdsec/config.yaml`

```yaml
...
...
db_config:
  use_wal: true
  ...
...
...
```

### Edit Ban Duration (optional)

file config in `/etc/crowdsec/profiles.yaml`

```yaml
...
...
decisions:
  - type: ban
    # Default is 4 hours
    duration: 4h
...
...
```

after some changes

```bash
sudo systemctl restart crowdsec
```