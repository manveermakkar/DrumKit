# 🥁 Drum Kit

An interactive browser-based drum kit that lets you play drum sounds using your **keyboard** or by **clicking buttons** on screen. Built with vanilla HTML, CSS, and JavaScript.

---

## 🎬 Demo

Seven drum pads are displayed on screen, each mapped to a keyboard key. Press a key or click a pad to trigger the corresponding drum sound with a visual animation.

---

## 🚀 Features

- **Keyboard Support** — Press keys `W`, `A`, `S`, `D`, `J`, `K`, `L` to play drum sounds instantly.
- **Click Support** — Each on-screen button is fully clickable for mouse/touch interaction.
- **Visual Feedback** — Active buttons animate with a glowing press effect (`box-shadow` + reduced opacity) for 100ms on every hit.
- **7 Unique Drum Sounds** — Covers toms, snare, crash cymbal, and kick bass.
- **Custom Drum Images** — Each pad displays a background image of the corresponding drum/cymbal instrument.
- **Stylish UI** — Dark navy theme with pink accents, bold typography using the *Arvo* font, and glowing text shadows.

---

## 🥁 Drum Pad Mapping

| Key | Instrument     | Sound File           |
|-----|----------------|----------------------|
| `W` | Tom 1          | `sounds/tom-1.mp3`   |
| `A` | Tom 2          | `sounds/tom-2.mp3`   |
| `S` | Tom 3          | `sounds/tom-3.mp3`   |
| `D` | Tom 4          | `sounds/tom-4.mp3`   |
| `J` | Snare          | `sounds/snare.mp3`   |
| `K` | Crash Cymbal   | `sounds/crash.mp3`   |
| `L` | Kick Bass      | `sounds/kick-bass.mp3` |

---

## 📁 Project Structure

```
drum-kit/
├── index.html          # Main HTML structure
├── styles.css          # Styling and drum pad themes
├── index.js            # Core interactivity and sound logic
├── images/
│   ├── tom1.png        # Background image for W pad
│   ├── tom2.png        # Background image for A pad
│   ├── tom3.png        # Background image for S pad
│   ├── tom4.png        # Background image for D pad
│   ├── snare.png       # Background image for J pad
│   ├── crash.png       # Background image for K pad
│   ├── kick.png        # Background image for L pad
│   └── drumIcon.png    # Browser tab favicon
└── sounds/
    ├── tom-1.mp3
    ├── tom-2.mp3
    ├── tom-3.mp3
    ├── tom-4.mp3
    ├── snare.mp3
    ├── crash.mp3
    └── kick-bass.mp3
```

---

## ⚙️ How It Works

### Event Listeners
The JavaScript sets up two types of event listeners:

1. **Click Events** — A loop iterates over all `.drum` button elements and attaches a click listener to each. When clicked, the button's `innerHTML` (the key letter) is passed to both `makeSound()` and `buttonAnimation()`.

2. **Keypress Events** — A `keypress` listener on the `document` captures the pressed key and passes `event.key` to the same two functions.

### `makeSound(key)`
A `switch` statement maps the incoming key to the correct audio file. A new `Audio` object is created and `.play()` is called immediately.

### `buttonAnimation(currentKey)`
Uses the key string as a CSS class selector (e.g. `.w`, `.j`) to find the matching button, adds the `pressed` class (which applies a glowing box shadow and reduced opacity), then removes it after **100ms** using `setTimeout` — creating a quick visual flash on every hit.

---

## 🛠️ Tech Stack

| Technology | Usage |
|---|---|
| **HTML5** | Page structure and button layout |
| **CSS3** | Styling, drum pad themes, animations |
| **Vanilla JavaScript** | Event handling, audio playback, DOM manipulation |
| **Google Fonts** | *Arvo* font for headings and button labels |
| **Web Audio API** | Native browser `Audio` object for sound playback |

---

## 🏁 Getting Started

1. **Clone or download** the repository.
2. Ensure the `sounds/` and `images/` folders are present with all required files.
3. Open `index.html` in any modern browser.
4. Start drumming — no installation or dependencies required!

> ⚠️ Some browsers may block autoplay audio. If sounds don't play, try clicking on the page first to satisfy the browser's user-interaction requirement.

---

## 🎨 Design Highlights

- **Color Palette:** Dark navy (`#283149`) background, off-white (`#DBEDF3`) text, vibrant pink (`#DA0463`) accents.
- **Button Style:** Large 150×150px rounded squares with a thick bordered outline, designed to look like physical drum pads.
- **Typography:** *Arvo* serif font with layered text shadows for a bold, musical aesthetic.

---

## 👨‍💻 Author

Made with ❤️ by **Manveer Makkar** 😎
