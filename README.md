# Vibe Coding Book Prompt Programs

Small programs generated entirely from plain-English prompts to Claude, collected as companion examples for a book on vibe coding. Each folder holds the program exactly as it was generated, plus the prompt that produced it.

Every program is a single self-contained HTML file: no build step, no install. Clone the repo and open any `index.html` in a browser.

## Projects

| Project | What it does | Tech | Prompt |
|---|---|---|---|
| [Photographs Taken per 5 Years](photos-per-5-years/) | Bar chart of estimated photos taken worldwide every five years, 1975–2025, with a linear/log scale toggle | HTML + Chart.js (CDN) | [View](photos-per-5-years/README.md#prompt) |
| [Lit Cube](lit-cube/) | 3D cube lit by a colored point light, with sliders for cube orientation and light color, position and intensity | HTML + raw WebGL (no libraries) | [View](lit-cube/README.md#prompt) |

## The prompts

### 1. Photographs Taken per 5 Years

> Please generate a bar chart Visualizer of the number of photographs taken estimated in 5-year intervals for the last 50 years

### 2. Lit Cube

> Write a JavaScript program that shows a cube with a colored light source. Create slider parts that can change the orientation of the polygon.

## Running locally

```bash
git clone https://github.com/<your-username>/vibe-coding-book-prompt-programs.git
cd vibe-coding-book-prompt-programs
# open photos-per-5-years/index.html or lit-cube/index.html in your browser
```

The photo chart loads Chart.js from a CDN, so it needs an internet connection. The cube runs fully offline but needs a WebGL-capable browser.

## Repository layout

```
vibe-coding-book-prompt-programs/
├── README.md               ← you are here
├── LICENSE
├── photos-per-5-years/
│   ├── README.md           ← prompt + notes
│   └── index.html
└── lit-cube/
    ├── README.md           ← prompt + notes
    └── index.html
```

## License

[MIT](LICENSE)
