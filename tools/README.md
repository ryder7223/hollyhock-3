# HHK3 Patcher

```bash
python3 tools/hollyhock.py extract roms/v02.01.2000.0000/OSupdateDLL.dll roms/v02.01.2000.0000/fw3069 path/to/v02.01.2000.0000/fw3070

python3 tools/hollyhock.py patch patches roms/v02.01.7002.0001/fw3070 roms/v02.01.7002.0001/hhk3070

python3 tools/hollyhock.py pack roms/v02.01.7002.0001/hhk3070 roms/v02.01.7002.0001/ResData3070_patch.bin roms/v02.01.7002.0001/OSupdateDLL.dll

```

## Patches

```
patches/
├── metadata.json
└── patch_name/
    ├── metadata.json
    └── patch_file.bin
```

First one is the `patch_metadata`
```yaml
patches_format_version: 1
fw3070_checksum: <hash of the firmware>
```

Second one is a `patchset_metadata`
```yaml
name: name_of_patch
patches: [
    file: patch_file.bin
    address: 0x8091FED0
]
```