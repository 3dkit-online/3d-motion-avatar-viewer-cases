# BVH root motion / BVH 根位移与原地行走

Viewer: https://3dretarget.com/bvh-viewer

Reset between the two files. Pause after loading, return to the first frame, disable Loop, and play each clip from start to finish.

| File | Expected observation |
| --- | --- |
| `walk-travel.bvh` | The legs walk and the character moves relative to the floor grid |
| `walk-in-place.bvh` | The same leg rhythm and vertical bob remain without horizontal travel |

The hierarchy, frame count, frame time, rotations, and vertical root values match. Only horizontal hips translation is zeroed in the in-place variant. This controlled transformation is not a general foot-sliding correction.

分别加载两个文件，从首帧关闭循环后完整播放。两者保留相同的步态与胯部上下运动，原地版只移除了水平根位移；它不能自动修复任意动作的脚滑。

[Detailed guide](https://3dretarget.com/guides/fix-bvh-scale-axis-and-root-motion#reproducible-case) · [中文指南](https://3dretarget.com/zh/guides/fix-bvh-scale-axis-and-root-motion#reproducible-case) · [Recording](../../recordings/bvh-root-motion.webm)
