# threejs-parallax-skill

A [Claude Code](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview) / [Cursor](https://cursor.com) / [Codex](https://openai.com/index/introducing-codex/) skill that creates **2.5D parallax effects** using Three.js with layered transparent PNG assets on `PlaneGeometry`.

## What it does

This skill teaches the AI agent how to build interactive parallax scenes where stacked transparent PNGs are rendered on separate Three.js planes with:

- **Mouse-driven parallax** — layers shift based on cursor position, with background layers moving least and foreground layers moving most
- **Scroll-driven layer motion** — layers drift independently (left/right/up/down) as the section scrolls through the viewport
- **Smooth interpolation** — all motion is lerped for a polished, fluid feel
- **Correct color rendering** — includes critical `SRGBColorSpace` settings to prevent washed-out textures

## Installation

### Claude Code

Copy the `threejs-parallax` folder into your project's `.claude/skills/` directory:

```bash
git clone https://github.com/JudyZZ/threejs-parallax-skill.git /tmp/threejs-parallax-skill
cp -r /tmp/threejs-parallax-skill/threejs-parallax .claude/skills/
```

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

## How to use it?

Once installed, the skill activates automatically when you mention things like:

- "Add a parallax effect with these assets (attaching your assets)."
- "Create a 2.5D scene with these assets (attaching your assets)"
- "Add depth effect with layered images with these assets (attaching your assets)"
- "Use these assets (attaching your assets) make an 2.5D graphic with paralax effect."

To have a better result, please also attach a screenshot of the outcome you want in the prompt, and ask the agent to reference it. 

The agent will guide the scene setup, layer configuration, and animation loop.

Additional tip for adjusting positions of assets: Ask the agent to show the position info of assest, and then prompt for the change you want.

## License

MIT — see [LICENSE](LICENSE).
