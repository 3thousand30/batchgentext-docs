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

1. In Step 2, click **Select samples file** or **Select samples folder**
2. The preview panel will confirm what was loaded

**Supported formats:**

| Method | Supported formats |
|---|---|
| Single file | `.txt`, `.md`, `.pdf`, `.docx`, `.yaml` |
| Folder | `.txt`, `.md`, `.pdf`, `.docx` (up to 5 files) |

For `.txt`, `.md`, `.pdf`, and `.docx` files, the entire document becomes one writing sample. For a YAML file, you can include multiple named samples:

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

### Download example files

Ready-to-use example files are available for every template. Download one, open it via **Select content list**, choose the matching template, and hit Generate.

| Template | Example file |
|---|---|
| Blog Article | [example-list.csv](example-list.csv) · [example-list.yaml](example-list.yaml) |
| LinkedIn Post | [example-linkedin.csv](example-linkedin.csv) |
| X (Twitter) Post | [example-x-posts.csv](example-x-posts.csv) |
| Facebook Post | [example-facebook.csv](example-facebook.csv) |
| Short Story | [example-stories.csv](example-stories.csv) |
| Technical Document | [example-technical.csv](example-technical.csv) |

> Each run uses one template for the entire list. Keep separate files per content type.

### Field reference

| Field | Aliases accepted | Required |
|---|---|---|
| `title` | `topic`, `subject` | Yes |
| `theme` | `category` | No |
| `keywords` | `tags`, `keyword` | No |
| `notes` | `note`, `guidance`, `context` | No |

### CSV format

```csv
title,theme,keywords,notes
"How to Price Your First Rental Property","RealEstate","property,investment,rental yield","Walk a first-time landlord through yield calculation and common pricing mistakes."
"5 Mistakes New Dog Owners Make in the First Month","Pets","dog training,puppy,habits","Warm reassuring tone. Practical fixes. Focus on first critical weeks."
```

### YAML format

```yaml
- title: "How to Price Your First Rental Property"
  theme: RealEstate
  keywords: "property, investment, rental yield"
  notes: |
    Walk a first-time landlord through the key numbers.
    Cover yield calculation, vacancy rate, and common pricing mistakes.

- title: "5 Mistakes New Dog Owners Make in the First Month"
  theme: Pets
  keywords: "dog training, puppy, habits"
  notes: |
    Warm and reassuring tone — not shaming.
    Practical fixes for each mistake.
```

All fields except `title` are optional — a one-column CSV with just titles works fine for a quick test run.

---

## 6. Run your first generation

1. In Step 3, click **Select content list** and choose your file
2. Choose a **template** (Blog Article is a good start)
3. Select your **output folder** (defaults to `Documents\BatchGenText`)
4. _(Optional)_ Change the **output format** — Auto uses the template's default (.md or .txt), or override to Markdown (.md) or Plain text (.txt)
5. Click **Preview first item** to generate just the first article and review it in-app before committing to the full batch
6. Click **Generate** (or **Generate Full Batch** from the preview dialog) to generate everything

The app processes each item one by one. A live log shows progress and token usage per article. When complete, a summary banner shows the full token count and a button to open the output folder.

Output files are saved in a timestamped subfolder (e.g. `2026-03-01_14-30-00`) so each run is kept separate. Preview and full batch share the same folder — the first article is not regenerated.

---

## Next steps

- Experiment with different templates and see which output format suits your workflow
- Add a quotes YAML file in Step 2 to weave curated quotes into your content
- Try the X/Twitter template with thread mode for social media batches
- Adjust the output language in Step 3 for non-English content
