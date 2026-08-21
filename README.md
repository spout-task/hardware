# SPOUT · hardware

Custom hardware for a **SPOUT** rig — part of the [spout-task](https://github.com/spout-task) project (see the
[project overview](https://github.com/spout-task)). Each subsystem has its own folder and README.

| Subsystem | Description | Folder |
|---|---|---|
| Dual-lick detector | Two-channel current-based lick sensing (third-party HMS design) | [`dual_lick_detector/`](dual_lick_detector/) |
| Teensy breakout board | PCB carrying the Teensy with solenoid drivers and I/O | [`teensy_breakout_board/`](teensy_breakout_board/) |
| Head-restrained setup | Headplate designs for optogenetics and two-photon imaging | [`head-restrained_setup/`](head-restrained_setup/) |
| Motorized manipulator | Three-axis motorized spout positioner | [`motorized_manipulator/`](motorized_manipulator/) |
| Optogenetics power modulator | Op-amp: 3.3 V PWM -> calibrated optical power (mW) | [`optogenetics_power_modulator/`](optogenetics_power_modulator/) |

## Related repositories
[software](https://github.com/spout-task/software) · [analyses](https://github.com/spout-task/analyses) · [settings](https://github.com/spout-task/settings) · [example_data](https://github.com/spout-task/example_data)

## License
Our custom designs: **CERN-OHL-S-2.0** ([`LICENSE`](LICENSE)).
The **dual-lick detector** is a third-party HMS design under its own upstream license — see
[`dual_lick_detector/README.md`](dual_lick_detector/README.md) and
https://github.com/HMS-RIC/2-Channel-Lick-Detector

## Status
The dual-lick detector design files are included. The other four subsystems currently ship
as placeholders; CAD/PCB files, a bill of materials, and assembly steps will be added.

## How to cite
See [`CITATION.cff`](CITATION.cff) and the [project overview](https://github.com/spout-task).
