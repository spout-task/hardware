# SPOUT hardware

Hardware for a **SPOUT** rig, part of the [spout-task](https://github.com/spout-task) project.
Every device has its own folder with design files, pictures and a README that explains what it does,
what to buy, how to make it and how to connect it to SPOUT.

A complete rig costs about **1,080 USD** (about 1,440 USD including a computer and screen).
The full bill of materials is in [`SPOUT_BOM.xlsx`](SPOUT_BOM.xlsx) and [`SPOUT_BOM.pdf`](SPOUT_BOM.pdf).

## Devices

| Group | Device | What it does | How it is made | Folder |
|---|---|---|---|---|
| Electronics | Teensy breakout board | Carries the Teensy 4.1, drives the solenoids and brings out all inputs and outputs | PCB, 3D printed housing | [`teensy_breakout_board`](teensy_breakout_board/) |
| Electronics | Dual lick detector | Detects licks on one or two spouts with sub millisecond precision | PCB, 3D printed housing | [`dual_lick_detector`](dual_lick_detector/) |
| Electronics | Optogenetics power modulator | Turns a Teensy PWM signal into a 0 to 5 V analog command, so light power can be set per trial | Hand built circuit, 3D printed housing | [`optogenetics_power_modulator`](optogenetics_power_modulator/) |
| Head fixation | Head restrained setup | Headplates and holders for behavior and for two photon imaging | Laser cut titanium, machined or 3D printed holders | [`head-restrained_setup`](head-restrained_setup/) |
| Head fixation | Breadboards | Rig base plate and round base for the head fixation | Machined aluminium (or bought) | [`breadboards`](breadboards/) |
| Spout positioning | Motorized manipulator | Three axis stepper stage that positions the spouts | Bought stages, 3D printed adapters, laser cut driver box | [`motorized_manipulator`](motorized_manipulator/) |
| Spout positioning | Spout holder | Holds the stainless steel lick spout(s) | 3D printed | [`spout_holder`](spout_holder/) |
| Miscellaneous | Housings | Boxes for the audio amplifier and for the power distribution breadboard | 3D printed | [`housing_miscellaneous`](housing_miscellaneous/) |

## Build order for one rig

1. **Base.** Mount the 12 x 18 inch breadboard on the table with two table clamps.
2. **Head fixation.** Build the head restrained setup on the round breadboard: magnetic base, post, clamp, aluminium tube and headplate holders.
3. **Water delivery.** Reservoir syringes, 3 way valves, solenoids in the solenoid holder, Tygon tubing, and the spouts in the spout holder.
4. **Spout positioning.** Stack the three linear stages with the printed adapters, mount the spout holder on a post on the top stage, and put the three drivers in the laser cut box.
5. **Electronics.** Teensy breakout board in its housing, power distribution box, dual lick detector in its housing. Connect the spouts to the lick detector and ground the mouse through the aluminium tube.
6. **Sound.** Audio amplifier in its housing and two speakers on short posts.
7. **Optogenetics (optional).** Optogenetics power modulator between the Teensy and the LED or AOM driver.
8. **Software.** Flash the firmware and open the GUI, see the [software](https://github.com/spout-task/software) repository.

Photos of the build process will be added.

## Conventions

* 3D printed parts: Prusa MK3, PLA, standard settings.
* Screws: 1/4 20 for the breadboards and posts, 4-40 for small parts.
* Units: mm, except the breadboards (inch).
* Each device folder has `files` (design files) and `pictures` (renders and photos).

## Related repositories
[software](https://github.com/spout-task/software), [analyses](https://github.com/spout-task/analyses), [settings](https://github.com/spout-task/settings), [example_data](https://github.com/spout-task/example_data)

## License
All hardware designs in this repository are released under **CERN-OHL-S-2.0** ([`LICENSE`](LICENSE)).
The dual lick detector and the Teensy breakout board were designed by the
[HMS Research Instrumentation Core](https://github.com/HMS-RIC), whose members are authors of SPOUT,
and are shared here as part of SPOUT. Newer revisions of the lick detector are developed in the
[HMS RIC repository](https://github.com/HMS-RIC/2-Channel-Lick-Detector).

## How to cite
See [`CITATION.cff`](CITATION.cff) and the [project overview](https://github.com/spout-task).
