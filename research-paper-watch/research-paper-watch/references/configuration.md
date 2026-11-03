# Configuration and onboarding

## Ask in small groups

Start with: “What topics or research questions should I monitor? List required concepts, useful synonyms and anything to exclude.”

Then ask: “Which industries, countries, organizations or outcomes should I focus on? Which are mandatory, and which are preferences?”

Ask: “Which journal list or ranking system should qualify, and which edition and ratings should I use? Do you want empirical papers, reviews, conceptual articles or all journal research?”

Ask: “Who are the important authors or researchers in your field? Provide names and, if available, ORCID IDs, Scopus Author IDs or profile links. Should I prioritize their papers, papers citing their work, or both?” Allow an empty author list. Resolve names before author-specific searches. Never promise exhaustive citation tracking.

Ask: “How far back should the first search go? How often should I update results, and on which weekday/time and timezone?” Ask schedule details only for recurring work.

Ask: “Which editable spreadsheet should I use, or should I create one? What rating scale, archive threshold and archiving schedule would you like?” Do not ask for an email unless sharing is explicitly requested and needed.

Offer as defaults: 30-day initial window; abstract-based screening; paywalled and open-access papers equal; 1–5 user ratings; archive 4–5. Keep scheduling manual until recurrence is requested. Do not silently impose a journal-ranking requirement when none was chosen.

## Private configuration shape

Use a user-controlled private destination (for example its Instructions tab) to persist settings. Save only within authorized scope. Never save private settings in the public skill folder.

```yaml
topics:
  - label: Example research theme
    required_concept_groups:
      - [primary concept, synonym]
      - [required secondary concept, alternative]
    preferred_keywords: []
excluded_topics: []
context:
  industries: []
  countries: []
  organization_types: []
  outcomes: []
  strict_requirements: []
important_authors:
  - name: Example Researcher
    orcid: null
    scopus_author_id: null
    profile_url: null
    priority: authored_papers # or citing_papers or both
ranking:
  system: null
  edition: null
  private_reference: null
  allowed_ratings: []
  strict: false
article_types: [empirical, review, conceptual]
require_verified_doi: true
assessment_basis: abstract
access_policy: include_paywalled_and_open_access
preferred_source: Scopus_when_accessible
initial_window_days: 30
schedule:
  frequency: manual
  weekday: null
  local_time: null
  timezone: null
destination:
  provider: null
  private_spreadsheet_id: null
rating:
  allowed_values: [1, 2, 3, 4, 5]
  archive_values: [4, 5]
archive_schedule:
  frequency: manual
  local_time: null
state:
  baseline_complete: false
  searched_through: null
  last_successful_run: null
```

Resolve one effective configuration per user/project. Preserve unrelated fields when updating. Do not reset the search boundary on a schedule-only change. When topics change materially, offer or follow the user's requested retrospective search and keep the prior delivery history. Calculate a 30-day inclusive baseline as local today minus 29 days through today; for example 5 October through 3 November. Do not hardcode this example in an automation.
