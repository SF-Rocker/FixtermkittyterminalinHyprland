# FixtermkittyterminalinHyprland
lets you use kitty terminal to open nano files in kitty.

# Instructions

```# On your local machine:
infocmp > xterm-kitty.terminfo
scp xterm-kitty.terminfo user@remote-ip:~

# On the remote machine:
tic -x xterm-kitty.terminfo
sudo mkdir -p /usr/share/terminfo/x
sudo tic -x -o /usr/share/terminfo xterm-kitty.terminfo
```

