# Distance Tracker

A lightweight progressive web app for measuring straight-line GPS distance from a set start point. Log and export timestamped readings — no app store required.

## Installation

**iPhone:**

1. Open the link in **Safari** (Chrome and other browsers do not support all required GPS features on iOS)
1. Bookmark it or keep the tab open for easy access

> **Note:** Adding to Home Screen is not recommended on iPhone — iOS restricts location access for home screen web apps.

**Android:**

1. Open the link in **Chrome** or **Samsung Internet**
1. Tap the menu and select **“Add to Home Screen”** for a full-screen app experience

## Usage

1. Open the app and wait for the signal accuracy indicator to turn **green**
1. Tap **Set Start Point** to lock in your origin location
1. Move around — distance updates live on screen
1. Tap **Log Distance** at any point to record a timestamped reading
1. Tap **Export Log** at the end of your session to download a `.txt` file of all recorded entries

## Signal Accuracy

The accuracy indicator shows the GPS margin of error and uses a traffic light system:

|Color   |Accuracy          |Meaning                    |
|--------|------------------|---------------------------|
|🟢 Green |+/- 16ft or better|Good to go                 |
|🟠 Orange|+/- 17–30ft       |Usable, some drift possible|
|🔴 Red   |+/- 31ft or worse |Wait for a better fix      |

Always wait for green before setting your start point for the most reliable readings.

## Limitations

- **Screen must stay on** — GPS updates pause if the screen locks or you switch apps. Keep the screen active for the duration of your session.
- **Straight-line distance only** — measures the direct distance from your start point, not the total path traveled.
- **iPhone: use Safari, do not add to Home Screen** — other browsers lack the required GPS APIs on iOS, and iOS restricts location access for home screen web apps. Open directly in Safari for reliable location access.
- **Android: use Chrome or Samsung Internet** — adding to Home Screen works correctly on Android.
- **Accuracy varies** — signal quality depends on your environment. Open sky gives the best results; dense buildings or tree cover will reduce accuracy.

## Export Format

Exported logs are saved as plain `.txt` files with one entry per line:

```
-- Session: 5/3/2026 7:08:01 PM --
[19:08:01] 0 ft
[19:10:22] 142 ft
[19:14:05] 0.31 mi
```

Files are saved to your Downloads folder or can be shared via the iOS share sheet.

## Tips

- Disable auto-lock in **Settings > Display & Brightness > Auto-Lock** before a long session
- Keep screen brightness up — low power mode can throttle GPS
- If accuracy stays red indoors, try moving near a window or stepping outside briefly