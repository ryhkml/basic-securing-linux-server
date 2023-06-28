### Make a backup of ntp defaults config

```bash
sudo cp /etc/ntp.conf /etc/ntp.conf-BACKUP
```

then, commenting out all server directives and add new server directives in `/etc/ntp.conf`

```text
...
...
# You do need to talk to an NTP server or two (or three).
#server ntp.your-provider.example

# pool.ntp.org maps to about 1000 low-stratum NTP servers.  Your server will
# pick a different set every time it starts up.  Please consider joining the
# pool: <http://www.pool.ntp.org/join.html>
#pool 0.debian.pool.ntp.org iburst
#pool 1.debian.pool.ntp.org iburst
#pool 2.debian.pool.ntp.org iburst
#pool 3.debian.pool.ntp.org iburst
...
...
# Add new directives at the bottom
pool pool.ntp.org iburst
```

after some changes

```bash
sudo systemctl restart ntp
```