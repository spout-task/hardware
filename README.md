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
| Head fixation | Head restrained setup | Headplates and holders for behavior and for two photon imaging | Laser cut titanium headplates, machined aluminium holders, ramps and cone | [`head-restrained_setup`](head-restrained_setup/) |
| Head fixation | Breadboards | Rig base plate and round base for the head fixation | Machined aluminium by a machine shop (or bought) | [`breadboards`](breadboards/) |
| Spout positioning | Motorized manipulator | Three axis stepper stage that positions the spouts | Bought stages and drivers, 3D printed adapters, laser cut driver box and drilling templates | [`motorized_manipulator`](motorized_manipulator/) |
| Spout positioning | Spout holder | Holds the stainless steel lick spout(s) and the two solenoid valves | 3D printed spout holders, laser cut solenoid holder | [`spout_holder`](spout_holder/) |
| Miscellaneous | Housings | Boxes for the audio amplifier and for the power distribution breadboard | 3D printed | [`housing_miscellaneous`](housing_miscellaneous/) |

## Build order for one rig

1. **Base.** The 12 x 18 inch breadboard is the base of the rig.
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
* Units: mm, except the breadboard STEP files (inch). DXF files are in mm.
* Each device folder has a `design` folder with `files` (design files) and `pictures` (renders). Electronics also have a `PCB` or `circuit` folder, and the manipulator a `schematics` folder.
* File types: STL to 3D print, DXF to laser cut, STEP to edit in CAD or to send to a machine shop. Flat parts come as DXF and STL, so you can laser cut or print them.
* Each README lists for every part how we made it and from what material.

## Related repositories
[software](https://github.com/spout-task/software), [analyses](https://github.com/spout-task/analyses), [settings](https://github.com/spout-task/settings), [example_data](https://github.com/spout-task/example_data)

## License
All hardware designs in this repository are released under **CERN-OHL-S-2.0** ([`LICENSE`](LICENSE)).
The dual lick detector and the Teensy breakout board were designed by the
[HMS Research Instrumentation Core](https://github.com/HMS-RIC), whose members are authors of SPOUT,
and are shared here as part of SPOUT. Newer revisions are developed in the HMS RIC repositories for the
[lick detector](https://github.com/HMS-RIC/2-Channel-Lick-Detector) and the
[Teensy breakout board](https://github.com/HMS-RIC/Teensy-Breakout-general-purpose).

## How to cite
See [`CITATION.cff`](CITATION.cff) and the [project overview](https://github.com/spout-task).
