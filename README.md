# steamdeck_startup_animations
A collection of steamdeck startup animations, plus a script to randomize your startup on each boot

credits / kudos go to kageuruf fo his original github repository:
https://github.com/kageurufu/steamdeck_startup_animations/blob/main/

# I put different boot animations in the folder, feel free to use other ones:

* 

# Installation

```sh
curl -o - https://raw.githubusercontent.com/Steamdeckchecker/Steamdeckrandomizeboot/main/install.sh | bash -
```

If you're (justifiably) not a fan of `curl | bash`, you can run this:

```sh
mkdir -p "$HOME/homebrew"
mkdir -p "$HOME/.config/systemd/user"
git clone https://github.com/Steamdeckchecker/Steamdeckrandomizeboot "$HOME/homebrew/startup_animations"
ln -sf "$HOME/homebrew/startup_animations/randomize_deck_startup.service" "$HOME/.config/systemd/user/randomize_deck_startup.service"
systemctl --user daemon-reload
systemctl --user enable --now randomize_deck_startup.service
```

# Uninstallation

```sh
bash $HOME/homebrew/startup_animations/uninstall.sh
