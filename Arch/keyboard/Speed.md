
1. For Xorg WMs

```bash
echo 'xset r rate 250 40' >> ~/.xprofile
```

2. For Hyprland

```bash
input {
    kb_layout = us,ru # languages
    kb_variant =
    kb_model =
    kb_options = grp:alt_shift_toggle # change layout with `alt + shift`
    kb_rules =
    
    follow_mouse = 1
    
    sensitivity = 0 # -1.0 - 1.0, 0 means no modification.
    
    repeat_delay = 250
    repeat_rate = 40
    
    touchpad {
        natural_scroll = false
    }
}
```
