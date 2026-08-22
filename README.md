# Personal Knowledge Base

This repository is a lightweight, Markdown-first home for technical notes, reading and listening notes, and personal thinking. Markdown files are the source of truth. Obsidian is an optional frontend, Git/GitHub provide history and remote storage, and AI tools can help organize or synthesize material without owning the content.

## Structure

```text
inbox/          Quick captures that need no immediate organization
daily/          Date-based notes and working logs
tech/           Consolidated technical notes by broad area
  ai/
  spark/
  airflow/
  other/
books/          Book summaries and personal responses
podcasts/       Episode summaries and personal responses
thoughts/       Longer-lived personal ideas and observations
templates/      Copyable note templates
```

The hierarchy is deliberately shallow. Add a subfolder only when a category has enough notes to make browsing difficult.

## Workflow: capture, then consolidate

1. Capture quickly in `inbox/` or `daily/`. Rough wording, incomplete ideas, and bare links are welcome.
2. Periodically search for related notes and merge useful material into an existing topic note, or create a canonical note in `tech/`, `books/`, `podcasts/`, or `thoughts/`.
3. Preserve the source or capture date when moving information. Do not delete the raw note unless it is no longer useful and deletion is intentional.

AI-written summaries belong under `AI Summary`. Personal sections such as `My Thoughts`, `My Takeaways`, and `Things I Disagree With` remain user-authored; AI may suggest changes but should not silently rewrite them.

Use ordinary Markdown links for external sources and lightweight wiki links such as `[[Spark AQE]]` for connections between notes. The files remain readable without Obsidian.

## Open in Obsidian

1. Install and open Obsidian.
2. Choose **Open folder as vault**.
3. Select this repository folder (`knowledge`).

No community plugins are required. The tracked vault setting only asks Obsidian to update links when a note is renamed or moved. Local workspace layout, caches, themes, and plugins are ignored by Git.

## Work with VS Code or Codex

Open the repository folder, edit any `.md` file, and use normal text search across the vault. When asking an AI agent to consolidate notes, identify the source notes and destination topic, and ask it to preserve provenance and user-authored sections. Repository-wide AI guidance lives in `AGENTS.md`.

## Add notes

Start from a template, then rename the copy:

```sh
cp "templates/technical-topic.md" "tech/spark/New Spark Topic.md"
cp "templates/book.md" "books/Book Title.md"
cp "templates/podcast.md" "podcasts/Podcast - Episode Title.md"
```

The current Spark notes are organized around:

- `tech/spark/Spark Architecture.md` — entry point and topic map
- `tech/spark/Spark AQE.md`
- `tech/spark/Spark SQL Query Lifecycle.md`
- `tech/spark/Spark Distributed Execution.md`
- `tech/spark/Spark Execution Terms.md`
- `tech/spark/Spark RDD.md`
- `tech/spark/Spark Repository Map.md`

## Basic Git workflow

```sh
git status
git add .
git commit -m "Add notes"
git push
```

To use GitHub, create an empty private or public repository, add it as `origin`, and push `main`. Do not store credentials, private tokens, or secrets in notes.
