
## Overview

This application continually searches your media libraries for missing content and items that need quality upgrades. It automatically triggers searches for both missing items and those below your quality cutoff. It's designed to run continuously while being gentle on your indexers, helping you gradually complete your media collection with the best available quality.

For detailed documentation, please visit our [Wiki](https://github.com/plexguide/Huntarr/wiki).


## How It Works

### 🔄 Continuous Automation Cycle

#### 1️⃣ Connect & Analyze
Huntarr connects to your Sonarr/Radarr/Lidarr/Readarr instance and analyzes your media library to identify both missing content and potential quality upgrades.

#### 2️⃣ Hunt Missing Content
- 📊 **Smart Selection:** Choose between random or sequential processing
- 🔍 **Efficient Refreshing:** Optionally skip metadata refresh to reduce disk I/O
- 🔮 **Future-Aware:** Automatically skip content with future release dates
- 🎯 **Precise Control:** Set exactly how many items to process per cycle

#### 3️⃣ Hunt Quality Upgrades
- ⬆️ **Quality Improvement:** Find content below your quality cutoff settings
- 📦 **Batch Processing:** Configure exactly how many upgrades to process at once
- 📚 **Large Library Support:** Smart pagination handles even massive libraries
- 🔀 **Flexible Modes:** Choose between random or sequential processing

#### 4️⃣ State Management
- 📝 **History Tracking:** Remembers which items have been processed
- 💾 **Persistent Storage:** State data is saved in the `/config` directory
- ⏱️ **Automatic Reset:** State is cleared after your configured time period (default: 7 days)

#### 5️⃣ Repeat & Rest
Huntarr waits for your configured interval (adjustable in settings) before starting the next cycle. This ensures your indexers aren't overloaded while maintaining continuous improvement of your library.

## Web Interface

Huntarr's live homepage will provide you statics about how many hunts have been pursed regarding missing media and upgrade searches! Note: Numbers reflected are but all required for testing... damn you Whisparr!

<p align="center">
  <img width="100%" alt="image" src="https://github.com/user-attachments/assets/db725ad6-3009-4835-ab44-289dda80d385" />
  <br>
  <em>Homepage</em>
</p>

Huntarr includes a real-time log viewer and settings management web interface that allows you to monitor and configure its operation directly from your browser.

<p align="center">
  <img width="100%" alt="image" src="https://github.com/user-attachments/assets/438e2013-2a54-4cf2-8418-63b0c6124730" />
  <br>
  <em>Logger UI</em>
</p>

### How to Access

The web interface is available on port 9705. Simply navigate to:

```
http://YOUR_SERVER_IP:9705
```

The URL will be displayed in the logs when Huntarr starts, using the same hostname you configured for your API_URL.

### Web UI Settings

The web interface allows you to configure all of Huntarr's settings:

<p align="center">
  <img width="930" alt="image" src="https://github.com/user-attachments/assets/06003622-0af3-4398-a46d-0fa4fb1f455b" />
  <br>
  <em>Settings UI</em>
</p>

