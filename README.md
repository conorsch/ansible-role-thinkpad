# ansible-thinkpad

Common config settings for hardware compatibility on Lenovo ThinkPads.

## Requirements

Tested on the following ThinkPad models:

* ThinkPad X1 Carbon 3rd
* ThinkPad T450s

Assumes a Debian-like OS.

## Role Variables

```
# Use the TrackPoint as a scroll-wheel when middle-click is depressed.
# Great for ergonomic scrolling without repetitive swiping motions.
thinkpad_x11_trackpoint_scroll: false

# Installing 'xbacklight' is generally good enough for brightness controls.
thinkpad_intel_backlight: false

# Sets boot options 'thinkpad_acpi force_load=1'. Was necessary briefly in 2015,
# but modern distros seem to have accounted for this problem, so off by default.
thinkpad_configure_acpi: false

# Some ThinkPads require additional pointer support, e.g. X1 3rd Gen
# under Ubuntu 14.04. Leave off unless trackpad isn't working
thinkpad_configure_imps: false
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
