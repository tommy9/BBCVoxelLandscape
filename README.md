﻿# BBCVoxelLandscape

Demonstration of voxel landscape for the BBC Micro. 

Based on the example code at https://github.com/s-macke/VoxelSpace/tree/master?tab=readme-ov-file

Assemble with beebasm
```
beebasm.exe -i voxasm.asm -do voxel.ssd -opt 2 -title Voxel
```

Screen display is a slightly reduced mode 8 with double buffering. The landscape is 8k of data (64x128 pixels) and it's averaged every other horizontal position to reduce the calculations required. Colour is simply based on landscape "height". Lots of pre-calculated tables wherever possible and a fast multiply (1408 multiplies for the initial frame) and a fast vertical line draw routine.
