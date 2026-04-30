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

Assume target skill folder name is `seeda-chatgpt-images-2-launcher`.

### Quick Start (Exact Upstream Flow)

Create a folder named `seeda-chatgpt-images-2-launcher` in both locations:

- `~/.claude/skills/`
- `~/.codex/skills/`

Then copy these items from this repo root into that folder:

- `SKILL.md`
- `agents/`
- `references/`

Then restart Claude Code and Codex.

### Windows (PowerShell)

```powershell
$SkillName = "seeda-chatgpt-images-2-launcher"
$RepoPath = "C:\path\to\gpt-image-2-skill"

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

### macOS/Linux

```bash
SKILL_NAME="seeda-chatgpt-images-2-launcher"
REPO_PATH="/path/to/gpt-image-2-skill"

mkdir -p ~/.claude/skills ~/.codex/skills
mkdir -p ~/.claude/skills/$SKILL_NAME ~/.codex/skills/$SKILL_NAME

cp "$REPO_PATH/SKILL.md" ~/.claude/skills/$SKILL_NAME/SKILL.md
cp -R "$REPO_PATH/agents" ~/.claude/skills/$SKILL_NAME/agents
cp -R "$REPO_PATH/references" ~/.claude/skills/$SKILL_NAME/references

cp "$REPO_PATH/SKILL.md" ~/.codex/skills/$SKILL_NAME/SKILL.md
cp -R "$REPO_PATH/agents" ~/.codex/skills/$SKILL_NAME/agents
cp -R "$REPO_PATH/references" ~/.codex/skills/$SKILL_NAME/references
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
