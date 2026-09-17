# Canonical Assessment Format

Use exactly:

```text
FORMATION|ACTION|OBJECTIVE|START_WINDOW|EVIDENCE
```

Rules:

- Use the canonical IDs found in the data.
- Use uppercase ASCII.
- Allowed action vocabulary: `ATTACK`, `DEFEND`, `REINFORCE`, `WITHDRAW`, `FEINT`.
- Express the start window as `YYYY-MM-DDTHH:00Z/HH:00Z`.
- Include exactly five evidence IDs.
- Sort evidence IDs lexicographically.
- Separate evidence IDs with commas.
- Use no spaces and no trailing newline.

Unrelated example:

```text
9DIV|REINFORCE|WEST-SECTOR|2031-08-04T06:00Z/12:00Z|E003,E014,E021,E087,E102
```

Validation example:

```bash
candidate='9DIV|REINFORCE|WEST-SECTOR|2031-08-04T06:00Z/12:00Z|E003,E014,E021,E087,E102'
printf '%s' "$candidate" | md5sum
```
