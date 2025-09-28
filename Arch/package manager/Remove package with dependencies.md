
## 1. yay

```bash
yay -Rns <package_name>
```

Explanation:

	-R → remove package
	-n → remove config files (backup and install reason info)
	-s → also remove dependencies that are not required by other packages

> If you want to check if unused dependencies remain in your system after removals

```bash
yay -Yc
```

## 2. pacman

```bash
sudo pacman -Rns <package_name>
```

> To clean up **all orphaned packages** system-wide (not just those tied to the one you removed)

```bash
sudo pacman -Rns $(pacman -Qtdq)
```

