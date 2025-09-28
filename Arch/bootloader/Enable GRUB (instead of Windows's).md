
1. Run command: `efibootmgr`

- Output will be something like this:

```bash
Boot0000* Windows Boot Manager
Boot0001* GRUB
```

2. change boot order

```bash
sudo efibootmgr -o 0001,0000
```

3. Install `os-prober`

```bash
sudo pacman -S os-prober
```

4. Open a file

`sudo vim /etc/default/grub`

5. Uncomment a line `GRUB_DISABLE_OS_PROBER=false`
6. Regenerate GRUB configuration

```bash
sudo grub-mkconfig -o /boot/grub/grub.cfg
```

- You should see something like

```bash
Found Windows Boot Manager on /dev/sdX
```

7. Reboot