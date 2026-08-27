# FBX geometry vs animation / FBX 模型与动作分开判断

Viewer: https://3dretarget.com/fbx-viewer

Reset the viewer before opening each file.

| File | Actual contents | Expected observation |
| --- | --- | --- |
| `character-static.fbx` | Character mesh and skeleton, zero clips | The character is visible; no animation item appears |
| `motion-only.fbx` | Animated skeleton, no mesh | The viewer supplies and labels its default preview character |
| `character-animated.fbx` | Character mesh, skeleton, and baked Dance clip | The file's own character and native FBX clip appear |

依次单独打开三个文件，并在每次比较前重置。纯动作文件中没有人物网格；Viewer 显示的人物由网站额外提供。静态原始 FBX 与转换后的动画 FBX 使用不同的骨架命名和坐标约定，不能直接把一份文件的曲线绑定到另一份骨架。

[Detailed guide](https://3dretarget.com/guides/fbx-animation-not-playing-after-export#reproducible-case) · [中文指南](https://3dretarget.com/zh/guides/fbx-animation-not-playing-after-export#reproducible-case) · [Recording](../../recordings/fbx-geometry-vs-animation.webm)
