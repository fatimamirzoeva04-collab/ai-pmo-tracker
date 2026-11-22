# AI Adoption PMO Tracker

> Illustrative sample data, not real company information.

A single-page tracker for running an AI adoption program at a global events and brand-experience agency. Built as a portfolio piece for a PMO / Innovation Projects internship.

**Live demo:** _add link after publishing_
**Author:** Fotima Mirzoeva, MS Project Management candidate at NYU · [LinkedIn](https://www.linkedin.com/in/fotima-mirzoeva-321778176)

## Why I built it

I built this while applying for an Innovation Projects internship at FIRST. I'm genuinely interested in the company, and I wanted to spend real time thinking through how I would do the job, not just describe it in a cover letter.

When an agency runs AI pilots across several offices, it gets hard to see what is on track, what is stuck, and what leadership needs to decide. This tracker is my answer to that: one place for initiatives, risks, test results and a weekly update.

## What it does

| Tab | Purpose |
| --- | --- |
| Initiatives | AI initiatives with owner, status, priority, next milestone and due date. Filters, a status chart and upcoming milestones. |
| RAID log | Risks, actions, issues and decisions from PMO meetings. Overdue follow-ups are highlighted. |
| AI Sprints | Two approaches to one task compared on time saved and quality, with a recommendation. |
| Benchmarking | Competitor and adjacent-industry AI moves, each with a source link. |
| Governance summary | A weekly leadership update generated from the other tabs, with a "Copy as text" button. |

Rows can be added, edited and deleted (delete has an undo). Data saves to the browser, and exports and imports as JSON.

## How to run it

Open `index.html` in a browser. There is nothing to install or build.

## How the governance summary is built

- **Counts by status:** every initiative, as it stands now.
- **Top 3 risks:** open risks, ranked by severity, then by earliest follow-up date.
- **Decisions this week:** decisions dated in the last 7 days, including today.
- **Asks:** open RAID items with the "Ask of leadership" field filled in.

## Data and privacy

- The AI Taskforce, its initiatives, owners, scores and dates are fictional. "Tool A" and "Tool B" are placeholders.
- The starter benchmark rows describe real, public announcements and link to their sources. The "What it means for us" notes are my own commentary.
- Data stays in the browser's `localStorage`. Nothing is sent to a server.
- Sample dates are set relative to the day you open the page. They become fixed after your first edit, and "Reset data" refreshes them.

## Technical notes

- One file: plain HTML, CSS and JavaScript, with no libraries.
- Storage calls are wrapped in `try/catch`, with a visible warning if saving fails.
- Imported files are validated, and text is escaped before display.
- Responsive layout, keyboard-accessible tabs, light and dark themes.

## Design decisions

- **The weekly summary is generated, not typed.** Status updates written by hand go stale and take time every week. If the update is built from the logs, keeping the logs current is the only job, and leadership always sees the same structure.
- **Risks have a severity level.** A long list of risks is hard to act on. Severity plus follow-up date decides which three reach leadership.
- **Sprints compare exactly two approaches.** A side-by-side test of two options is quick to run and easy to explain, and it ends in a clear recommendation: adopt A, adopt B, or test again.

## Limitations

- Data lives in one browser. There is no shared, multi-user version.
- The summary reports the current state and does not keep past weeks.
- Sprint results are entered by hand, so they are only as good as the testing behind them.

## What I would do next

- Save each weekly summary so leadership can see trends over time, not just this week.
- Move the data to a shared source, such as a spreadsheet or a database, so a whole team can update it.
- Add an adoption view: how many people in each office use the approved tools, and where training is needed.

## How AI was used

I built this with Claude Code. I wrote the brief describing what I wanted, including which sections it needed and what the sample data should look like. I tested each version myself and asked for changes where it fell short, for example a mobile-friendly layout. The structure follows the responsibilities in the internship posting: tracking initiatives, logging risks and decisions, testing AI approaches, benchmarking and leadership reporting.

## What I learned

Writing a clear brief is most of the work: the more precise I was about what each section was for, the better the result. Testing it as a user would, including on a phone, showed problems I would not have seen by reading the code. This was also my first project published on GitHub.
