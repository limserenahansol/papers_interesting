# Setup: archive paper Q&A to GitHub

**User request:** From now on, when asking any paper and summary, always upload the file, summary, and conversation to [papers_interesting](https://github.com/limserenahansol/papers_interesting).

## What was done

- Initialized repo layout: `entries/` for Markdown logs, `files/` for optional PDFs/attachments.
- Added Cursor rule `behavior_task/.cursor/rules/papers-interesting-archive.mdc` (`alwaysApply: true`) so future sessions create an entry, save attachments when present, and **git commit + push** to `papers_interesting` on `main`.

## Conversation recap

- User asked for a standing workflow: any paper + summary request should be archived to the GitHub repo with file(s), summary, and conversation.
- Repository was empty; first commit pushed with README and folder structure; this meta-entry documents the policy.

**Files:** none attached in this thread.
