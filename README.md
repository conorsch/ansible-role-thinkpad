# ansible-thinkpad

Common config settings for hardware compatibility on Lenovo ThinkPads.

## Requirements

Tested on the following ThinkPad models:

* ThinkPad X1 Carbon 3rd
* ThinkPad T450s

Assumes a Debian-like OS.

## Role Variables

```
# TODO
```

## Dependencies

If you have problems with graphical distortion, changing the X11 video driver
may help. Changing the driver is disabled by default because it may negatively
affect video performance.

`thinkpad_driver_downgrade: false`

This was an issue under Ubuntu 14.04 but may have since been patched in stable.

## Example Playbook

```
- hosts: laptop
  roles:
     - role: conorsch.thinkpad
       thinkpad_x11_trackpoint_scroll: true
```

## License

MIT
