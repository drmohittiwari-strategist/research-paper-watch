# Editable shortlist and automation

## Sheet structure

Load the relevant spreadsheet authoring/editing instructions. For an existing sheet, resolve the exact supplied ID, read metadata and use bounded reads with actual tab names. Do not substitute a title match for an inaccessible exact target. Preserve the existing schema and native structures unless a change is requested.

For new destinations, use Today, Archive, Instructions and Search Log; add a ranking reference tab only when needed. Keep Today as a stable tab name even for weekly updates. Use these default columns unless the user supplies a schema:

| Column | Field |
| --- | --- |
| A | Discovery date |
| B | Paper title |
| C | Authors |
| D | Journal |
| E | Verified journal rating, or not configured |
| F | Publication date, labelled first-online or issue |
| G | Research theme |
| H | Why relevant, including verified important-author signal |
| I | Method / data, abstract-based |
| J | Key finding and limitation, abstract-based |
| K | Verified DOI link |
| L | Publisher link |
| M | Access status, informational only |
| N | Your notes |
| O | Your rating (1–5) |

Leave N/O blank for new papers. Preserve/extend the rating dropdown with valid values 1,2,3,4,5. If the user changes the rating scale, use the configured values rather than hardcoded defaults. Do not create dummy scholarly records to demonstrate ratings. Keep long prose wrapped and links readable; preserve existing formatting on edits. Read back new rows and validation before reporting success.

Keep persistent normalized DOI delivery history even when the user deletes Today rows. Record run date, search window, sources/coverage, delivery status and successful searched-through boundary. Store author preferences and search configuration privately in Instructions. Do not import personal settings from another user's example.

## Archive safely

Use the configured user-rating threshold (default 4 or 5), not the journal rating or machine assessment. Leave lower-rated and unrated rows in Today. Group/archive by discovery date and record archive date separately if the schema permits. Do not overwrite existing archived data or user edits.

Re-read eligible source rows immediately before mutation. Append only archive-missing DOI records, read them back, then remove only source rows whose identity, notes and rating still match the verified snapshot. Delete row indexes in descending order. After partial failure, retry via DOI comparisons and retain source rows when uncertain. Never clear Today as a whole.

## Schedule independently

Check the actual available automation tool and existing tasks. Reuse matching tasks when changing cadence; never duplicate a schedule merely because preferences changed. Use the user's IANA timezone. Resolve weekly weekday and local time from the user's instruction or an explicit stated assumption.

Embed the effective scope, ranking reference, exact private sheet target, abstract rules, paywall neutrality, important-author preferences, delivery deduplication and checkpoint behavior in task instructions. Ensure recurring execution can load the relevant tools and user configuration. Use a separate archive task if the user requests timed archiving. Changing search cadence alone must not change archiving or unrelated monitoring tasks.

A refresh request runs immediately using current settings. Do not replace it with an automation update. A skill installation creates no schedules by itself. After a successful baseline, preserve that completion marker; daily/weekly runs continue from the last successful boundary with a stated seven-calendar-day overlap for indexing delays unless configured otherwise. Deduplicate the overlap against persistent delivery history. Never advance the boundary after failed or unverified writes. Report a blocked connection or missing capability and complete independent available work without fabricating execution.
