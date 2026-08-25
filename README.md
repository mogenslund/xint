# Iron Veil: Static Intelligence Exercise

This is a small fictional, static-file intelligence game. It contains no server,
custom executable, database, or generated state. Use ordinary terminal tools such
as `find`, `grep`, `awk`, `sort`, `cut`, `jq`, `md5sum`, and an editor.

All countries, units, people, places, and events are fictional.

## Start

```bash
cat briefings/mission-001.md
cat reference/assessment-format.md
find intel -type f | sort
```

Investigate the files and write an assessment. The mission requires one canonical
assessment string containing a conclusion and exactly five evidence IDs.

Validate a candidate with:

```bash
candidate='...'
hash=$(printf '%s' "$candidate" | md5sum | cut -d' ' -f1)
find validation -type f -name "$hash.success" -print
```

A printed path means the assessment is accepted. No output means it is not.

Do not inspect `author/` until you want the solution. For an actual release, keep
`author/` out of the player package.
