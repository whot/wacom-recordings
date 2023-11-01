Wacom Recordings
================

This repository contains recordings of interactions with tablet devices. With
the [hid-replay tool](https://gitlab.freedesktop.org/libevdev/hid-tools) you
can re-create a tablet device at the kernel level and trick the rest of
the stack into having a tablet device connected.

If you just need a device *present*, it doesn't matter which recording you use.
Otherwise, check the filename and the top of the file for a description of what
the file does.

Note that most devices have multiple logical devices, usually one for the
tablet events and one for the touch events. For full emulation you may need
to replay (or at least create) both devices but in most cases this does not
matter.

If you need a recording of a specific interaction, please file an issue.

Creating/replaying devices
==========================

Note that `hid-replay` needs to create a UHID kernel device via `/dev/uhid` and thus
needs to be run as root. It can be run from the git repository:

```
$ git clone https://gitlab.freedesktop.org/libevdev/hid-tools
$ cd hid-tools
$ sudo ./hid-replay <recording>
```

Alternatively you can pip install it (as root)

```
$ sudo pip install https://gitlab.freedesktop.org/libevdev/hid-tools
$ sudo hid-replay <recording>
```

License
=======

MIT if copyright even applies, these are just recordings.
