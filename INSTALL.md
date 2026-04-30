# GPT Image 2 Skill Installation

Install this skill into Claude Code, Codex, or both.

## Skill Name

`seeda-chatgpt-images-2-launcher`

## Requirements

1. Git installed
2. Claude Code and/or Codex installed
3. A default browser configured

## Install with `git clone` (Recommended)

### macOS/Linux

```bash
mkdir -p ~/.claude/skills ~/.codex/skills

git clone https://github.com/paaranchice/gpt-image-2-skill ~/.claude/skills/seeda-chatgpt-images-2-launcher
git clone https://github.com/paaranchice/gpt-image-2-skill ~/.codex/skills/seeda-chatgpt-images-2-launcher
```

### Windows (PowerShell)

```powershell
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude\skills" | Out-Null
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.codex\skills" | Out-Null

git clone https://github.com/paaranchice/gpt-image-2-skill "$env:USERPROFILE\.claude\skills\seeda-chatgpt-images-2-launcher"
git clone https://github.com/paaranchice/gpt-image-2-skill "$env:USERPROFILE\.codex\skills\seeda-chatgpt-images-2-launcher"
```

## Install from an Existing Clone

Use this when you already have the repository on your machine.

### macOS/Linux

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

### Windows (PowerShell)

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

## Restart

1. Close Claude Code completely.
2. Close Codex completely.
3. Reopen the client you want to use.
4. Trigger with `Launch my GPT Image 2 workspace`.

## Verify

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

If installed with `git clone`:

### macOS/Linux

```bash
git -C ~/.claude/skills/seeda-chatgpt-images-2-launcher pull
git -C ~/.codex/skills/seeda-chatgpt-images-2-launcher pull
```

### Windows (PowerShell)

```powershell
git -C "$env:USERPROFILE\.claude\skills\seeda-chatgpt-images-2-launcher" pull
git -C "$env:USERPROFILE\.codex\skills\seeda-chatgpt-images-2-launcher" pull
```

Restart Claude Code and Codex after updating.

## Uninstall

### macOS/Linux

```bash
rm -rf ~/.claude/skills/seeda-chatgpt-images-2-launcher
rm -rf ~/.codex/skills/seeda-chatgpt-images-2-launcher
```

### Windows (PowerShell)

```powershell
Remove-Item -Recurse -Force "$env:USERPROFILE\.claude\skills\seeda-chatgpt-images-2-launcher"
Remove-Item -Recurse -Force "$env:USERPROFILE\.codex\skills\seeda-chatgpt-images-2-launcher"
```
