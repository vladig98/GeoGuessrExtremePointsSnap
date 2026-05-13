# GeoGuessr Cardinal Snap - Stealth HUD

A Tampermonkey userscript designed for advanced GeoGuessr training. This script intercepts your guesses and automatically snaps your coordinate to the absolute furthest North, South, East, or West point of the country you clicked in. It also features a "Random" mode for unpredictable directional snapping. 

This tool is built to help you learn the exact longitudinal and latitudinal reach of every country on Earth.

## 🎯 Features & Accuracy

* **Hand-Picked Precision:** Every single coordinate in this script was meticulously hand-picked and verified. The data accounts for complex maritime borders, exclaves, and territorial disputes.
* **Invisible Extremes:** Do not be surprised if your guess snaps to the middle of the ocean! Many countries' true extreme points are tiny offshore islets, reefs, or lone maritime beacons that do not render on standard Google Maps zoom levels. 
* **Mainland vs. All Mode:** Use the HUD to toggle between "Mainland Bound" (snaps to continental borders only) and "All" (includes overseas territories and distant islands).
* **Stealth HUD:** A lightweight, non-intrusive UI that hovers in the corner of your screen and expands only when you need to configure your snap direction.

## ⚠️ Important Gameplay Note (The UN Rule)

This script relies on GeoGuessr's internal geocoding API to determine which country you clicked on. **GeoGuessr's API strictly recognizes UN Member States.** Because of this limitation, clicking on non-UN entities or overseas territories (such as **Taiwan, Greenland, Guam, Puerto Rico, etc.**) will return an API error. When this happens, the script will fallback and snap your guess to the absolute edge of the Earth (the North/South pole or the Antimeridian). 

**The Workaround:** To ensure the script correctly identifies the sovereign nation, **always click on the mainland** of the country you are trying to guess, even if you want your final snapped point to be an overseas territory.

## ⚙️ Installation & Required Settings

To use this script, you must have the [Tampermonkey](https://www.tampermonkey.net/) extension installed in your browser.

**CRITICAL TAMPERMONKEY SETTINGS:**
For this script to function correctly, you must enable two specific settings in your browser's extension manager:
1. Go to your browser's extension settings (e.g., `chrome://extensions/` for Chrome/Brave).
2. Find **Tampermonkey** and click **Details**.
3. Toggle on **Allow access to file URLs**.
4. Make sure Tampermonkey itself is enabled, and the script is toggled **ON** in the Tampermonkey dashboard.

### How to Install
1. Open the Tampermonkey dashboard and click the **Create a new script** tab (the `+` icon).
2. Delete the default template code.
3. Paste the entirety of the `GeoGuessr Cardinal Snap` script into the editor.
4. Go to `File` > `Save` (or press `Ctrl+S` / `Cmd+S`).
5. Open GeoGuessr and start training!
