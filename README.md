# ShipLog

Turn your Claude Code transcript and a short spoken note into a weekly check-in, a build-in-public post, a submission write-up and a 2-minute demo script.

**Live:** https://pradeeptrain9.github.io/shiplog/

## Use it
1. Open the page and click **Load sample** to see the output.
2. For your own work, choose a Claude Code `.jsonl` file (`ls -t ~/.claude/projects/*/*.jsonl | head`) or paste plain text, one instruction per line.
3. Add a note by typing, with the mic button, or with Wispr Flow.
4. **Generate**, then copy each section or download all as Markdown.

## Privacy
Single static file. Transcripts are parsed in your browser and never uploaded. API keys, tokens, emails and your home folder name are masked in the output; read it before posting. The mic button uses your browser's speech service, which may send audio to its provider. Your note and project name are saved in your browser's local storage only.

## Develop
No build step. `python3 -m http.server`, then open `/?test`; the tab title reads `ShipLog tests passed` when the self-checks pass.

## Limits
Output is template-based, not written by an LLM. Word count is a proxy (your prompts to Claude), not the Wispr Insights figure. Masking uses regexes and will miss unusual secret formats.
