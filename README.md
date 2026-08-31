# Spider
God's Eye View Spatial Intelligence Platform

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](./LICENSE) [![Build](https://img.shields.io/github/actions/workflow/status/access403/gods-eye-view/ci.yml?branch=main)](https://github.com/access403/gods-eye-view/actions) [![Node](https://img.shields.io/badge/node-%3E%3D18-blue)](https://nodejs.org/)

## Overview
Spider is a browser-first spatial intelligence console that renders live public telemetry (aircraft ADS‑B, ships AIS, satellite TLEs, seismic events, traffic cameras, and weather overlays) onto a photorealistic 3D tile globe. It provides real-time situational awareness, filtering, time-travel playback, and a voice-driven control plane for hands-free querying and commands.

## Key Visual Layers & Sensors
- Aircraft (ADS‑B): Live aircraft positions, altitude, heading, speed, callsign, and flight plan overlays (OpenSky / ADSB aggregators).
- Ships (AIS): Vessel positions, MMSI, callsign, destination, and track history (AISStream / AISHub).
- Satellites (TLE): Real-time propagated orbital tracks from TLE sources (Celestrak) with pass predictions.
- Earthquakes: USGS feeds rendered as event points and magnitude heatmaps.
- Public CCTV: Geolocated camera registry with optional thumbnails/streams (obeying source TOS).
- Weather & Overlays: Precipitation, clouds, and wind raster/vector overlays from OpenWeatherMap or similar.

## Prerequisites & API Key Guide
- 🟢 Zero-config public feeds: USGS, Celestrak (TLE), many camera registries.
- 🟡 Free keys / rate-limited: OpenSky, OpenWeatherMap, TomTom (traffic).
- 🔴 Metered / commercial: Cesium Ion, Google 3D Tiles/Maps, OpenAI Realtime voice.

Create a .env from .env.example and fill required keys for the features you want.

## Quickstart & Setup
1. Clone the repo and change directory:

```bash
git clone https://github.com/access403/gods-eye-view.git
cd gods-eye-view
```

2. Install dependencies:

```bash
npm install
```

3. Copy configuration and start dev server:

```bash
cp .env.example .env
# edit .env to add any keys you need
npm run dev
# open http://localhost:5173
```

## Interactive Controls
- Mouse: Orbit, pan, zoom (Cesium controls)
- Space: Toggle live updates
- L: Toggle layer legend
- F: Toggle filters panel
- C: Center on selected entity
- P: Toggle playback (time scrubbing)
- V: Toggle voice console

Visual modes: NVG (night-vision), FLIR (thermal palette), Cockpit mode (HUD overlays)

Voice examples:
- "Show aircraft near San Francisco"
- "Track flight KL123"
- "Highlight vessels over 10,000 tons"
- "Set overlay to NVG"

## Team & Credits
- Team: Team Spider
- Team Lead: Jhimit Chakma
- Contributors: Udit Nath, Pahar Murasing
- Upstream: Based on God's Eye View (access403/gods-eye-view)

## License & Contributing
- License: MIT
- Contributing: Fork, create a kebab-case feature branch, run linters, include tests when appropriate, and open a PR against main.

