# GPT Image 2 Skill

A Claude Code and Codex skill that opens a GPT Image 2 creator workflow in one trigger.

## Features

- One-trigger launch from chat to creator workspace
- Prompt-first image workflow with still-to-video handoff support
- Built for landing-page funnels and fast first action
- Works in both Claude Code and Codex

## Prerequisites

1. Claude Code and/or Codex installed
2. Git installed
3. Network access and a default browser

## Installation

Skill folder name:

`seeda-chatgpt-images-2-launcher`

### Option A: Quick Install with `git clone` (Recommended)

#### macOS/Linux

```bash
git clone https://github.com/paaranchice/gpt-image-2-skill ~/.claude/skills/seeda-chatgpt-images-2-launcher
git clone https://github.com/paaranchice/gpt-image-2-skill ~/.codex/skills/seeda-chatgpt-images-2-launcher
```

#### Windows (PowerShell)

```powershell
git clone https://github.com/paaranchice/gpt-image-2-skill "$env:USERPROFILE\.claude\skills\seeda-chatgpt-images-2-launcher"
git clone https://github.com/paaranchice/gpt-image-2-skill "$env:USERPROFILE\.codex\skills\seeda-chatgpt-images-2-launcher"
```

### Option B: Install Both from an Existing Local Clone

If you already cloned this repo to your machine:

#### macOS/Linux

```bash
REPO_PATH="/path/to/gpt-image-2-skill"
SKILL_NAME="seeda-chatgpt-images-2-launcher"

mkdir -p ~/.claude/skills/$SKILL_NAME ~/.codex/skills/$SKILL_NAME

cp "$REPO_PATH/SKILL.md" ~/.claude/skills/$SKILL_NAME/SKILL.md
cp -R "$REPO_PATH/agents" ~/.claude/skills/$SKILL_NAME/agents
cp -R "$REPO_PATH/references" ~/.claude/skills/$SKILL_NAME/references

cp "$REPO_PATH/SKILL.md" ~/.codex/skills/$SKILL_NAME/SKILL.md
cp -R "$REPO_PATH/agents" ~/.codex/skills/$SKILL_NAME/agents
cp -R "$REPO_PATH/references" ~/.codex/skills/$SKILL_NAME/references
```

#### Windows (PowerShell)

```powershell
$RepoPath = "C:\path\to\gpt-image-2-skill"
$SkillName = "seeda-chatgpt-images-2-launcher"

$CcTarget = Join-Path $env:USERPROFILE ".claude\skills\$SkillName"
$CodexTarget = Join-Path $env:USERPROFILE ".codex\skills\$SkillName"

New-Item -ItemType Directory -Force -Path $CcTarget | Out-Null
New-Item -ItemType Directory -Force -Path $CodexTarget | Out-Null

Copy-Item -Force (Join-Path $RepoPath "SKILL.md") (Join-Path $CcTarget "SKILL.md")
Copy-Item -Recurse -Force (Join-Path $RepoPath "agents") (Join-Path $CcTarget "agents")
Copy-Item -Recurse -Force (Join-Path $RepoPath "references") (Join-Path $CcTarget "references")

Copy-Item -Force (Join-Path $RepoPath "SKILL.md") (Join-Path $CodexTarget "SKILL.md")
Copy-Item -Recurse -Force (Join-Path $RepoPath "agents") (Join-Path $CodexTarget "agents")
Copy-Item -Recurse -Force (Join-Path $RepoPath "references") (Join-Path $CodexTarget "references")
```

### Restart Clients

1. Close Claude Code completely.
2. Close Codex completely.
3. Reopen both clients.

## Usage

After restart, ask with phrases like:

- `Launch my GPT Image 2 workspace`
- `Start prompt-to-image now`
- `Open still-to-video starter`
- `Take me to GPT Image 2 generator`

## Verify Installation

### macOS/Linux

```bash
ls -la ~/.claude/skills/seeda-chatgpt-images-2-launcher
ls -la ~/.codex/skills/seeda-chatgpt-images-2-launcher
```

### Windows (PowerShell)

```powershell
Get-ChildItem "$env:USERPROFILE\.claude\skills\seeda-chatgpt-images-2-launcher"
Get-ChildItem "$env:USERPROFILE\.codex\skills\seeda-chatgpt-images-2-launcher"
```

## Update

If installed via clone:

```bash
git -C ~/.claude/skills/seeda-chatgpt-images-2-launcher pull
git -C ~/.codex/skills/seeda-chatgpt-images-2-launcher pull
```

For full install and uninstall instructions, see `INSTALL.md`.
