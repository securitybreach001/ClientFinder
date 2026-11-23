# ClientFinder

[Open the web app](https://securitybreach001.github.io/ClientFinder/)

ClientFinder is a Vancouver prospecting and sales CRM. Open the site in a regular browser profile. In **Data & settings**, import a batch from the City of Vancouver or add a manually researched business. Open a prospect in **Explorer** to check its available licence history and record verified research. Use **Research Queue** to qualify businesses and **Calling Queue** to log manual calls and schedule follow-ups.

## Architecture and progress

- A static HTML, CSS, and JavaScript app runs on GitHub Pages. No installation, server credentials, or paid API is needed.
- Official City API queries import up to 500 issued Vancouver licences per batch. History is queried on demand across the current, 2013–2024, and 1997–2012 datasets. The matching rules require a corroborating address, province, and business name, with postal codes checked when both records have one. Excluded matches stay excluded when history is refreshed.
- CRM records, research notes, call history, and do-not-call flags are saved to browser storage. They are scoped to the browser profile and site origin. Export a JSON backup before clearing browsing data or switching profiles.
- Included in the MVP are search and age filters, score explanations and completeness, website classifications, research and calling queues, bilingual call scripts, follow-ups, a sales pipeline, and JSON backup/restore.

## Known limits and next steps

This release uses targeted searches and browser storage. Full historical bulk indexing, moved-business matching, configurable scoring and packages, CSV exchange, richer analytics, and automated regression tests are outstanding. Name prefiltering can miss changed names and spelling variants. The historical query is capped at 100 candidates per dataset. Distinct licence years indicate recorded evidence and do not establish founding date or uninterrupted operation.

Contains information licensed under the [Open Government Licence – Vancouver](https://opendata.vancouver.ca/pages/licence/).
