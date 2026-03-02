---
layout: default
title: Troubleshooting
nav_order: 5
---

# Troubleshooting

Common issues and how to fix them.

---

## API errors during generation

### 401 Unauthorized

Your API key is invalid or has been revoked.

- Double-check you copied the full key (no leading/trailing spaces)
- Log in to your provider's dashboard and verify the key is active
- Generate a new key if needed and update it in the app settings

### 403 Forbidden

Your account doesn't have permission to use the selected model.

- Some providers require billing to be set up before accessing certain models
- Try switching to a different model in the settings dialog
- Check your provider dashboard for account restrictions

### 429 Too Many Requests

You've hit your provider's rate limit.

- Free tier accounts have strict request-per-minute limits — consider upgrading
- Reduce your batch size and run in smaller chunks
- Wait a few minutes and try again
- Switch to a provider with higher rate limits (Groq is fast and generous on free tier)

### 500 / 503 Server Error

The provider's servers are having issues — this is on their end, not yours.

- Wait a few minutes and retry
- Check your provider's status page for ongoing incidents
- Switch to a different provider temporarily

---

## Connection test fails

**"Test connection" shows an error but my key looks correct:**

1. Make sure the Base URL matches your provider exactly — see [Finding Your Base URL](base-url)
2. Check that you selected the right provider preset (each has a different base URL)
3. Try copying the API key again directly from your provider dashboard
4. Check if your provider requires a specific model name — update the model field in settings

---

## Content list issues

**CSV file not loading:**

- Make sure the first row is a header row with column names (`title`, `keywords`, etc.)
- If your fields contain commas, wrap them in double quotes: `"Sleep, rest, and recovery"`
- Try saving the file as UTF-8 encoding if you're using non-English characters

**YAML file not loading:**

- YAML is indent-sensitive — use 2 spaces, not tabs
- Each item must start with `- ` (dash + space)
- Validate your YAML at [yamllint.com](https://www.yamllint.com) if you're unsure

**Articles generating with wrong titles:**

- The app accepts `title`, `topic`, or `subject` as column names — make sure one of them is present
- Check for hidden characters or BOM markers if copying from Excel

---

## Generation stops mid-batch

If one article fails (e.g. API timeout), the app logs the error and continues with the next item. Check the generation log — failed items show in red with the error reason.

To retry only the failed items, create a new content list with just those titles and run again.

---

## Output files are empty or missing

- Check that the output folder path exists and the app has write permission to it
- If using a network drive or OneDrive-synced folder, try switching to a local path (e.g. `Documents\BatchGenText`)
- Single X/Twitter posts are all collected into one `tweets.txt` file — look for that instead of individual files

---

## App won't start or crashes on launch

- Try running the app as Administrator (right-click → Run as administrator) once — this can help with initial DPAPI setup
- Check that your Windows is up to date (the app requires Windows 10 or later)
- Reinstall the app from the Microsoft Store if the issue persists

---

## Still stuck?

[Open an issue](https://github.com/3thousand30/batchgentext-docs/issues) and include:
- The error message you're seeing
- Which AI provider you're using
- Your content list format (CSV or YAML)
- What template you selected
