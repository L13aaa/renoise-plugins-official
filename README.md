# renoise-plugins-official

AI video production skills by Renoise: creative direction, generation, analysis, e-commerce content, and download.

## Skills

| Skill | Description |
|-------|-------------|
| **director** | Creative director and single entry point for video creation: product ads, short films, TikTok e-commerce, drama, comedy |
| **gemini-gen** | Visual understanding and multimodal analysis via Gemini 3.1 Pro: product analysis, video script extraction, style extraction |
| **renoise-gen** | AI video and image generation engine: Renoise CLI, material pool, product design sheets, scene backgrounds |
| **video-download** | Video downloader: yt-dlp plus Douyin/TikTok fallback |

## Installation

### Claude Code

```bash
claude plugin marketplace add ArcoCodes/renoise-plugins-official
claude plugin install renoise@renoise-plugins-official
```

Then connect your Renoise account:

```text
/renoise:setup
```

### Codex

Requires Codex 0.117.0 or newer.

```bash
codex plugin marketplace add ArcoCodes/renoise-plugins-official
codex plugin add video-maker@renoise-plugins
```

Start a new Codex thread after installing so the skills are loaded.

To update later:

```bash
codex plugin marketplace upgrade renoise-plugins
codex plugin add video-maker@renoise-plugins
```

### OpenClaw

```bash
openclaw plugins install @renoise/plugin
```

## Environment Variables

| Variable | Required By | Description |
|----------|-------------|-------------|
| `RENOISE_API_KEY` | All generation and analysis skills | Renoise API credential. Get one at https://www.renoise.ai |

## Repository Layout

```text
.agents/plugins/marketplace.json      # Codex marketplace entry
.claude-plugin/marketplace.json       # Claude Code marketplace entry
plugins/video-maker/                  # Shared plugin implementation
plugins/video-maker/.codex-plugin/    # Codex plugin manifest
plugins/video-maker/.claude-plugin/   # Claude Code plugin manifest
openclaw.plugin.json                  # OpenClaw manifest
```
