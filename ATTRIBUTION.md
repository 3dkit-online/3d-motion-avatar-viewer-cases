# Sources and conversion notes

All included example assets and accompanying documentation are released under CC0 1.0. This file records provenance even though attribution is not required.

## Characters

### Universal Animation Library 2 Standard Female Mannequin

- Creator: Quaternius
- Source: https://quaternius.com/packs/universalanimationlibrary2.html
- Included derivatives: `avatar.vrm`, `character-animated.fbx`
- Included original: `character-static.fbx` is the original `Mannequin_F.fbx`, renamed only
- Conversion: the original mesh, proportions, and materials were retained; canonical humanoid names were added and source animations were excluded before VRM/animated-FBX export by 3D Retarget Online

### Universal Animation Library Standard Mannequin

- Creator: Quaternius
- Source: https://quaternius.com/packs/universalanimationlibrary.html
- Included derivative: `avatar-ual1.glb`
- Conversion: the original mesh, proportions, and materials were retained; canonical humanoid names were added and source animations were excluded
- Role: an independent rigged preview avatar, not an output of the BVH file

## Motions

- Creator: Quaternius
- Source: https://quaternius.com/packs/universalanimationlibrary.html
- Clips: Dance and Walk
- Conversion: canonical normalization plus VRMA, BVH, and motion-only FBX export by 3D Retarget Online
- The animated FBX binds the canonical Dance motion to the UAL2 target's own rest skeleton

`walk-travel.bvh` preserves canonical Walk root travel. Both BVH variants share a constant vertical rebase that places the minimum hips offset at zero while preserving the vertical range. `walk-in-place.bvh` then sets only horizontal canonical hips translation to zero before the same BVH export. Timing, rotations, and vertical motion are preserved.

## Rights and warranties

No pixiv/VRoid sample avatar or Adobe Mixamo asset is included. No trademark, publicity, or other third-party rights are granted. No compatibility certification or fitness warranty is implied.
