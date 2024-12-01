Wacom Recordings
================

This repository contains recordings of interactions with tablet devices. With
the [hid-replay tool](https://github.com/hidutils/hid-replay) you
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
needs to be run as root. It can be installed with `cargo`:

```
$ sudo CARGO_INSTALL_ROOT=/usr/local cargo install hid-replay
$ sudo hid-replay path/to/recording
```

Alternatively you can download a pre-built binary from the 
[hid-replay releases](https://github.com/hidutils/hid-replay/releases).
```
$ unzip hid-replay.zip
$ chmod +x hid-replay
$ sudo ./hid-replay
```

License
=======

MIT if copyright even applies, these are just recordings.
