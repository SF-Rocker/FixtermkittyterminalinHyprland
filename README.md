# FixtermkittyterminalinHyprland
lets you use kitty terminal to open nano files in kitty through another bash or non zsh system configuration via ssh.

# Instructions

# On your local machine:
infocmp > xterm-kitty.terminfo
``` scp xterm-kitty.terminfo user@remote-ip:~ ```
# Don't forget to cd into home/user to find that terminfo file we need to send it system-wide with su privileges.
# Don't remove the :~ from the ip address, it will not know where to send it, to verify it worked you will be prompted the password for the ssh transfer twice.

# On the remote machine:
tic -x xterm-kitty.terminfo
```sudo mkdir -p /usr/share/terminfo/x
sudo tic -x -o /usr/share/terminfo xterm-kitty.terminfo
```


--------------------------------------------------------
# For Ubuntu, Debian, ARCH, Manjaro, EndeavorOS, etc.
``` sudo apt install kitty-terminfo ```   # Debian/Ubuntu
``` sudo pacman -S kitty-terminfo ```    # Arch

or Option 2 havn't tried it but may work but will break kitty functionality.
``` export TERM=xterm-256color ```

