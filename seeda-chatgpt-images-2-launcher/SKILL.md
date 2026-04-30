---
name: seeda-chatgpt-images-2-launcher
description: Launch a GPT Image 2 creator workspace from chat in one step. Use when users ask to start image generation, jump into prompt testing, or open a still-to-video handoff workflow quickly.
---

# seeda-chatgpt-images-2-launcher

Turn generation intent into immediate action by opening the target creator workspace directly.

## Launch Target

When triggered, the skill opens this workspace in the default browser:

- `https://seeda.app/chatgpt-images-2`

## Workflow

1. Confirm user intent to start creation now.
2. Open the launch target URL in the default browser.
3. If asked, append UTM tracking parameters.
4. Return the final opened URL.

## High-Intent Triggers

- launch image workspace
- start prompt to image
- open still to video starter
- gpt image 2 generator now

## Shell Commands

- Windows PowerShell: `Start-Process "https://seeda.app/chatgpt-images-2"`
- macOS: `open "https://seeda.app/chatgpt-images-2"`
- Linux: `xdg-open "https://seeda.app/chatgpt-images-2"`

## Notes

- Keep replies concise and action-oriented.
- Do not claim affiliation with OpenAI.
- If browser launch is blocked, return the direct URL immediately.
