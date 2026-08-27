# BVH motion and preview avatars / BVH 动作与预览角色

Files: `walk-in-place.bvh` and the separate rigged `avatar-ual1.glb`.

Viewer: https://3dretarget.com/bvh-viewer

1. Open `walk-in-place.bvh` and play it. The visible default character is supplied by the viewer, not stored in the BVH.
2. Inspect model and skeleton view. The skeleton shown belongs to the current target avatar, not a raw reconstruction of every BVH hierarchy node.
3. Replace the preview character with `avatar-ual1.glb` without replacing the motion, then play again.

先加载 BVH 并观察 Viewer 提供的默认人物，再把预览角色替换为独立的 `avatar-ual1.glb`。BVH 包含层级与动作通道，不包含人物网格；GLB 是独立目标角色，不是 BVH 的转换结果。

This is a known positive GLB target comparison, not universal rig certification.

[Detailed guide](https://3dretarget.com/guides/free-bvh-animations-for-retargeting#reproducible-case) · [中文指南](https://3dretarget.com/zh/guides/free-bvh-animations-for-retargeting#reproducible-case) · [Recording](../../recordings/bvh-avatar-preview.webm)
