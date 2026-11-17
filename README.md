# Claude Code sessions

42 Claude Code session transcripts (`<project>/<session-id>.jsonl`, one JSON record per line), shared for reference.

Scrubbed before upload: API keys, tokens, passwords, database URLs, email addresses, phone numbers → `[redacted]`;
screenshots → `[image removed]`. Scrubbing is pattern-based — if you spot anything sensitive, please open an issue.

Read one: `jq -r 'select(.type=="user" or .type=="assistant") | .message.content | if type=="string" then . else (.[]? | .text? // empty) end' <file>.jsonl`
