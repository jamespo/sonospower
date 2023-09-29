# sonospower


Control your sonos speaker from a Powermate USB rotary controller.

## Requirements

Linux, Python 3, a sonos speaker & a USB powermate controller.

## Install

1. Copy 95-powermate.rules to  /etc/udev/rules.d/
2. Ensure the user you run this as is in uinput group (create group if required, or choose another group). Note if you add to user group membership you will need to reboot so that systemd user process picks it up. 
3. Reload udev conf (sudo udevadm control -R)
4. Copy contents of systemd/ to ~/.config/systemd/user/
5. systemctl --user enable sonospower.path
6. systemctl --user daemon-reload
7. Plug in powermate
8. Create a virtualenv
9. Install the requirements (pip install -r requirements.txt)
10. Copy sonospower to /usr/local/bin (or whatever path in .service file). Ensure python shebang path reflects virtualenv.
11. systemctl --user start sonospower.service (or reboot)

## Usage

* Rotate left - reduce volume
* Rotate right - increase volume
* Push button - play / pause
* Double push button - next track
