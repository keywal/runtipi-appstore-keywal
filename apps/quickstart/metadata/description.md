<!--logo-start-->
![Quickstart Logo](https://github.com/Kometa-Team/Quickstart/raw/master/static/images/logo.webp)
<!--logo-end-->

<!--body1-start-->
## Welcome to Kometa Quickstart

## ✨ Features

Kometa Quickstart is more than just a YAML generator — it’s a full interactive environment for configuring, validating, and running Kometa. Key features include:

### Multiple Ways to Run Quickstart
- **Local Python:** Works on Windows, macOS, and Linux
- **Frozen Builds:** Precompiled executables for Windows, macOS, and Linux (no Python required)
- **Docker Image:** Official image on Docker Hub with persistent `/config` volume support
- **Branch Support:** Choose between `master` (stable) and `develop` (bleeding-edge) branches for every runtime option

### Safe Playground Mode
- **Plex Test Libraries:** Downloadable from the start page so you can experiment without touching production libraries
- **No Risk to Production:** All Quickstart data, credentials, and configs are stored locally

### Config Management & History
- **SQLite-Backed Storage:** All configs and page data are stored in a database, so you can switch between configs at any time
- **Automatic Backups:** Every config is saved as a versioned `.yml` file for historical reference
- **Download & Run Anywhere:** Final configs can be downloaded and run outside Quickstart if preferred

### Guided, Validated Workflow
- **Step-by-Step Pages:** Each section validates its own data, giving you instant feedback before proceeding
- **Library Telemetry:** Pulls real Plex server data (Plex Pass status, library types, agent/scanner compatibility)
- **Dynamic Toggles & Templates:** Rich UI for enabling collections, overlays, and builder template variables

### Built-in Kometa Runner
- **One-Click Execution:** The final page creates a Kometa virtual environment (if needed), installs dependencies, and runs `kometa.py` against the generated config
- **Run Command Builder:** Dynamically builds and previews CLI commands with flags like `--run`, `--operations-only`, `--times`, etc.
- **Process Management:** Start, stop, and monitor Kometa runs directly from the web interface

### Live Previews & Assets
- **Overlay Preview Generator:** Combines overlays and template variables into real-time preview images
- **Custom Artwork Uploads:** Drag-and-drop or fetch library images from a URL so you can see what the overlays look like on your favorite poster.

### Automatic Updates
- **Quickstart Self-Updater:** One-click update to latest master or develop branch
- **Kometa Sync:** Option to pull and update Kometa itself (nightly/master) before running


Kometa Quickstart is a guided Web UI that helps you create a Configuration File for use with Kometa.

Special thanks to [meisnate12](https://github.com/meisnate12), [bullmoose20](https://github.com/bullmoose20), [chazlarson](https://github.com/chazlarson), and [Yozora](https://github.com/yozoraXCII) for their contributions to this tool.

## Table of Contents

- [Welcome to Kometa Quickstart](#welcome-to-kometa-quickstart)
- [✨ Features](#-features)
  - [Multiple Ways to Run Quickstart](#multiple-ways-to-run-quickstart)
  - [Safe Playground Mode](#safe-playground-mode)
  - [Config Management \& History](#config-management--history)
  - [Guided, Validated Workflow](#guided-validated-workflow)
  - [Built-in Kometa Runner](#built-in-kometa-runner)
  - [Live Previews \& Assets](#live-previews--assets)
  - [Automatic Updates](#automatic-updates)
- [Table of Contents](#table-of-contents)
- [Prerequisites](#prerequisites)
- [Installing Quickstart](#installing-quickstart)
- [1 - Installing on Windows](#1---installing-on-windows)
- [2 - Installing on Mac](#2---installing-on-mac)
- [3 - Installing on Ubuntu (Linux)](#3---installing-on-ubuntu-linux)
- [4 - Running in Docker](#4---running-in-docker)
  - [`docker run`](#docker-run)
  - [`docker compose`](#docker-compose)
- [5 - Installing locally](#5---installing-locally)
  - [Windows:](#windows)
  - [Linux/Mac:](#linuxmac)
  - [Debugging \& Changing Ports](#debugging--changing-ports)