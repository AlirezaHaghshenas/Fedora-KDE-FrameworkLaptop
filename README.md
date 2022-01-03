# Fedora-KDE-FrameworkLaptop
This is a personal note for setting up Fedora and KDE on the Framework Laptop

# Before formatting
1. Backup:
   1. Secrets (backup these in an encrypted storage):
      1. `~/.ssh` folder
      1. gpg key(s) `~/.gnupg`
      1. Dotnet secrets folder
      1. Passwords in: Firefox, Brave, Opera, Chromium, Chrome
      1. kubernetes config
      1. Crypto wallet phrase(s)
   1. Also backup as encrypted:
      1. zsh_history
      1. zshrc
   1. Work folder:
        1. (remove all `node_modules` with: `find . -name 'node_modules' -type d -prune -exec rm -rf '{}' +`)
        1. Find surprisingly large folders with: `du -h -d1` and take care (delete, compress, etc) of large files as needed
        1. Use `rsync -rtv /home/alireza/work/ /path-to-backup/work` to backup work.
        1. Run the above command once more to see errors and react if necessary.
   1. Personal, Documents, Downloads, Pictures, Videos, Music (all except temp sub-folders)
   1. Postman
2. Clean:
   1. Enrolled Fingerprints

# During installation:
1. Download media: (KDE spin)
1. Partitioning:
    1. `/home`: encrypted ext4, 100GB
    2. `/`: encrypted btrfs, 50GB
    3. `/home/alireza/data`: unencrypted ext4 (for database like files)
    4. `home/alireza/work`: unencrypted btrfs (for text source code)
    5. 32GB swap
    6. /boot and /boot/efi: 1gb each, unencrypted
1. 

# After installation
1. Set tap to click and natural scrolling on touchpad.
1. Update all packages, restart
1. Install terminator, set background transparency to 75%
1. Install git
1. Change Ctrl+Alt+T to open Terminator: In keyboard shortcuts, type konsole, remove shortcut and create one for Terminator
2. Install zsh and oh-my-zsh
3. Install
4. Add a panel to the external monitor, set panels to never group icons.
5. Install firefox multi account containers
6. Add persian keyboard, set layout to be per application, add layout indicator widget to panel, set it to show flag, change "Alternative shortcut" to Win+Space.
7. Add Bitwarden add-on, disable auto login filling
8. Install Spotify
9. Install an ad blocker
10. VsCode, change to light theme
1. Generate new ssh key