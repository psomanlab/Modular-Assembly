# Voxelated-Assembly
## Welcome to the _Voxelated Assembly of Scalable and Perfusable Tissue Constructs_ repo!


This repository contains all the files and information needed to fabricate and customize multimaterial perfusion bioreactors, including:
+ CAD models in STEP format for:
   - [Printable bioreactor parts (all bioreactor sizes are in one STEP file)](Bioreactors)
   - [Printed tools, such as bioreactor racks, bioreactor shims, voxel slicing jig](Tools)
   - Hydrogel voxels
+ 3MF project files containing all printable bioreactor parts, complete with print profiles for Prusament PCCF and Recreus FilaFlex Pro 60A for the 5 Toolhead Prusa XL
+ [BOM for bioreactors, with links for sourcing](README.md#bioreactor-bom-by-size)
+ [Prusa XL modifications for printing of Shore 60A filament](README.md#prusa-xl-modifications-list)
  

## Bioreactor BOM, by Size
| Bioreactor | [M3x8 SHCS DIN 912](https://www.mcmaster.com/91292A112/) | [M3x25 SHCS DIN 912](https://www.mcmaster.com/91292A020/) | [M3x30 SHCS DIN 912](https://www.mcmaster.com/91292A022/) | [M3 Square Nut DIN 562](https://www.mcmaster.com/97259A101/) | [M3 Hex Nut DIN 934](https://www.mcmaster.com/97700A110/) | [3mm Glass Slide](https://bolioptics.com/25pc-plane-slide-microscope-slide-glass-slides-3mm-25pc-sl39103102/) | 3mm Laser Cut Acrylic |
|   :---:    |       :---:       |        :---:       |        :---:       |         :---:         |       :---:        |      :---:      |         :---:         |
|    1x1     |         8         |          4         |          -         |           8           |         4          |        2        |           -           |
|    2x1     |         8         |          4         |          -         |           8           |         4          |        2        |           -           |
|    3x1     |        12         |          4         |          -         |          12           |         4          |        2        |           -           |
|    2x2     |        16         |          4         |          -         |          16           |         4          |        -        |     2 (35 x 35 mm)    |
|    2x3     |        16         |          4         |          -         |          16           |         4          |        -        |     2 (45 x 35 mm)    |
|    3x3     |        16         |          4         |          -         |          16           |         4          |        -        |     2 (45 x 45 mm)    |
|    3x6     |        24         |          -         |          6         |          24           |         6          |        -        |     2 (75 x 45 mm)    |


## Prusa XL Modifications List
Minor modifications were required to enable printing of Prusament PCCF and Recreus FilaFlex 60A on the Prusa XL: 
+ **Nozzles:** All nozzles were replaced with wear-resistant 0.4 mm E3D ObXidian nozzles to allow printing of PCCF. Standard flow nozzles were used, but high flow variants will also work. Phaetus SiC nozzles are not recommended for printing PCCF, as they exhibited a high degree of nozzle buildup with this material.
+ **Enclosure:** The printer was also equipped with the official Prusa XL enclosure for printing warp-prone materials. This may not be a firm requirement, but the enclosure does help with filament path modification (see below).
+ **Filament Path:** To print Shore 60A TPU, the standard filament path must be modified to reduce friction and eliminate gaps.
   - Toolhead 5 was dedicated to printing TPU and was modified with a [main plate](https://www.printables.com/model/1486985-xl-nextruder-main-plate-for-bogie-idler-with-load) and [idler lever](https://www.printables.com/model/1365827-mk4s-xl-core-one-bogie-idler-with-more-pivot) featuring a more constrained filament path.
   - The filament sensor in toolhead 5 was modified by replacing the tensioning spring with two small magnets. [Instructions for the modification can be found here in the filament sensors section.](https://www.printables.com/model/975519-xl-nextruder-super-constrained-main-plateidler-lev).
   - The side-mounted filament sensor and PTFE tube for toolhead 5 were bypassed to reduce friction. Filament was instead fed via a [magnetic spool holder](https://www.printables.com/model/128189-magnetic-mounted-spool-holder) mounted to the top of the enclosure, with the filament passed through an empty rivet hole.
   - Filament was guided to the toolhead using short segments of PTFE tubing clipped to the cable harness with [modified cable clips](https://www.printables.com/model/718498-prusa-xl-soft-tpu-cable-clip-to-extruder-prusa-xl).
   - [Nozzle wipers](https://www.printables.com/model/894119-diy-silicone-tube-nozzle-wiper-prusa-xl-mounting-h) made from segments of silicone tubing were installed to help clean the nozzles during tool changes.
