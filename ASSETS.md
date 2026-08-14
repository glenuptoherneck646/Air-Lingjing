# 📦 Asset Distribution

<a href="./ASSETS.md"><strong>English</strong></a> · <a href="./ASSETS.zh-CN.md"><strong>简体中文</strong></a>

Large Unreal maps, Blueprints, meshes, materials, textures, particles, fonts, and other binary assets are distributed separately through Hugging Face:

```text
Coming soon / 即将上传
```

The public Hugging Face URL and checksum manifest will be added here after upload.

## Recommended Asset Repository

```text
EmbodyIntelligence-Assets/
├── Content/
│   ├── ArtRes/
│   ├── Program/
│   ├── StarterContent/
│   └── Waterfalls/
├── README.md
└── MANIFEST.sha256
```

## Download

```text
Coming soon / 即将上传
```

Verify `MANIFEST.sha256` if the asset repository provides it.

## Install

Close Unreal Editor and back up the host project's existing `Content/` directory. Merge the downloaded `Content/` into the host project:

```text
HostProject/
├── HostProject.uproject
├── Content/                         # Hugging Face assets
└── Plugins/
    └── EmbodyIntelligence/          # GitHub plugin source
```

Linux/macOS:

```bash
cp -a EmbodyIntelligence-Assets/Content/. <HostProject>/Content/
```

PowerShell:

```powershell
Copy-Item `
  -Path .\EmbodyIntelligence-Assets\Content\* `
  -Destination <HostProject>\Content\ `
  -Recurse -Force
```

Do not copy these assets into `HostProject/Plugins/EmbodyIntelligence/Content/`. The C++ source references `/Game/...`, which resolves against the host project's `Content/` mount.

Before publishing the asset repository, document its matching source release, Unreal/Cesium versions, checksums, third-party sources, licenses, and redistribution terms.
