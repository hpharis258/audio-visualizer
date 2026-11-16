Build a music visualiser web app in a single file called index.html (HTML, CSS and JavaScript, no frameworks, no build step, no external libraries).

What it does:
- The user drags and drops (or picks) an audio file (MP3 or WAV) and an image (JPG or PNG, e.g. album cover).
- It shows a live preview on a canvas: the image in the centre with the visualiser effects around it, reacting to the music.
- The user can export the result as a video file with the audio included.

Visual effects (selectable from a dropdown):
1. Circular bars: frequency bars arranged in a circle around the image
2. Classic bars: bars along the bottom of the screen
3. Waveform: a glowing line that follows the audio waveform
4. Particles: particles that burst outward on bass hits
The image should pulse (scale up slightly) with the bass in every mode.

Customisation panel:
- Colour picker for the bars/glow (default neon cyan)
- Background: blurred, darkened version of the uploaded image
- Text fields for song title and artist name, shown at the bottom
- Resolution presets: 1920x1080 (YouTube), 1080x1920 (Shorts/TikTok), 1080x1080 (Instagram)

Export:
- Use the Web Audio API AnalyserNode for the audio data.
- Record the canvas with canvas.captureStream(60) combined with the audio track using MediaRecorder.
- Use MP4 if MediaRecorder.isTypeSupported('video/mp4') is true, otherwise WebM.
- Export plays the song from the start to the end, then automatically downloads the video file.
- Show a progress bar and the time remaining while exporting.

Design: dark theme, modern and clean, controls on the left, large preview on the right.
Make sure everything works by opening index.html directly in Chrome.