# threejs-parallax-skill

A [Cursor](https://cursor.com) / [Codex](https://openai.com/index/introducing-codex/) skill that creates **2.5D parallax effects** using Three.js with layered transparent PNG assets on `PlaneGeometry`.

## What it does

This skill teaches the AI agent how to build interactive parallax scenes where stacked transparent PNGs are rendered on separate Three.js planes with:

- **Mouse-driven parallax** — layers shift based on cursor position, with background layers moving least and foreground layers moving most
- **Scroll-driven layer motion** — layers drift independently (left/right/up/down) as the section scrolls through the viewport
- **Smooth interpolation** — all motion is lerped for a polished, fluid feel
- **Correct color rendering** — includes critical `SRGBColorSpace` settings to prevent washed-out textures

## Installation

### Cursor

Copy the `threejs-parallax` folder into your project's `.cursor/skills/` directory:

```bash
git clone https://github.com/JudyZZ/threejs-parallax-skill.git /tmp/threejs-parallax-skill
cp -r /tmp/threejs-parallax-skill/threejs-parallax .cursor/skills/
```

### Codex

Use the Codex skill installer:

```bash
codex install-skill --repo JudyZZ/threejs-parallax-skill --path threejs-parallax
```

Or manually copy into `~/.codex/skills/`:

```bash
git clone https://github.com/JudyZZ/threejs-parallax-skill.git /tmp/threejs-parallax-skill
cp -r /tmp/threejs-parallax-skill/threejs-parallax ~/.codex/skills/
```

## Usage

Once installed, the skill activates automatically when you mention things like:

- "Add a parallax effect"
- "Create a 2.5D scene"
- "Add depth effect with layered images"
- "Make an interactive media placeholder with parallax"

The agent will guide the scene setup, layer configuration, and animation loop.

## License

MIT — see [LICENSE](LICENSE).
