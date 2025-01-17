# System76 Open Firmware

An open source distribution of firmware utilizing coreboot, EDK2, and System76
firmware applications.

## Supported models

These models are supported and will receive updates through the firmware
manager:

- addw2
- bonw14
- darp6
- darp7
- galp4
- galp5
- gaze15
- gaze16-3050
- gaze16-3060
- gaze16-3060-b
- lemp9
- lemp10
- oryp6
- oryp7
- oryp8

Other models may be in development or available without support, and can be
seen in the `models/` directory.

If the device becomes bricked it will require restoring the current firmware
using an external programmer. See [flashing](./docs/flashing.md) for details.

### Schematics

System76 customers may request board schematics for their system by sending an
email to firmware@system76.com with the subject line  "Schematics for _model_",
where _model_ is one of the supported models listed above. Please include the
serial number of your system for verification.

You may not share these without explicit permission from System76.

## Changelog

For a list of important changes please see the [changelog](./CHANGELOG.md).

## Dependencies

### Install toolchain
```
./scripts/deps.sh
```

### Load Rust environment (or optionally reboot)
```
source ~/.cargo/env
```

### Build firmware, replace qemu with your model (look in the models directory for examples)
```
./scripts/build.sh qemu
```

### Emulate firmware, only available after building the qemu model
```
./scripts/qemu.sh
```
