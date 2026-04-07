AuraConv is a single-file, mobile-optimized web app designed for Cloudflare Pages. 

Key Features:
- Interval Blocking: Blocks every N samples (50, 100, 200, etc.) creating rhythmic gaps in the live microphone input
- Convolution Reverb: Applies a generated reverb tail to the blocked signal for ambient textures
- Real-time Visualization: Spectrum analyzer showing the processed audio output
- Mobile-First: Touch-optimized controls, responsive layout, and viewport-locked scaling
- Single File: Everything inline (HTML, CSS, JS) - just upload to Cloudflare Pages

How it works:
1. Grants microphone access
2. Processes audio through ScriptProcessorNode to zero-out samples at specified intervals (creating the "blocked" effect)
3. Passes through ConvolverNode with a generated impulse response for the reverb effect
4. Visualizes the output in real-time

The "taps" control lets you select how frequently audio is blocked (every 50, 100, 200+ samples), while the duration slider controls how long each block lasts (percentage of the interval).
