# Skill Installation Guide (Claude Code + Codex)

This guide installs the same skill into:

- Claude Code (CC)
- Codex

## 1. Prerequisites

1. Git is installed.
2. Claude Code is installed.
3. Codex is installed.
4. The skill folder contains `SKILL.md`.

## 2. Skill Paths

### Claude Code

- Windows: `C:\Users\<YourUser>\.claude\skills`
- macOS/Linux: `~/.claude/skills`

### Codex

- Windows: `C:\Users\<YourUser>\.codex\skills`
- macOS/Linux: `~/.codex/skills`

## 3. Install by Copy (Recommended)

Assume skill folder name is `seeda-chatgpt-images-2-launcher`.

### Quick Start (Exact Upstream Flow)

Copy `seeda-chatgpt-images-2-launcher` into:

- `~/.claude/skills/`
- `~/.codex/skills/`

Then restart Claude Code and Codex.

This repository already contains that folder at:

- `seeda-chatgpt-images-2-launcher/`

If you cloned this repo, use that exact folder as the source.

### Windows (PowerShell)

```powershell
$SkillName = "seeda-chatgpt-images-2-launcher"
$RepoSkillPath = "C:\path\to\repo\$SkillName"

$CcTarget = Join-Path $env:USERPROFILE ".claude\skills\$SkillName"
$CodexTarget = Join-Path $env:USERPROFILE ".codex\skills\$SkillName"

New-Item -ItemType Directory -Force -Path (Split-Path $CcTarget) | Out-Null
New-Item -ItemType Directory -Force -Path (Split-Path $CodexTarget) | Out-Null

Copy-Item -Recurse -Force $RepoSkillPath $CcTarget
Copy-Item -Recurse -Force $RepoSkillPath $CodexTarget
```

### macOS/Linux

```bash
SKILL_NAME="seeda-chatgpt-images-2-launcher"
REPO_SKILL_PATH="/path/to/repo/$SKILL_NAME"

mkdir -p ~/.claude/skills ~/.codex/skills
cp -R "$REPO_SKILL_PATH" ~/.claude/skills/
cp -R "$REPO_SKILL_PATH" ~/.codex/skills/
```

## 4. Verify

### Windows

```powershell
Get-ChildItem "$env:USERPROFILE\.claude\skills\seeda-chatgpt-images-2-launcher"
Get-ChildItem "$env:USERPROFILE\.codex\skills\seeda-chatgpt-images-2-launcher"
```

### macOS/Linux

```bash
ls -la ~/.claude/skills/seeda-chatgpt-images-2-launcher
ls -la ~/.codex/skills/seeda-chatgpt-images-2-launcher
```

Restart Claude Code and Codex after installation.

### Restart Checklist (Detailed)

1. Close all Claude Code windows and running sessions.
2. Close all Codex windows and running sessions.
3. Reopen Claude Code.
4. Reopen Codex.
5. Run a trigger phrase such as `Launch my GPT Image 2 workspace`.

## 5. Uninstall

### Windows

```powershell
Remove-Item -Recurse -Force "$env:USERPROFILE\.claude\skills\seeda-chatgpt-images-2-launcher"
Remove-Item -Recurse -Force "$env:USERPROFILE\.codex\skills\seeda-chatgpt-images-2-launcher"
```

### macOS/Linux

```bash
rm -rf ~/.claude/skills/seeda-chatgpt-images-2-launcher
rm -rf ~/.codex/skills/seeda-chatgpt-images-2-launcher
```
