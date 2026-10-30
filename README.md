# ROBO-CAD

CAD for the EduSCARA resistor-sorting rig: grippers, a camera tower and a multimeter mount.
Only CAD is kept here: Fusion sources, STEP exports and print-ready STLs.

## Structure

```
ROBO-CAD/
├── camera_tower/
│   └── corner_watchtower/
├── gripper/
│   ├── 1-parallelogram/
│   └── 2-rack-n-pinion/
└── multimeter/            (empty for now)
```

Each design folder holds its `.f3d` (Fusion 360 source) and `.step` (neutral exchange) files at the top level. Print-ready meshes are in an `stl/` subfolder.

## Designs

### `camera_tower/corner_watchtower`
Camera tower that holds an Arducam above the rig's back corner, looking down at the pick plate. Two column options: a 2020 aluminium extrusion (main) or a printed column.

- `camera_tower_200mm.f3d`: assembly with the aluminium column.
- `camera_tower_200mm_printed_column.f3d`: assembly with the printed column.
- `camera_tower_base_print.f3d`, `camera_tower_head_print.f3d`, `camera_tower_column_print.f3d`: print-ready part files.
- `camera_tower_with_rig.f3d`, `camera_tower_with_arm_and_rig.f3d`: the tower placed in the rig scene, without and with the arm.
- `*.step`: assembly exports for both column options.
- `stl/`: base, head and printed column.

### `gripper/1-parallelogram`
Double-parallelogram gripper driven by an SG90 servo through a 2:1 spur gear pair. Bolt-on "Cranked A" tips on jaw carriers. All pins and caps are printed.

- `Gripper v3a.1 - Bolt-on Tips.f3d` / `.step`: the main model.
- `Gripper v3 - Printed hardware (pins + caps).f3d`: the printed pins and caps.
- `Gripper v3 - SG90 changed parts + pinion variants.f3d`: the SG90 rework parts and pinion variants, including the final 4.6 mm bore pinion.
- `stl/`: the 14 gripper parts (numbered 01 to 16, with 11 and 12 unused) plus the pins and caps.

### `gripper/2-rack-n-pinion`
Single-pinion, twin-rack parallel gripper driven by a NEMA 8 stepper, mounted on the EduSCARA Z-shaft.

- `Gripper v3 - Housing.f3d` / `.step`: the gripper itself.
- `EduSCARA + Gripper v3.f3d` / `.step`: the gripper on the EduSCARA arm.
- `stl/`: the 7 printed parts (base plate, arm plate, racks, pinion, motor adapter, shaft insert).

### `multimeter`
Not started yet.

## Notes

- File names inside the designs still carry earlier version labels (for example the rack-and-pinion gripper's files say "Gripper v3"). The folder names are the current naming.
- Fusion files open in Autodesk Fusion. Use the `.step` files for other CAD tools.
- STLs are exports from the CAD. If a part changes, regenerate its STL.
