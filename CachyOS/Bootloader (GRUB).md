
- Enable Windows detection in GRUB

```bash
sudo vim /etc/default/grub
```

- Remove comment from

```toml
GRUB_DISABLE_OS_PROBER=false
```

- regenerate GRUB config

```bash
sudo grub-mkconfig -o /boot/grub/grub.cfg
```

- Reboot