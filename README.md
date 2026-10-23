# ShipLog

Turn your Claude Code transcript and a short spoken note into a weekly check-in, a build-in-public post, a submission write-up and a 2-minute demo script.

**Live:** https://pradeeptrain9.github.io/shiplog/

## Use it
1. Open the page and click **Load sample** to see the output.
2. For your own work, choose a Claude Code `.jsonl` file (`ls -t ~/.claude/projects/*/*.jsonl | head`) or paste plain text, one instruction per line.
3. Add a note by typing, with the mic button, or with Wispr Flow.
4. **Generate**, then copy each section or download all as Markdown.

## Optional AI polish (off by default)
Open "Polish with AI", tick the box, pick a free-tier provider (Groq, OpenRouter free models, or Google Gemini), paste your own API key and Generate. The four template outputs are rewritten by the model; if the call fails you get the template version plus the error. The key lives only in the tab's memory. Only the masked drafts (stats, your note, up to 5 quoted prompts) are sent, never the raw transcript. Model ids are editable because free models get retired.

## Privacy
Single static file. Transcripts are parsed in your browser and never uploaded. API keys, tokens, emails and your home folder name are masked in the output; read it before posting. The mic button uses your browser's speech service, which may send audio to its provider. Your note and project name are saved in your browser's local storage only.

## Develop
No build step. `python3 -m http.server`, then open `/?test`; the tab title reads `ShipLog tests passed` when the self-checks pass.

## Limits
Output is template-based unless you enable the AI polish. Word count is a proxy (your prompts to Claude), not the Wispr Insights figure. Masking uses regexes and will miss unusual secret formats.
