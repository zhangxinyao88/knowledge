# Instructions for AI Agents

This repository is a Markdown-first personal knowledge base. Markdown is the source of truth; Obsidian is an optional frontend. Keep every note understandable in GitHub and ordinary Markdown editors.

## Core behavior

- Search existing notes before creating a new canonical topic.
- Prefer adding useful connections to existing notes over creating duplicates.
- Consolidate duplicate or overlapping technical concepts when there is a clear canonical destination.
- Do not aggressively reorganize files or expand the hierarchy without a clear, practical benefit.
- Keep Markdown simple and portable. Avoid Dataview dependencies, elaborate tags, generated IDs, databases, and unnecessary Obsidian-specific syntax or plugins.
- Use normal Markdown for headings, lists, code, and external links. Wiki links such as `[[Spark AQE]]` are acceptable for lightweight internal connections.

## Protect user-authored thinking

- Treat `My Thoughts`, `My Takeaways`, `Things I Disagree With`, `Things I Learned`, and similarly personal sections as user-authored content.
- Never silently rewrite, replace, or reinterpret those sections.
- AI may suggest edits or connections, but must keep suggestions separate until the user accepts them.
- Put AI-generated summaries under an explicitly labeled `AI Summary` heading. Do not present AI synthesis as the user's view.
- Preserve the original meaning and voice when the user explicitly asks for editing of personal sections.

## Accuracy and provenance

- Do not invent facts, quotations, book content, podcast content, sources, or user opinions.
- Clearly mark uncertainty, incomplete information, and unverified claims.
- When consolidating raw notes, preserve useful provenance such as capture date, source URL, book chapter, podcast episode, or originating filename.
- Do not delete raw notes unless the user explicitly instructs you to do so.
- If source material conflicts, retain the disagreement or ask the user instead of quietly choosing a version.

## Capture and consolidation

- Allow `inbox/` and `daily/` notes to remain rough. Do not require categorization during capture.
- During consolidation, first locate related notes, then merge non-duplicative information into the best existing note when appropriate.
- Keep personal reflection separate from summaries and reference material.
- Add a small number of meaningful related-note links rather than broad, speculative link lists.

Before making broad changes, inspect the repository and explain why the change materially improves usability. Keep changes focused, reviewable, and Git-friendly.
