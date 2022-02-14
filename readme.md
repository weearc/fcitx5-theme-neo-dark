# Neo dark

A simple theme for fcitx5 better used under system-wide light theme.

## Screenshot

- InputMethod Change Content</br>
![image-20220215000122203](/home/ddqi/git/fcitx5-skin/neo-dark/screenshot/input.png)</br>

- Wide Panel Horizontal</br>
![Content](screenshot/h.png)</br>

- Thin Panel Horizontal</br>
![horizontal](screenshot/h2.png)<br>

## Install
### Fcitx5
For Arch Linux users:</br>
Try out fcitx5 by using the following command:
```bash
yay -S fcitx5-git fcitx5-qt5-git fcitx5-gtk-git fcitx5-chinese-addons-git
```
If you have added the `Arch Linux CN Repo`, please install directly from archlinuxcn.</br>

Then add the following lines:
- xorg: to `~/.xprofile`

```bash
export GTK_IM_MODULE=fcitx5
export XMODIFIERS="@im=fcitx"
export QT_IM_MODULE=fcitx5
fcitx5 > /dev/null &
```

- wayland: to `~/.pam_environment`

```bash
GTK_IM_MODULE DEFAULT=fcitx5
QT_IM_MODULE DEFAULT=fcitx5
XMODIFIERS DEFAULT=@im=fcitx5
```
Also, you should add the following lines to `~/.config/fcitx5/profile`:
```
[Groups/0]
# Group Name
Name=Default
# Layout
Default Layout=us
# Default Input Method
DefaultIM=pinyin

[Groups/0/Items/0]
# Name
Name=keyboard-us
# Layout
Layout=

[Groups/0/Items/1]
# Name
Name=pinyin
# Layout
Layout=

[GroupOrder]
0=Default
```

If you want to change settings in kde system settings, you should install package `fcitx5-kcm-git`.

### Fcitx5-skin-simple-blue
First, clone the repo to `~/.local/shre/fcitx5/themes/`

```bash
git clone https://github.com/weearc/fcitx5-theme-neo-dark  ~/.local/share/fcitx5/themes/neo-dark
```

Add the following to your `~/.config/fcitx5/conf/classicui.conf`

```ini
# True, if you want a vertical candidate list
Vertical Candidate List=False
Theme=neo-dark
```

Your may choose wide or thin panel with the combination for ` input_panel.png & theme-wide.conf` or `input_panel-thin.png & theme-thin.conf` and rename them to `input_panel.png ` and `theme.conf`.</br>

Also better use `one-line` mode for the theme and don't use vertical input.</br>

**Every time you change the settings please reload fcitx5**

Thanks to the help of Csslayer and oldherl from Archlinux CN.


## License

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or distribute this software, either in source code form or as a compiled binary, for any purpose, commercial or non-commercial, and by any means.
