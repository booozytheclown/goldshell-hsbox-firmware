# Goldshell HS Box Firmware Research

Independent community research into the **original, first-generation Goldshell HS Box** ASIC miner firmware, including reverse engineering, hardware configuration, recovery, thermal management, and firmware upgrade mechanisms.

## Recovery Firmware 2.2.3

| Property | Value |
|---|---|
| Manufacturer | Goldshell |
| Model | **HS Box (original / first generation)** |
| Firmware | 2.2.3 recovery image |
| Control Board | MCB_V5_4 (as identified by image filename) |
| Format | Raw IMG microSD recovery image |
| File size | 18,077,003 bytes |
| Purpose | Recovery and community firmware research |

**[Firmware Releases](https://github.com/booozytheclown/goldshell-hsbox-firmware/releases)** — download recovery image after release `recovery-2.2.3` is published.

**Compatibility warning:** This image is intended for the **original HS Box**, **not the HS Box II / HSBox2**, HS Box Pro, SC Box, or other Goldshell models. The `.img` is a raw microSD recovery image, **not a `.cpb` web-interface firmware update**. Do not upload this image through the miner's normal web firmware updater.

### SHA-256 Verification

Firmware: `burn-Goldshell-HSBox_MCB_V5_4-2.2.3.img`

SHA-256 recorded in the supplied hash file:

`3d3aac7fe59e0fb5cabd7c3a45038d1f5d26ed7e44e5aadf73a6290492cac704`

Linux verification (after placing the image and `.sha256` file together):

```bash
sha256sum -c burn-Goldshell-HSBox_MCB_V5_4-2.2.3.img.sha256
```

Windows PowerShell verification:

```powershell
Get-FileHash -LiteralPath ".\burn-Goldshell-HSBox_MCB_V5_4-2.2.3.img" -Algorithm SHA256
```

**Verification status:** SHA-256 was independently checked against the local recovery image and **matched the supplied hash record**. This does not independently prove manufacturer authenticity or safety. Hardware flashing has not been tested here.

For normal first-generation HS Box web updates, consult [Goldshell's official firmware repository](https://github.com/goldshellminer/firmware/tree/master/Handshake-%26-Siacoin-Miner/Goldshell-HSBox). Keep recovery images and normal `.cpb` firmware packages clearly distinguished.

## Research Objectives

- Reverse engineer the original HS Box recovery firmware.
- Document the embedded Linux filesystem and firmware architecture.
- Investigate firmware validation, signing, upgrading, and microSD recovery.
- Research fan speeds, thermal regulation, and ASIC control mechanisms.
- Explore Blake2b-related compatibility and performance improvements, with results clearly labeled as confirmed or experimental.
- Share reproducible technical findings and encourage community development.

## Contributing

Community contributions are welcome!

Use GitHub Issues to report discoveries, document firmware behavior, or propose improvements.

Submit Pull Requests for research documentation, independently developed tools, and reproducible analysis.

Please avoid publishing passwords, private keys, wallet data, miner credentials, serial numbers, or personally identifiable information. Do not assume a modified or cross-model firmware image is safe to flash.

## Disclaimer

This project is independent and is not affiliated with or endorsed by Goldshell.

Original firmware and manufacturer documentation remain subject to their respective intellectual property rights. This repository does not claim to license Goldshell's proprietary firmware under an open-source license.

Firmware modification and flashing carry risks, including hardware damage and device failure. Experimental work should be performed with appropriate safeguards and a working recovery path.

This repository does not guarantee firmware safety, authenticity, compatibility, or suitability for production hardware.
