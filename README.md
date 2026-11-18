# ImgCompress for TerraMaster TOS 7

ImgCompress is a self-hosted web application for compressing images, converting 70+ formats, editing images, upscaling with AI, and removing backgrounds, optimized for deployment on TerraMaster TOS 7 NAS systems.

## 1. Overview & Source Repository

* **Application Name:** ImgCompress
* **Container Image Source:** Pulled directly from official Docker Hub repository (`karimz1/imgcompress:v1.0.0`)
* **Application Storage Path:** `/Volume1/DockerAppData/imgcompress-outkastm`
* **Official Upstream Project:** <https://imgcompress.karimzouine.com>
* **Upstream Source Repository:** <https://github.com/karimz1/imgcompress>
* **Support:** <https://tmnascommunity.eu/forums/topic/imgcompress-docker>

## 2. Port & Network Configuration

* **Host Published Port:** `3570`
* **Internal Container Port:** `5000`
* **Protocol:** HTTP

Upon installation via the TOS App Center, the web interface is accessible at `http://<NAS_IP_ADDRESS>:3570`.

## 3. Persistent Data Directories

ImgCompress is stateless and processes all image files transiently inside the container without requiring external database storage. No persistent host volume mounts are required for operation; temporary runtime files remain isolated within `/Volume1/DockerAppData/imgcompress-outkastm` or container ephemeral storage and are cleared automatically.

## 4. Privacy Policy & Data Handling (Compliance Item 4)

This application strictly operates locally on your TerraMaster NAS with built-in AI models and zero external cloud dependencies.

* **Upstream Project & Privacy Overview:** <https://github.com/karimz1/imgcompress#privacy-by-design>

### Privacy & Telemetry Statements:

1. **No External Tracking / Telemetry:** ImgCompress processes all conversions, compression, AI upscaling, and background removal locally on your hardware and contains no telemetry, tracking, or analytics. It does not transmit images, personal data, or usage metrics to external servers.
2. **Local Processing & Storage:** All uploaded images and processed outputs remain exclusively on your local NAS device and never leave your local network.

## 5. Installation & Deployment Guide

### Installation via TOS App Center

1. Open **TOS App Center** on your TerraMaster NAS.
2. Search for the **ImgCompress** app and install it.
3. Launch the application or navigate directly to `http://<NAS_IP>:3570`.

## 6. License

* **Upstream Application:** Governed under the **GNU General Public License v3.0 (GPL-3.0)** (<https://github.com/karimz1/imgcompress/blob/main/LICENSE>).