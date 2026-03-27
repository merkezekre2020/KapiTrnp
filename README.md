# KapiTrnp 🚀

KapiTrnp is a GitHub Actions workflow that clones Mesa, builds the Turnip Vulkan driver, and publishes an AdrenoTools-ready release asset to GitHub Releases. 🎮

## ✨ What it does

- Clones the Mesa repository from the configured source.
- Sets up the Android NDK and a newer Meson toolchain.
- Builds the `freedreno` Turnip driver for Android aarch64.
- Packages the driver as a `.zip` file with `meta.json` for AdrenoTools.
- Uploads the zip to the repository Releases page. 📦

## 🛠️ Release format

Each release asset contains:

- `libvulkan_freedreno.so`
- `meta.json`

The zip is named with the Mesa ref and commit SHA so builds are easier to track. 🔎

## ▶️ How to run

Use the workflow dispatch button in GitHub Actions and provide:

- Mesa repository URL
- Mesa branch or tag
- Release tag

You can also trigger the workflow automatically by pushing a tag that matches the release pattern. 🏷️

## 📌 Notes

- The workflow is tuned for Android Turnip builds.
- The release asset is a zip file only.
- No checksum file is published.

## 🧩 Project status

This repository mainly exists as a build automation setup for Turnip release packaging. ✨
