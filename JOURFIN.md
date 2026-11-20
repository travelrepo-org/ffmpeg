# ffmpeg for Jourfin

This repository is a fork of [BtbN/FFmpeg-Builds](https://github.com/BtbN/FFmpeg-Builds). Its branch `jourfin`
builds the ffmpeg that [Jourfin](https://github.com/travelrepo-org/jourfin) bundles as a fallback for decoding
and encoding videos, motion photos and HEIC photos, and publishes it as releases here, so Jourfin can pin stable
download addresses and SHA-256 checksums. It is not an official FFmpeg release and is not affiliated with the
FFmpeg project.

- Builds start by hand only (Actions → "Jourfin ffmpeg release" → Run workflow) with an exact ffmpeg tag, such
  as `n9.0.2`. There is no schedule and no build on push.
- Linux and Windows (x64, ARM64): static GPL builds by this repository's scripts, using upstream's public
  dependency images; each build records the image digest and the script commit.
- macOS (Apple silicon, Intel): built on GitHub's macOS runner with ffmpeg's own decoders and VideoToolbox only.
- Every release carries the corresponding source: the ffmpeg source archive, the build scripts, the dependency
  sources they download, the licence texts, a provenance file per build and `SHA256SUMS`.

The branch `master` follows upstream unchanged.
