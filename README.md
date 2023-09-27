# sonospower


Control your sonos speaker from a Powermate USB rotary controller.

## Requirements

Linux, Python 3, a sonos speaker & a USB powermate controller.

## Install

1. Copy 95-powermate.rules to  /etc/udev/rules.d/
2. Ensure the user you run this as is in uinput group (create group if required)
3. Reload udev conf (udevadm control -R)
4. Plug in powermate
5. Create a virtualenv
6. Install the requirements (pip install -r requirements.txt)
7. Run sonospower!
