# GoldenEye 007 N64 Aimbot Patch

A binary ROM patch for GoldenEye 007 (N64) that implements a screen-wide aimbot with auto-fire for single-player mode. The game already has a built-in "aim-assist" feature which locks onto enemies that are already near the crosshair - this existing logic has been "recycled" and modified to cover the entire field of view. The aim adjustment speed has also been increased, and unlike the original feature, the weapon now automatically fires when a target is acquired.

## Details

Increasing the threshold of the built-in auto-aim feature only requires a few simple patches to the existing MIPS instructions.

Adding the auto-fire feature was slightly more complicated. This additional logic required a trampoline, with the additional code inserted into unused ROM space. This new code cycles the trigger when the auto-aim feature is locked onto a target.

## Usage

For legal reasons, the modified ROM is not available to download directly from this repository.

You must first acquire the original ROM file:
`GoldenEye 007 (U) [!].z64`

SHA256: 2cdcec8a9f0cb6e36337f3ee39d8ad105dc8afa6ba1c02d466e8f5b771f9a162

SHA1: abe01e4aeb033b6c0836819f549c791b26cfde83

### Applying the Patch

An IPS patch file is provided: [GoldenEyeAimbot.ips](https://github.com/x86matthew/GoldeneyeAimbot/raw/main/GoldenEyeAimbot.ips)

You can apply this patch using [ROM Patcher JS](https://www.marcrobledo.com/RomPatcher.js/)

Select the original ROM and the IPS file

### Patched ROM Hashes

After applying the patch, verify your ROM against these hashes:

SHA256: d54698378dc7c84ff72ce0f38a02c0249d1c65f15e7436525870212527eeb53c

SHA1: 942a5746d3b17441e4a3c236f2549585f3cb9c3d
