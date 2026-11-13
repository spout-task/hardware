# Head restrained setup

Headplates and holders that keep the mouse's head still during behavior (with optogenetics) and two photon
imaging. The headplates are laser cut from titanium; the holders, ramps and imaging cone are machined
from aluminium (3D printing also works for the holders and ramps).

<p align="center">
  <img src="design/pictures/head-restriction_setup_side.png" alt="Head restrained setup, side view" width="32%">
  <img src="design/pictures/head-restriction_setup_top.png" alt="Head restrained setup, top view" width="32%">
  <img src="design/pictures/head-restriction_setup_imaging.png" alt="Head restrained setup with the imaging holder" width="32%">
</p>
<p align="center"><em>Head restrained setup: side view, top view, and with the imaging holder.</em></p>

## At a glance

| | |
|---|---|
| Function | Head fixation for behavior (small plate) and for two photon imaging (plate with window opening) |
| Fabrication | Headplates: laser cut grade 5 titanium. Holders, ramps, cone: machined aluminium; holders and ramps can also be 3D printed |
| Approximate cost | Headplates 1.40 to 1.61 USD each, cone 4.50 USD, mounting hardware about 280 USD |
| Used by | SPOUT1 and SPOUT2 |

## The parts

| Part | Purpose |
|---|---|
| Behavior headplate | Small plate that leaves the skull free for optical fibers and other implants |
| Behavior holders, left and right | Clamp the behavior headplate |
| Behavior 15 degree ramp (right) | Levels the head of mice implanted at an angle. Only a right ramp exists, because a left one is too small to be practical |
| Imaging headplate | Plate with a central opening for a cranial window or GRIN lens; three small magnets are pressed into it |
| Imaging holder | Large U shaped holder for the imaging headplate |
| Imaging 15 degree ramps, left and right | Level the head of mice implanted at an angle for lateral imaging, so straight and angled mice train on the same rig |
| Imaging cone | Sits on the imaging headplate with three magnets and holds water for the objective. Seal with a thin layer of silicone (Picodent Eco sil speed) |
| Imaging cover | Snaps on magnetically to protect the window between sessions. Add silicone if the mouse removes it |

<p align="center">
  <img src="design/pictures/headplate_behavior_photo.png" alt="Behavior headplate, titanium" width="32%">
  <img src="design/pictures/headplate_2pimaging_photo.png" alt="Imaging headplate, titanium, with three magnets" width="25%">
  <img src="design/pictures/headplate_2pimaging_cone_photo.png" alt="Imaging cone, aluminium, with three magnets" width="25%">
</p>
<p align="center"><em>Behavior headplate, imaging headplate with magnets, and imaging cone.</em></p>

## Files

All design files are in [`design/files`](design/files/) and renders in [`design/pictures`](design/pictures/).

| Part | Files | What it is | How we made it |
|---|---|---|---|
| Behavior headplate | [`.dxf`](design/files/headplate_behavior.dxf), [`.stl`](design/files/headplate_behavior.stl), [`.step`](design/files/headplate_behavior.step) | 27.5 x 10.4 mm | Laser cut, grade 5 titanium 0.04 inch (1 mm), SendCutSend |
| Imaging headplate | [`.dxf`](design/files/headplate_2pimaging.dxf), [`.stl`](design/files/headplate_2pimaging.stl), [`.step`](design/files/headplate_2pimaging.step) | 27.5 x 23.8 mm | Laser cut, grade 5 titanium 0.04 inch (1 mm), SendCutSend |
| Imaging cover | [`.dxf`](design/files/headplate_2pimaging_cover.dxf), [`.stl`](design/files/headplate_2pimaging_cover.stl), [`.step`](design/files/headplate_2pimaging_cover.step) | 17.6 x 15.5 mm | Laser cut, titanium, SendCutSend |
| Behavior holders, left and right | [`left.stl`](design/files/headplate_behavior_holder_left.stl), [`left.step`](design/files/headplate_behavior_holder_left.step), [`right.stl`](design/files/headplate_behavior_holder_right.stl), [`right.step`](design/files/headplate_behavior_holder_right.step) | Clamp the behavior headplate | Machined aluminium (can also be 3D printed) |
| Behavior ramp, right | [`.stl`](design/files/headplate_behavior_15degreesramp_right.stl), [`.step`](design/files/headplate_behavior_15degreesramp_right.step) | 15 degree ramp | Machined aluminium (can also be 3D printed) |
| Imaging holder | [`.stl`](design/files/headplate_2pimaging_holder_big.stl), [`.step`](design/files/headplate_2pimaging_holder_big.step) | U shaped holder | Machined aluminium (can also be 3D printed) |
| Imaging ramps, left and right | [`left.stl`](design/files/headplate_2pimaging_15degreesramp_left.stl), [`left.step`](design/files/headplate_2pimaging_15degreesramp_left.step), [`right.stl`](design/files/headplate_2pimaging_15degreesramp_right.stl), [`right.step`](design/files/headplate_2pimaging_15degreesramp_right.step) | 15 degree ramps | Machined aluminium (can also be 3D printed) |
| Imaging cone | [`.stl`](design/files/headplate_2pimaging_cone.stl), [`.step`](design/files/headplate_2pimaging_cone.step) | Water cone for the objective | Machined aluminium 6061, eMachineShop |

DXF files are in mm.

## Bill of materials

| Qty | Part | Supplier | Part number | Price (USD) |
|---|---|---|---|---|
| 1 | Behavior headplate | SendCutSend | Titanium | 1.40 |
| 1 | Imaging headplate | SendCutSend | Titanium | 1.61 |
| 1 | Imaging cone | eMachineShop | Aluminium 6061 | 4.50 |
| 3 | Magnets for the headplate, 1/16 x 1/32 inch | K&J Magnetics | | 0.14 each |
| 3 | Magnets for the cone, 2 x 0.5 mm | The Magnet Baron | | 0.15 each |
| 2 | Headplate holders | Machined, aluminium | | |
| 1 | Kinematic magnetic base | Newport | BK-3A | 159.64 |
| 1 | Pedestal post holder | Thorlabs | PH1 | 8.74 |
| 1 | Optical post | Thorlabs | TR6 | 8.66 |
| 1 | Adjustable height optics clamp | Thorlabs | VG100 | 93.34 |
| 1 | Aluminium tube (body tube, also the mouse ground) | McMaster-Carr | 6061 | 6.75 |
| 1 | Banana socket | | | 1.28 |
| 1 | Round breadboard | see [`breadboards`](../breadboards/) | | |

Full list: [`SPOUT_BOM.xlsx`](../SPOUT_BOM.xlsx).

## Assembly

1. Mount the round breadboard on the rig breadboard.
2. Build the head fixation post: kinematic magnetic base, pedestal post holder, optical post and optics clamp.
3. Mount the headplate holders (with a ramp if needed) on the head fixation post with 4-40 screws.
4. Place the aluminium tube for the mouse body and connect it to the lick detector ground with the banana socket.
5. Press the magnets into the imaging headplate and the cone.

Photos of the build process will be added. Surgery and headplate implantation are described in the
Methods of the [SPOUT paper](https://www.biorxiv.org/content/10.64898/2026.08.21.746318v2).

## License
**CERN-OHL-S-2.0** ([`LICENSE`](../LICENSE)).
