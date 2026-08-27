# 3D motion and avatar viewer cases

Small, reproducible files for diagnosing common VRMA, FBX, and BVH viewer problems. Each case separates what is actually stored in a file from what a viewer may add for preview.

用于排查 VRMA、FBX 和 BVH 常见播放问题的最小可复现样例。每个案例都会区分“文件实际包含的内容”和“Viewer 为预览额外提供的内容”。

These are diagnostic examples, not universal importer certification. Reset the viewer between comparisons unless a case explicitly asks you to keep the current motion.

## Cases / 案例

| Case | Files | What it demonstrates | Guide | Recording |
| --- | --- | --- | --- | --- |
| [VRMA needs an avatar](cases/vrma-needs-avatar/) | `avatar.vrm`, `motion.vrma` | A VRMA contains motion, not a character mesh | [Guide](https://3dretarget.com/guides/what-is-a-vrma-file-and-how-to-open-it#reproducible-case) · [中文](https://3dretarget.com/zh/guides/what-is-a-vrma-file-and-how-to-open-it#reproducible-case) | [WebM](recordings/vrma-needs-avatar.webm) |
| [FBX geometry vs animation](cases/fbx-geometry-vs-animation/) | static character, motion-only, animated character | Geometry and animation are independent FBX contents | [Guide](https://3dretarget.com/guides/fbx-animation-not-playing-after-export#reproducible-case) · [中文](https://3dretarget.com/zh/guides/fbx-animation-not-playing-after-export#reproducible-case) | [WebM](recordings/fbx-geometry-vs-animation.webm) |
| [BVH motion and preview avatars](cases/bvh-avatar-preview/) | `walk-in-place.bvh`, separate rigged GLB | A BVH has hierarchy and motion channels, not a character mesh | [Guide](https://3dretarget.com/guides/free-bvh-animations-for-retargeting#reproducible-case) · [中文](https://3dretarget.com/zh/guides/free-bvh-animations-for-retargeting#reproducible-case) | [WebM](recordings/bvh-avatar-preview.webm) |
| [BVH root motion](cases/bvh-root-motion/) | travelling and in-place BVH | A controlled comparison where only horizontal root translation changes | [Guide](https://3dretarget.com/guides/fix-bvh-scale-axis-and-root-motion#reproducible-case) · [中文](https://3dretarget.com/zh/guides/fix-bvh-scale-axis-and-root-motion#reproducible-case) | [WebM](recordings/bvh-root-motion.webm) |

## Quick start / 快速开始

1. Download or clone this repository. For a stable snapshot, use [Viewer Cases v1.0.0](https://github.com/3dkit-online/3d-motion-avatar-viewer-cases/releases/tag/v1.0.0).
2. Open the README inside one case directory.
3. Use the linked online viewer, or import the files into your own target application.
4. Reset between files and compare the documented observations.

下载或克隆仓库后，进入对应案例目录阅读步骤。可以使用案例链接中的在线 Viewer，也可以在自己的目标软件中导入。比较不同文件前请先重置 Viewer，避免上一份模型或动作影响判断。

No build step or dependency installation is required. The online viewer processes selected files locally in the browser.

## Repository layout

```text
cases/
  vrma-needs-avatar/
  fbx-geometry-vs-animation/
  bvh-avatar-preview/
  bvh-root-motion/
recordings/
checksums.sha256
ATTRIBUTION.md
LICENSE
```

## Scope and limitations / 适用边界

- File extensions and filenames are hints, not proof of file contents or ecosystem compatibility.
- A playable timeline alone does not prove correct retargeting, pose semantics, root motion, or destination compatibility.
- The FBX files intentionally demonstrate three different content combinations; do not attach one rig's curves directly to another skeleton.
- The BVH avatar case uses a known GLB preview target. It does not claim universal compatibility with arbitrary avatars.
- The examples contain no Adobe Mixamo or pixiv/VRoid sample assets.

## License and provenance / 许可与来源

The example files and documentation are released under [CC0 1.0](LICENSE). Source and conversion details are recorded in [ATTRIBUTION.md](ATTRIBUTION.md). Attribution is appreciated but not required.

案例文件与文档采用 [CC0 1.0](LICENSE) 发布，素材来源和转换说明见 [ATTRIBUTION.md](ATTRIBUTION.md)。引用不是许可条件，但欢迎教程作者链接到本仓库或对应指南。

This license does not apply to the 3D Retarget Online website, its application source code, or unrelated assets.
