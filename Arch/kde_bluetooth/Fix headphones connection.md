- Ensure that they're installed

```bash
sudo pacman -S --needed pipewire pipewire-alsa pipewire-pulse wireplumber bluez bluez-utils
```

```bash
sudo vim /etc/bluetooth/main.conf
```

- Ensure these lines exist and are NOT commented:

```
[General]
Enable=Source,Sink,Media,Socket
```

- (Optional, but helps TWS):

```
ControllerMode=dual
FastConnectable=true
```

- Restart everything (order matters)

```bash
sudo systemctl restart bluetooth
systemctl --user restart pipewire wireplumber
```

- Inside `bluetoothctl` (CLI tool)

```bash
remove <mac_address_of_device>
power off
power on
agent on
default-agent
scan on
pair <mac_address_of_device>
trust <mac_address_of_device>
```

- wait for 5-10 seconds, after that connect
