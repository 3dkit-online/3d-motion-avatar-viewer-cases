# VRMA needs an avatar / VRMA 需要角色

Files: `avatar.vrm` and `motion.vrma`.

Viewer: https://3dretarget.com/vrm-viewer

1. Drop only `motion.vrma` onto the empty viewer. It cannot provide a character; a load error is not evidence that the VRMA is corrupt.
2. Reset, then open `avatar.vrm`. The character appears without motion.
3. Use **Add motion** to load `motion.vrma`, then play the native VRMA clip.

先单独加载 `motion.vrma`，它不会提供角色网格；重置后加载 `avatar.vrm`，再通过“添加动作”载入 VRMA。这个对照说明角色与动作是两个独立资源。

[Detailed guide](https://3dretarget.com/guides/what-is-a-vrma-file-and-how-to-open-it#reproducible-case) · [中文指南](https://3dretarget.com/zh/guides/what-is-a-vrma-file-and-how-to-open-it#reproducible-case) · [Recording](../../recordings/vrma-needs-avatar.webm)
