## Hi, I'm Abdulsamed

**Test Automation Engineer · GenAI-driven QA** — İstanbul, Türkiye

I build test automation for web, mobile and API, and LLM-powered tools that generate and evaluate tests.
Currently a QA & Test Automation Engineer at [Eriklabs](https://eriklabs.io), testing POS and back-office
systems for restaurant chains. On [SmartCase](https://smartcase.dev), our AI-powered
test automation platform, I work on PDF-to-scenario generation, LLM-driven self-healing of failed steps
and its MCP server for IDE agents.

## Agentic QA pipeline (built and in daily use)

An agentic QA workflow I built and use daily on a client project. It carries a task from analysis
through test design, test data, execution and automation to reporting.

- Claude Code skills and sub-agents, with work split across models by task cost
- A custom MCP server that lets the agent work with the web app under test
- Python helper tools for change analysis, test-document checks and test-data preparation
- A Chrome recorder extension that masks sensitive data at capture time and exports Playwright code
- Human approval built in: test cases come from an approved scope, and nothing is posted without sign-off

## Projects

> These repositories are private. I'm happy to walk through the code on request.

### QA Artifact Generator

Turns a free-text requirement or bug report (Turkish or English) into three QA artifacts:
a structured test case, a Gherkin feature and a Playwright test skeleton.

- **Stack:** TypeScript (strict), Node.js / Express, React + Vite, Claude API, Zod, Vitest, Docker
- Forced tool-use keeps the LLM output schema-conformant; a bounded retry loop covers what JSON Schema can't express
- Server tests run fully offline against a dependency-injected mock client
- Eval pipeline on an 18-case golden dataset (mixed TR/EN) with an 80% pass-rate gate: generated Playwright code
  is type-checked and its steps are compared with the Gherkin scenario

### PDF-to-Test-Scenario Generator

A research tool that generates test scenarios from PDF requirement documents and benchmarks LLMs and prompting
methods against a 95-item gold checklist, scored by an LLM judge.

- **Stack:** Python, FastAPI, JavaScript
- Compared open-weight models (70–120B) with a frontier model on coverage, ungrounded tests, time and cost
- A multi-stage pipeline lifted an open-weight 80B model from **15.5% to 83.5%** coverage (**94.7%** with
  self-consistency) at 2–4× lower cost than the frontier model
- Context-window experiments (4K–262K tokens): the multi-stage pipeline keeps ~80% coverage even at 4K

| Method (open-weight 80B model) | Coverage |
|---|---|
| Single plain prompt | 15.5% |
| Single strong prompt | 55.8% |
| Multi-stage pipeline | 83.5% |
| Multi-stage + self-consistency | 94.7% |

## Tech stack

- **Languages:** Java · TypeScript · Python · JavaScript · SQL
- **Test automation:** Selenium · WebdriverIO · Playwright · Appium · Cucumber (BDD) · JUnit · TestNG
- **API & performance:** RestAssured · Postman · Swagger/OpenAPI · Apache JMeter
- **GenAI:** Claude Code (skills, sub-agents) · MCP server development · Claude API · LLM evaluation (golden datasets, LLM-as-judge)
- **Backend & DevOps:** Express · FastAPI · Docker · Jenkins · Azure DevOps · Kafka · MSSQL

## Contact

[LinkedIn](https://www.linkedin.com/in/abdulsamederyigit)
