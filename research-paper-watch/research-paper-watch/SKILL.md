---
name: research-paper-watch
description: Discover and assess recent journal research from verified abstracts, including paywalled papers, using configurable topics, journal rankings and important authors. Use when users request a research-paper watch, editable literature shortlist, initial retrospective search, recurring paper updates, rating-based archiving, or changes to those search preferences.
---

# Research Paper Watch

## Establish the request

Distinguish setup, immediate search, refresh, preference change, scheduling and archiving. Carry out only the requested operations. Treat a request to build or install this skill as distinct from authorization to run searches, alter existing sheets or create schedules.

Read [configuration.md](references/configuration.md) before setup or changing preferences. Read [screening.md](references/screening.md) before discovery and assessment. Read [sheet-and-schedule.md](references/sheet-and-schedule.md) before sheet writes, scheduling or archiving.

Discover available scholarly search, spreadsheet and automation capabilities. Load their applicable instructions. Prefer connected service tools; use authorized alternatives if a capability is unavailable. Explain material limitations. Never claim a skill alone provides database subscriptions, a scheduler or spreadsheet connectivity.

## Use optional sources without connection prompts

Treat Sider Scholar, Scopus and all other scholarly services as optional search sources, not installation prerequisites. Use an already connected, authorized scholarly source when suitable. If none is usable, continue with available web search, publisher abstracts and authoritative DOI records. Do not display a Sider Scholar integration requirement, installation card, connection prompt or unsolicited recommendation to add a scholarly plugin. Do not initiate an optional service connection flow merely to improve coverage.

If a source reports missing authentication or requests a connection, stop using that source and switch to an available alternative; do not expose the optional connection prompt as a required user action. Do not bypass any access controls. Ask about connecting a particular scholarly service only when the user explicitly requests that service and its required access cannot be fulfilled with existing tools. When no available source can support verification, explain the actual research limitation and request relevant abstracts or records instead of insisting on an integration.

Keep spreadsheet and scheduling capability requirements separate from optional discovery sources. Report sources actually used and any material coverage limitations. Never hide an execution failure or imply that Scopus or Sider Scholar was searched when it was not.

## Collect preferences once

Reuse preferences explicitly supplied in the current conversation or the user's verified private configuration. Ask only missing questions, at most three closely related questions per turn. Allow “no preference.” Ask for the following:

1. What research topics, questions and alternative keywords should the search cover? Which concepts must occur together, and what should be excluded?
2. Which industries, countries, firm types and outcomes matter? Which contexts are strict requirements versus preferences?
3. Which journals or ranking systems qualify? Can the user provide the exact list and edition? What ratings and article types are acceptable?
4. Who are the important authors or researchers in the field? Request names and optional ORCID, Scopus Author ID or profile links. Ask whether to prioritize their papers, papers citing their work, or both.
5. How far back should the first search go? Should updates be manual, daily or weekly? Ask the weekday, local time and timezone when scheduling.
6. Where should the editable shortlist live? Ask for an existing exact destination or permission to create a new one. What rating scale and archive threshold should be used, and when should archiving run?

Use the full question wording and configuration fields in the reference. Summarize the effective settings before first execution; make reasonable defaults explicit. Ask a clarification only when an unresolved constraint prevents correct execution. Never force a separate approval for already authorized searches or reversible edits.

Keep each user's settings private. Never embed personal emails, destination IDs, credentials, schedules or an author's private watchlist into the shared skill. Do not publish private configuration to GitHub. Use environment/tool-managed credentials, never request passwords or keys in chat.

## Search and assess

1. Compute an explicit inclusive initial date window in the user's timezone. Default to the last 30 calendar days including today only when the user has not specified otherwise. For subsequent updates, use the saved successful-search boundary with overlap for delayed indexing.
2. Construct separate queries per topic, expanding meaningful synonyms. Apply AND only to required concept groups and OR within alternatives. Search title, abstract and author keywords when supported. Do not require every theme to match one paper.
3. Prefer Scopus for discovery and abstracts when authorized access is available. Otherwise use available scholarly indexes and publisher abstracts. Report actual sources used; a web query restricted to scopus.com is not a full Scopus database search.
4. Include open-access and subscription papers equally. Never filter or rank by free download availability. Never require full text to shortlist an abstract-verified paper.
5. Verify the DOI and matching title, authors, journal and dates using publisher/authoritative DOI records. Separate first-online, issue, discovery and acceptance dates. Do not infer publication from acceptance or search-engine recency.
6. Match journals to the exact configured ranking edition using ISSN and normalized title. Do not treat Scopus indexing as an ABDC rating. Hold uncertain matches out of a strict shortlist; report unresolved candidates separately.
7. Read the available abstract and write a concise original assessment of topic fit, contribution, described method/data, stated findings, practical research usefulness and limitations. Label it “Abstract-based assessment.” Never invent unstated sample sizes or claim a full-paper quality review.
8. Use important-author matches as an additional relevance signal. Resolve ambiguous names by identifiers, affiliations and subject area. Never exclude strong work by other authors unless the user explicitly requests an author-only watch. Verify citation relationships before stating them; when unavailable, report the limitation and retain topic discovery.
9. Deduplicate normalized DOI against Today, Archive and the persistent delivery log, including deleted shortlist rows. Use verified identity checks for DOI-less records; include them only if the user's policy allows it.
10. Include all strong matches without a forced quota. Prefer no qualifying results to weak or fabricated additions. Record coverage limitations without claiming exhaustiveness.

## Save and report

Read the current destination metadata, exact headers, relevant records and validation before writing. Preserve all user notes, ratings and prior edits. Append only new verified records. Verify writes before marking delivery or advancing the successful-search boundary. Recover partial failures idempotently using DOI checks.

Leave user ratings blank for new papers. Keep machine assessments distinct from user ratings. Apply the configured archive rule only in an authorized archive run; verify destination entries before removing exact matching source rows.

Create or update schedules only when requested. Check existing tasks privately first to avoid duplicates. Include the private effective configuration and destination in the task instructions; do not rely solely on future availability of this skill. Keep search and archive schedules independent unless the user requests both changed. A manual refresh means execute now, not merely queue a later run.

Report the searched date range, additions count, sources used and significant limitations. Link the verified editable destination once. Explain how to rate papers and the applicable archive rule. Claim completion only for actions confirmed by tool results. If the user asks for a GitHub-ready copy, include only the reusable skill folder and generic references; do not publish or choose a repository without user direction.
