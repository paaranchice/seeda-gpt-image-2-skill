# GPT Image 2 Skill - Instant Launch for Prompt-to-Image Workflows

[![Use Case](https://img.shields.io/badge/Use%20Case-Prompt--to--Image-blue?style=for-the-badge)](#why-this-gpt-image-2-skill)
[![Flow](https://img.shields.io/badge/Flow-Still%20to%20Video-0f766e?style=for-the-badge)](#what-users-can-do-after-launch)
[![Clients](https://img.shields.io/badge/Clients-Claude%20Code%20%2B%20Codex-111827?style=for-the-badge)](#install)

This repository ships a focused **gpt image 2 skill** that turns intent into action: users trigger one phrase, land in a ready creator workspace, and start generating immediately.

Instead of asking users to navigate menus and docs first, this skill removes friction at the exact moment they are ready to create.

---

## Why This GPT Image 2 Skill

- **One-trigger launch**  
  Move from chat to live workspace without extra steps.
- **Creator-first flow**  
  Start with still image generation, validate composition, then move to motion.
- **Campaign-ready behavior**  
  Works well for landing pages, demos, and SEO funnels where speed-to-first-result matters.

## What Users Can Do After Launch

Based on the current page flow, users can:

- Create images from text prompts
- Edit with reference images
- Choose aspect ratio and output size (including high-resolution final output)
- Validate a still frame before spending credits on video generation
- Continue into image-to-video as a second step

## How It Works

1. **Trigger the skill**: user asks to launch GPT Image 2 generation.
2. **Open workspace**: skill opens the creator workspace in the default browser.
3. **Draft first**: user tests prompt and composition on still image output.
4. **Scale to production**: user refines and proceeds to video handoff when ready.

## High-Intent Trigger Phrases

- "Launch my GPT Image 2 workspace"
- "Start prompt-to-image now"
- "Open still-to-video starter"
- "Take me to GPT Image 2 generator"

## Install

Create a local skill folder named `seeda-chatgpt-images-2-launcher` and copy these root items from this repo into it:

- `SKILL.md`
- `agents/`
- `references/`

### Windows (PowerShell)

```powershell
# 1) Set your local repo path
$RepoPath = "C:\path\to\gpt-image-2-skill"
$SkillName = "seeda-chatgpt-images-2-launcher"

# 2) Create destination folders if missing
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude\skills" | Out-Null
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.codex\skills" | Out-Null

# 3) Create target skill directories
$CcTarget = Join-Path $env:USERPROFILE ".claude\skills\$SkillName"
$CodexTarget = Join-Path $env:USERPROFILE ".codex\skills\$SkillName"
New-Item -ItemType Directory -Force -Path $CcTarget | Out-Null
New-Item -ItemType Directory -Force -Path $CodexTarget | Out-Null

# 4) Copy root skill files into both targets
Copy-Item -Force (Join-Path $RepoPath "SKILL.md") (Join-Path $CcTarget "SKILL.md")
Copy-Item -Recurse -Force (Join-Path $RepoPath "agents") (Join-Path $CcTarget "agents")
Copy-Item -Recurse -Force (Join-Path $RepoPath "references") (Join-Path $CcTarget "references")

Copy-Item -Force (Join-Path $RepoPath "SKILL.md") (Join-Path $CodexTarget "SKILL.md")
Copy-Item -Recurse -Force (Join-Path $RepoPath "agents") (Join-Path $CodexTarget "agents")
Copy-Item -Recurse -Force (Join-Path $RepoPath "references") (Join-Path $CodexTarget "references")

# 5) Verify files exist
Get-ChildItem "$env:USERPROFILE\.claude\skills\seeda-chatgpt-images-2-launcher"
Get-ChildItem "$env:USERPROFILE\.codex\skills\seeda-chatgpt-images-2-launcher"
```

### macOS/Linux

```bash
# 1) Set your local repo path
REPO_PATH="/path/to/gpt-image-2-skill"
SKILL_NAME="seeda-chatgpt-images-2-launcher"

# 2) Create destination folders if missing
mkdir -p ~/.claude/skills ~/.codex/skills

# 3) Create target skill directories
mkdir -p ~/.claude/skills/$SKILL_NAME ~/.codex/skills/$SKILL_NAME

# 4) Copy root skill files into both targets
cp "$REPO_PATH/SKILL.md" ~/.claude/skills/$SKILL_NAME/SKILL.md
cp -R "$REPO_PATH/agents" ~/.claude/skills/$SKILL_NAME/agents
cp -R "$REPO_PATH/references" ~/.claude/skills/$SKILL_NAME/references

cp "$REPO_PATH/SKILL.md" ~/.codex/skills/$SKILL_NAME/SKILL.md
cp -R "$REPO_PATH/agents" ~/.codex/skills/$SKILL_NAME/agents
cp -R "$REPO_PATH/references" ~/.codex/skills/$SKILL_NAME/references

# 5) Verify files exist
ls -la ~/.claude/skills/seeda-chatgpt-images-2-launcher
ls -la ~/.codex/skills/seeda-chatgpt-images-2-launcher
```

### Restart (Required)

1. Completely close Claude Code.
2. Completely close Codex.
3. Reopen both clients.
4. Trigger with: `Launch my GPT Image 2 workspace`.

Detailed guide: `INSTALL.md`

## CTA

If your goal is higher click-to-create conversion, install the skill and make generation one trigger away.
