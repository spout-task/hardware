# Motorized manipulator

Three motorized linear stages stacked into an X, Y, Z manipulator that positions the lick spouts in
front of the mouse. Each stage has its own stepper motor driver and controller, so spouts can be moved
precisely and returned to the same position every session.

<p align="center">
  <img src="design/pictures/micromanipulator_to_breadboard1.png" alt="Adapter from stage to breadboard" width="40%">
  <img src="design/pictures/micromanipulator_stage2postHalfInch1.png" alt="Adapter from stage to post" width="40%">
</p>

## At a glance

| | |
|---|---|
| Function | Three axis positioning of the spout holder |
| Fabrication | Bought linear stages and drivers, 3D printed adapters, laser cut driver box and drilling templates |
| Control | Manually from the controller display, or by TTL input to the drivers |
| Approximate cost | 240 USD |
| Used by | SPOUT1 and SPOUT2 |

The drivers accept TTL control, so the stages can be moved by a microcontroller or a computer.
The SPOUT firmware does not move the stages; in SPOUT they are positioned manually.

## Files

All design files are in [`design/files`](design/files/) and renders in [`design/pictures`](design/pictures/).

| Part | Files | What it is | How we made it |
|---|---|---|---|
| Adapter to breadboard | [`.stl`](design/files/micromanipulator_to_breadboard.stl), [`.step`](design/files/micromanipulator_to_breadboard.step) | Plate (4 x 2 inch) that mounts the bottom stage on the breadboard | 3D printed, PLA |
| Adapter to 1/2 inch post | [`.stl`](design/files/micromanipulator_stage2postHalfInch.stl), [`.step`](design/files/micromanipulator_stage2postHalfInch.step) | Adapter from the top stage to a 1/2 inch post | 3D printed, PLA |
| Adapter to 1/4 inch post | [`.stl`](design/files/micromanipulator_stage2postQuarterInch.stl), [`.step`](design/files/micromanipulator_stage2postQuarterInch.step) | Adapter from the top stage to a 1/4 inch post | 3D printed, PLA |
| Drilling template 5 cm | [`.dxf`](design/files/template_linear_track_holes-5cm.dxf), [`.stl`](design/files/template_linear_track_holes-5cm.stl), [`.step`](design/files/template_linear_track_holes-5cm.step) | Template (1 mm) to mount one stage on the carriage of another | Laser cut, 1 mm acrylic |
| Drilling template 10 cm | [`.dxf`](design/files/template_linear_track_holes-10cm.dxf), [`.stl`](design/files/template_linear_track_holes-10cm.stl), [`.step`](design/files/template_linear_track_holes-10cm.step) | Same, for the 10 cm position | Laser cut, 1 mm acrylic |
| Drilling template edge | [`.dxf`](design/files/template_linear_track_holes-edge.dxf), [`.stl`](design/files/template_linear_track_holes-edge.stl), [`.step`](design/files/template_linear_track_holes-edge.step) | Template (30 x 28 x 1 mm) for the end plate of a stage | Laser cut, 1 mm acrylic |
| Driver box | [`.pdf`](design/files/box_mounting_steppermotor_drivers.pdf), [`.ai`](design/files/box_mounting_steppermotor_drivers.ai) | Box for the three drivers | Laser cut, 1/8 inch acrylic |

3D printed parts: Prusa MK3, PLA, standard settings. The templates can also be 3D printed from the STL files.

## Schematics

Schematics of the linear stage and of the stepper motor driver and controller.

<p align="center">
  <img src="schematics/track_1.png" alt="Linear stage, top and side view with dimensions in mm" width="48%">
  <img src="schematics/track_2.png" alt="Linear stage with motor lead colors" width="48%">
</p>

| Schematic | What it shows |
|---|---|
| [`track_1.png`](schematics/track_1.png) | Linear stage, top and side view with dimensions in mm (175 mm long, carriage 32 mm with 4 M3 holes) |
| [`track_2.png`](schematics/track_2.png) | Linear stage with the stepper motor lead colors: green A minus, blue B minus, black A+, red B+ |
| [`driver_1.png`](schematics/driver_1.png) | Front panel of the driver and controller |
| [`driver_2.png`](schematics/driver_2.png) | Front panel with every button, indicator and the speed knob labelled |
| [`driver_3.png`](schematics/driver_3.png) | Driver board: microstep DIP switch table, current adjustment, control input header, motor and power terminals |
| [`driver_4.png`](schematics/driver_4.png) | Wiring of the stepper motor and the 24 V supply to the driver |

<p align="center">
  <img src="schematics/driver_2.png" alt="Driver front panel, labelled" width="48%">
  <img src="schematics/driver_4.png" alt="Wiring of motor and power supply" width="48%">
</p>

## Bill of materials

| Qty | Part | Supplier | Part number | Price (USD) |
|---|---|---|---|---|
| 3 | Linear stage with NEMA 11 stepper motor (50 mm) | Befenybay | BE073-1 | 47.30 each |
| 3 | Stepper motor driver and controller | Banria | 4257 | 26.90 each |
| 1 | Power supply 24 V | DROK | | 15.89 |
| 1 | Laser cut driver box | | | |
| 1 | 3D printed adapter to breadboard | | | |
| 1 | 3D printed adapter to post | | | |

Full list: [`SPOUT_BOM.xlsx`](../SPOUT_BOM.xlsx).

## Assembly

0. You do not need the adapters nor taking apart the linear track if they have screw holes in them to allow assembling X, Y, and Z axes.
1. Laser cut the adapters and the driver box and the drilling templates.
2. 3D print the micromanipulator_to_breadboard, micromanipulator_stage2post, and a water_spout_(bottom or side)_mount.
3. Open each linear track (4 screws in total), remove the front and bottom plate, and carefully make sure you do not drop bearings.
4. Use the laser cut adapter (5 or 10 cm, depending on your linear track) to mark drill holes in the bottom plate. Do the same for the front part using adapter template_linear_track_holes-edge.
5. Drill 4 holes (3 mm) in the bottom plate, two holes in the front plate (3 mm), and (counter)sink the screw head.
6. Reassemble the linear tracks and mount them using M3 screws to make X, Y, and Z axes.
7. Screw the bottom linear track (X or Y) on micromanipulator_to_breadboard and mount it on the breadboard with 1/4 20 screws.
8. Mount micromanipulator_stage2post on the top linear track (Z) and use optical posts (cage rods) and a swivel (mini-post swivel post clamp) to mount the [spout holder](../spout_holder/) in it.
10. Connect four wires to each stepper motor driver [`driver_4.png`](schematics/driver_4.png) and solder those a connector. Connect the three drivers with a shared positive and negative and solder it to a general connector. Click the three drivers in the driver box, mount the connectors and power connector to the side, and glue the driver box using acrylic cement.
11. Connect each motor to a connector [`driver_4.png`](schematics/driver_4.png). Motor leads: black A+, green A minus, blue B minus, red B+ (check the label on your motor). Make sure the labels match when you plug it into the driver box.

Photos of the build process will be added.

## Use

* Move an axis with the CW and CCW buttons; set the speed with the knob.
* Set the microstep resolution with the DIP switch and the motor current (0 to 4 A) with the potentiometer on the driver board; see [`driver_3.png`](schematics/driver_3.png).
* For TTL control, connect the CW, CCW and STOP inputs on the driver header to your controller.

## License
**CERN-OHL-S-2.0** ([`LICENSE`](../LICENSE)) for the printed and laser cut parts. The stages and drivers are commercial products.
