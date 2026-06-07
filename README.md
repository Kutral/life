# ⌛ Memento Mori — Your Life in Weeks

> *"You could leave life right now. Let that determine what you do and say and think."* — Marcus Aurelius

**Memento Mori** is an interactive, highly-optimized visual mirror of your lifetime. By rendering your life expectancy as a single grid of dots (weeks, months, or years), it transforms abstract time into a concrete count—revealing the weeks you have already spent and the precious ones that remain.

---

## ✨ Features

*   **The Grid of Life:** A single-screen visual representation of your entire life. Every dot is one week.
*   **Live Lifespan Realisation:** Watch the seconds of your life drain in real-time alongside heartbeats and breaths.
*   **The Tail End:** A visceral countdown of how many summers, full moons, birthdays, and weekends you have left to experience.
*   **Aesthetic & Modern Design:** Elegant typography, responsive dark modes, glassmorphism card layouts, and subtle spotlight cursor effects.
*   **Fully Private:** Zero database, zero tracking. All inputs (name, date of birth) are saved locally on your device via `localStorage`.

---

## 🚀 Performance Optimizations

To ensure a premium feel, the application is optimized for smooth, 60fps interaction on both desktop and mobile screens:

*   **Batch Rendered Canvas:** The onboarding background runs a live field of 2,000+ interactive dots. Static dots are batch-rendered into a single path to reduce draw calls from ~3,000 to <150 per frame.
*   **Zero Layout Thrashing:** Mathematically derives grid positioning and caches element dimensions on hover, avoiding expensive synchronous layout reflows (`offsetTop`/`offsetWidth` queries).
*   **CSS Containment:** Localizes rendering inside the calendar grid using `contain: layout paint;` to prevent DOM interactions from reflowing the main layout.
*   **Organic Animations:** Fake loader transition is shortened to `2.4s` using a `cubic-bezier(0.25, 1, 0.5, 1)` easing curve for progress indicators and SVGs.

---

## 🛠️ Tech Stack

*   **Core:** HTML5, CSS3 (Vanilla), JavaScript (Vanilla)
*   **Fonts:** Fraunces (serif headers), Newsreader (serif body), JetBrains Mono (monospaced metrics)
*   **Deployment:** GitHub Pages (automatic builds)

---

## ⚙️ Running Locally

Since the project is built with pure, serverless vanilla web technologies, running it locally requires no build steps or dependencies:

1. Clone the repository:
   ```bash
   git clone https://github.com/Kutral/life.git
   ```
2. Navigate into the directory and open `index.html` in any browser, or start a local HTTP server:
   ```bash
   npx serve
   ```

---

*Memento Mori · Created to remind you to live today.*
