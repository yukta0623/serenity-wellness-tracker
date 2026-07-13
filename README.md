# serenity-wellness-tracker
Serenity — a neumorphic wellness app for mood logging, habit tracking, and guided 4-7-8 breathing exercises, with data persisted locally via localStorage. Soft, tactile UI in pink, lavender &amp; mint.

# Serenity — Wellness & Mood Tracker

A neumorphic-styled wellness and mood tracking app built with pure HTML5, CSS3, and vanilla JavaScript, with all data persisted locally in the browser.

![Made with HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![Made with CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![Made with JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

## 🔗 Live Demo

https://yukta0623.github.io/serenity-wellness-tracker/

## ✨ Overview

Serenity is a single-page application for logging daily mood, tracking habits, and practicing guided breathing — styled with a soft, tactile **neumorphic** ("soft UI") design language of pink, lavender, and mint tones. All data (mood logs and habits) is stored in the browser via `localStorage`, so a user's history persists between visits without any backend.

## 🚀 Features

- **Mood logging:** select a mood/emoji, add an optional note, and save a timestamped entry (`srnMoodLog` in `localStorage`)
- **7-day bar chart:** visualises mood scores over the last week
- **Habit tracker:** toggle daily habits with automatic streak counting (`srnHabits` in `localStorage`)
- **Wellness metric sliders** for tracking subjective daily metrics
- **Guided breathing exercise** using the 4-7-8 technique, with an animated circle that:
  - expands and turns pink during the inhale phase
  - holds steady with a neutral colour during the hold phase
  - contracts and turns mint during the exhale phase
- **Mood history filtering** by date/tag
- **Daily streak calculation** for consistent habit completion
- Neumorphic UI throughout: raised, inset, and button shadow states for a soft, pressable feel

## 🎨 Design System

**Neumorphic shadow system**
| Shadow | Effect |
|---|---|
| `--shadow-sm` (raised) | Elements appear to float above the surface |
| `--shadow-in` (inset) | Elements appear pressed into the surface (active/selected state) |
| `--shadow-btn` (button) | Stronger raised shadow for interactive buttons |

**Colour palette:** soft pink, lavender, and mint tones layered over a warm off-white background (`#fdf6fb`), designed to feel calm and non-clinical.

## 🧠 Technical Highlights

- **Local persistence:** `srnMoodLog` (array of `{ mood, score, emoji, note, timestamp, id }`) and `srnHabits` (array of `{ name, done, streak }`) are read from and written to `localStorage` on every change.
- **Mood submission flow:** validates that a mood was selected → builds a log entry → prepends it to the array (newest first) → persists to `localStorage` → re-renders the history list, bar chart, and stats counters → resets the form with a confirmation toast.
- **Breathing animation:** a single circle element is driven through inhale/hold/exhale phases via CSS transforms (`scale(1.2)` → static → `scale(0.88)`) and colour transitions timed to the 4-7-8 breathing technique.

## 🗂️ Project Structure

```
serenity-wellness-tracker/
├── index.html          # Entire app — markup, styles, and script in one file
├── README.md
├── LICENSE
└── .gitignore
```

## 🔮 Future Improvements

Documented directly from the project's original planning notes:

- Cloud sync via Firebase or Supabase for cross-device access
- Weekly and monthly mood trend charts using Chart.js or D3
- Push notification reminders for daily mood check-ins
- Export mood data as CSV or PDF
- Custom mood labels and emoji selection
- Dark mode toggle with a separate neumorphic shadow set
- Habit reset timer that resets "done" states at midnight
- Mood correlation analysis (e.g. does more sleep correlate with better mood?)
- Progressive Web App (PWA) manifest for home-screen install
- Accessibility improvements: ARIA labels, keyboard navigation

## 👤 Author

**Yukta Brahmankar**
Student, Walchand College of Engineering, Sangli

## 📄 License

This project is licensed under the [MIT License](LICENSE).
