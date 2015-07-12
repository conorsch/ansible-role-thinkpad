ansible-thinkpad
=========

Common config settings for fixing hardware compatibility on Lenovo X1 Carbon 3rd Gen and Ubuntu 14.04.

Requirements
------------

Assumes Ubuntu. Assumes 3rd gen for X1 Carbon series (serial number /^20BS/).

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

If you have problems with graphical distortion, changing the X11 video driver
may help. Changing the driver is disabled by default because it may negatively
affect video performance.

`thinkpad_driver_downgrade: false`

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: laptop
      roles:
         - { role: conorsch.thinkpad-ansible, thinkpad-driver_downgrade: true }

License
-------

MIT
