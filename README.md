ansible-role-watchmap
=========

Set up smart watch tool [watchmap](https://github.com/nbr23/watchmap) to plot activity when watch is plugged to USB, legeraging `udev` rules and `systemd` oneshot services.

Role Variables
--------------

- `watchmap_out_dir`: Target directory where the HTML watchmap outputs will be sotred on the target system
- `watchmap_user`: User on the target system with which to run the watchmap processing
- `watchmap_vendor_id`: Vendor ID of your device (can be found using `lsusb`. My garmin device's vendor ID is: `091e`)

Example Playbook
----------------

```
---
- hosts: all

  roles:
  - role: ansible-role-watchmap
    vars:
        watchmap_out_dir: /data/watchmap
        watchmap_user: watchmap_user
        watchmap_vendor_id: 091e
```
License
-------

MIT
