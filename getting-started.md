---
layout: default
title: Getting Started
nav_order: 2
---

# Getting Started

This guide walks you through setting up BatchGen Text with AI and generating your first batch of content.

---

## 1. Install the app

Download and install **BatchGen Text with AI** from the Microsoft Store. Once installed, launch it from the Start menu.

---

## 2. Set up your AI provider

Before generating anything, you need an API key from an AI provider.

1. Click the **settings icon** (top right of the app)
2. Select your provider from the dropdown — if you're not sure which one to pick, see [Choosing an AI Provider](choosing-a-provider)
3. Click **Get API key** to open the provider's signup page
4. Paste your API key into the field and click **Save**
5. Click **Test connection** to confirm everything is working

Your API key is encrypted and stored on your device only. It is sent directly to your chosen provider — nowhere else.

---

## 3. Configure your persona (Step 1)

The persona defines the voice and tone the AI will write in. Think of it as your AI writing assistant's character.

The app includes three starter personas to choose from:

- **Chatty Betty** — warm, conversational, relatable
- **Serious Darius** — authoritative, precise, professional
- **Creative Sam** — imaginative, playful, unconventional

Select a persona by clicking its card. The detail panel on the right shows the full persona definition — identity, core beliefs, writing style, and quality bar.

You can customise any persona or add your own (up to 5 total) directly in the app later.

---

## 4. Load writing samples (Step 2, optional)

Writing samples let the app reverse-engineer your writing style and produce content that sounds like _you_, not like a generic AI.

To use samples:

1. Prepare a YAML file with your existing articles (see format below)
2. In Step 2, click **Select samples file** or point the app to a folder containing sample files
3. The preview panel will confirm what was loaded

**Sample file format:**

```yaml
- title: "My First Article"
  content: |
    The full text of your article goes here.
    Multiple paragraphs are fine.

- title: "Another Article"
  content: |
    Another piece of your writing.
```

Up to 3 samples are used per generation run. More is fine — the app picks from them automatically.

---

## 5. Prepare your content list (Step 3)

The content list is a CSV or YAML file listing everything you want to generate. At minimum, each item needs a title.

**CSV format:**

```csv
title,theme,keywords,notes
"Why Sleep Matters","Health","sleep, recovery, habits","Focus on science-backed tips"
"Morning Routines That Stick","Productivity","habits, morning","Keep it practical"
```

**YAML format:**

```yaml
- title: "Why Sleep Matters"
  theme: "Health"
  keywords: "sleep, recovery, habits"
  notes: "Focus on science-backed tips"

- title: "Morning Routines That Stick"
  theme: "Productivity"
  keywords: "habits, morning"
  notes: "Keep it practical"
```

All fields except `title` are optional. The app also accepts common aliases — `topic` or `subject` instead of `title`, `tags` instead of `keywords`, `guidance` instead of `notes`.

---

## 6. Run your first generation

1. In Step 3, click **Select content list** and choose your file
2. Choose a **template** (Blog Article is a good start)
3. Select your **output folder** (defaults to `Documents\BatchGenText`)
4. Click **Generate**

The app processes each item one by one. A live log shows progress and token usage per article. When complete, a summary banner shows the full token count and a button to open the output folder.

Output files are saved in a timestamped subfolder (e.g. `2025-06-01_14-30-00`) so each run is kept separate.

---

## Next steps

- Experiment with different templates and see which output format suits your workflow
- Add a quotes YAML file in Step 2 to weave curated quotes into your content
- Try the X/Twitter template with thread mode for social media batches
- Adjust the output language in Step 3 for non-English content
