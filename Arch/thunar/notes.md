
- For image preview, install `sudo pacman -S tumbler`
- For image view, install `yay -S qView`
- Default viewer for all images with `qView`:
	- Find out, the desktop file name: `ls /usr/share/applications | grep -i qview`, the result will be something like this: `com.interversehq.qView.desktop`
	- set `qView` as a default image types:

```bash
xdg-mime default com.interversehq.qView.desktop image/png
xdg-mime default com.interversehq.qView.desktop image/jpeg
xdg-mime default com.interversehq.qView.desktop image/webp
xdg-mime default com.interversehq.qView.desktop image/gif
xdg-mime default com.interversehq.qView.desktop image/bmp
xdg-mime default com.interversehq.qView.desktop image/tiff
```
