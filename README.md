# QA Engineer Portfolio — Felipe Siqueira

[![E2E](https://github.com/felipezoltowski/qa-portfolio/actions/workflows/ch06-e2e-nightly.yml/badge.svg)](…)
[![API](https://github.com/felipezoltowski/qa-portfolio/actions/workflows/ch05-api.yml/badge.svg)](…)
[![Performance](https://github.com/felipezoltowski/qa-portfolio/actions/workflows/ch07-performance.yml/badge.svg)](…)
[![Security & A11y](https://github.com/felipezoltowski/qa-portfolio/actions/workflows/ch08-security-a11y.yml/badge.svg)](…)

A working QA portfolio built over 12 weeks following the [roadmap.sh/qa](https://roadmap.sh/qa)
curriculum. Ten chapters, each one an artifact rather than a set of notes.

**Live reports:** [E2E](…) · [API](…) · [Performance](…) · [Accessibility](…)
**Stack:** TypeScript · Playwright · Postman/Newman · k6 · JMeter · OWASP ZAP · axe-core · GitHub Actions

---

## Chapters

| # | Chapter | What's in it | Stack |
|---|---|---|---|
| 01 | [Fundamentals](chapters/01-fundamentals) | Testing concepts, SDLC models, test oracles, risk matrix, ITIL | — |
| 02 | [Manual Testing](chapters/02-manual-testing) | 80 test cases, 15 bug reports, traceability matrix, exploratory charters | TestRail, Jira |
| 03 | [Web Foundations](chapters/03-web-foundations) | HAR analysis, DevTools diagnostics, selector strategy, Git drills | DevTools |
| 04 | [Observability](chapters/04-observability) | 30 SQL investigation queries, log analysis, escalation packets | SQL, Sentry, Grafana |
| 05 | [API Testing](chapters/05-api-testing) | 50 requests with assertions, JSON Schema, contract tests, CI | Postman, Newman |
| 06 | [**E2E Framework**](chapters/06-e2e-playwright) ⭐ | POM framework, fixtures, visual regression, cross-browser matrix | Playwright, Allure |
| 07 | [Performance](chapters/07-performance) | Smoke/load/stress/soak/spike, thresholds as CI gates | k6, JMeter, Lighthouse |
| 08 | [Security & A11y](chapters/08-security-a11y) | 12 OWASP challenges, ZAP triage, authz tests, WCAG audits | ZAP, Juice Shop, axe |
| 09 | [Support Toolkit](chapters/09-support-toolkit) | Runbooks, troubleshooting method, KB articles, escalation templates | — |
| 10 | [Capstone](chapters/10-capstone) | Full QA function on a real OSS app, ending in a go/no-go call | all of the above |

## Start here

If you have two minutes: [the E2E framework architecture](chapters/06-e2e-playwright/docs/ARCHITECTURE.md)
and [the capstone QA report](chapters/10-capstone/qa-report.md).

If you have ten: [locator strategy](chapters/06-e2e-playwright/docs/LOCATOR-STRATEGY.md),
[flaky-test policy](chapters/06-e2e-playwright/docs/FLAKY-TESTS.md), and
[performance results analysis](chapters/07-performance/docs/results-analysis.md).

## Running it

```bash
git clone https://github.com/felipezoltowski/qa-portfolio.git
cd qa-portfolio && npm install
npm run test:smoke        # ~2 min
```

Per-chapter instructions are in each chapter README.

## Coverage

[Roadmap node checklist](docs/ROADMAP-COVERAGE.md) — every roadmap.sh/qa node, linked to the
artifact that demonstrates it.

## Notes

- [Learning journal](docs/LEARNING-JOURNAL.md) — 12 weekly entries, including what didn't work
- [Tool decisions](docs/TOOL-DECISIONS.md) — why Playwright over Cypress, k6 over JMeter
- [ADRs](docs/adr) — architecture decisions with their reasoning

## Scope and authorisation

All security and load testing was performed against locally-hosted instances I control.
See [DISCLAIMER](chapters/08-security-a11y/DISCLAIMER.md).

## License

MIT — see [LICENSE](LICENSE). Study notes are my own writing; where I've drawn on the ISTQB
CTFL syllabus or other sources, they're cited in the file.
