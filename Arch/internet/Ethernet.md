

> Arch linux ethernet fixing (usually after installation)

# Only if you use `systemd-networkd`

- `systemctl status systemd-networkd`
- `ip a`
- `networkctl status <your_interface>`, interface like: `enp2s0`. If it says config: unmanaged — that means no matching .network file exists
- Create or check /etc/systemd/network/<your_interface>.network

```toml
[Match]
Name=<your_interface> # example: enp2s0

[Network]
DHCP=yes
```

- `sudo systemctl restart systemd-networkd`
- `networkctl status enp2s0`
- `ip a`