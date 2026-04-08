# AuraConv 🎛️

[![Deploy to Cloudflare Pages](https://img.shields.io/badge/Deploy-Cloudflare%20Pages-orange?style=flat-square&logo=cloudflare)](https://developers.cloudflare.com/pages/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)

> A mobile-optimized convolution filter web app for experimental audio processing. Transform live microphone input or generated noise using sample-accurate blocking, spatial rotation, and convolution reverb—all in a single HTML file.

![AuraConv Screenshot](https://via.placeholder.com/600x400/0a0a0a/667eea?text=AuraConv+Interface)

## Overview

AuraConv is a browser-based audio processor that applies **sample-accurate interval blocking** to audio sources, creating rhythmic gaps or chopped bursts, then processes the result through a **convolution reverb** and optional **3D spatial rotation**. Originally designed as a creative tool for sound design and experimental music, it runs entirely client-side and is optimized for mobile devices and Cloudflare Pages hosting.

**Key Concept:** Every *N* samples (50, 100, 200, etc.), the audio is either blocked (creating silence gaps) or allowed through (creating isolated bursts), depending on polarity settings. The resulting texture is then smeared and spatialized using convolution reverb and HRTF-based 3D audio.

## Features

- 🎤 **Dual Audio Sources**: Toggle between live microphone input or built-in white noise generator
- ⏱️ **Sample-Accurate Blocking**: Block intervals at 50, 100, 200, 500, 1000, or 2000 samples
- 🎚️ **Variable Block Duration**: Control gap/burst length from 10% to 90% of the interval
- 🔄 **Polarity Inversion**: Switch between "Silence Gaps" (normal) and "Chopped Bursts" (inverted) modes
- 🌀 **3D Circular Rotation**: HRTF-based spatial audio rotation around the listener's head (0.1–2.0 Hz)
- 🏛️ **Convolution Reverb**: Adjustable decay time (1–10 seconds) for ambient tail generation
- 📱 **Mobile-First**: Touch-optimized controls, responsive layout, viewport-locked scaling
- ⚡ **Single File Deployment**: One HTML file—no build process, no dependencies
- 🎨 **Real-time Visualization**: Dynamic spectrum analyzer with mode-specific color coding

## Installation & Deployment

### Cloudflare Pages (Recommended)
1. Download `index.html` from this repository
2. Log in to [Cloudflare Pages](https://pages.cloudflare.com/)
3. Create a new project → Upload the `index.html` file
4. Your app is live instantly with HTTPS

### Local Usage
Simply open `index.html` in any modern web browser. No server required.

```bash
# Optional: local server for testing
npx serve .
# or
python -m http.server 8000
