# GoldenEye 007 N64 Aimbot Patch

A binary ROM patch for GoldenEye 007 (N64) that implements a screen-wide aimbot with auto-fire for single-player mode. The game already has a built-in "aim-assist" feature which locks onto enemies that are already near the crosshair - this existing logic has been "recycled" and modified to cover the entire field of view. The aim adjustment speed has also been increased, and unlike the original feature, the weapon now automatically fires when a target is acquired.

## Details

Increasing the threshold of the built-in auto-aim feature only requires a few simple patches to the existing MIPS instructions.

Adding the auto-fire feature was slightly more complicated. This additional logic required a trampoline, with the additional code inserted into unused ROM space. This new code cycles the trigger when the auto-aim feature is locked onto a target.

## Usage

For legal reasons, the modified ROM is not available to download directly.

You must first acquire the original ROM file:
`GoldenEye 007 (U) [!].z64`

SHA256: 2cdcec8a9f0cb6e36337f3ee39d8ad105dc8afa6ba1c02d466e8f5b771f9a162

SHA1: abe01e4aeb033b6c0836819f549c791b26cfde83

The bytes listed in [patched_bytes.txt](patched_bytes.txt) can then be applied to this ROM file.
