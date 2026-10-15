# Small Organisation Ops

**Lightweight operating tools for organisations that need discipline but do not need another platform.**

Small organisations still need to know what work is underway, what could go wrong, which policies matter and why important decisions were made. They do not automatically need Jira, a GRC platform, a PMO tool or a specialist administrator to maintain that information.

These templates are deliberately small. They are designed to be understood at a glance, maintained without specialist administration and used in ordinary meetings.

> **If maintaining the register becomes more work than running the work, the register has failed.**

## The four registers

| Register | Question it answers | Review habit |
|---|---|---|
| [Project register](project-register/README.md) | What work is underway and what needs attention next? | Weekly or fortnightly |
| [Risk register](risk-register/README.md) | What could materially prevent the organisation achieving its objectives? | Monthly and when conditions change |
| [Policy register](policy-register/README.md) | Which policies exist, who owns them and how do we know they are operating? | Monthly by exception; formal review by date |
| [Decision register](decision-register/README.md) | What important decisions were made, why, and when should they be revisited? | At the meeting where the decision is made |

Each register is intentionally independent. Use only the ones you need.

## How they work together

```text
WORK / PROJECT
     |
     +---- exposes ----> RISK
     |                    |
     |                    +---- may require ----> POLICY / CONTROL
     |
     +---- requires ----> DECISION
                              |
                              +---- changes ----> WORK / PROJECT
```

Do not duplicate information merely because two registers touch the same subject. Reference the other register in the existing free-text field instead.

Example:

- a project row can say `R-03 remains the main delivery risk` in **Comments / Actions / Risks**;
- a risk action can say `D-04 approved the interim control`;
- a decision rationale can say `supports Project: Community Hall Roof`.

The identifiers are optional. They are useful when the registers are discussed together but do not justify new columns.

## Operating principles

### 1. One row should tell you enough to act

A register is not a filing cabinet. If a row needs a separate briefing to explain what it means, rewrite the row.

### 2. Keep ownership singular

Use one accountable owner in the register. Other contributors can be mentioned in the comments or action text.

### 3. Record the next useful thing

For projects, the most valuable forward-looking field is the next milestone/date. For risks, it is the next action/review. For policies, it is the review date. For decisions, it is the revisit trigger.

### 4. Use free text deliberately

The larger comments/action fields are not a failure of data modelling. They are where small teams can keep context together instead of fragmenting it across fifteen rarely maintained columns.

### 5. Archive finished material

Do not leave completed work, expired risks and superseded decisions in the live view forever. Move them to an archive periodically so the current register remains readable.

## A practical operating rhythm

See [OPERATING-RHYTHM.md](OPERATING-RHYTHM.md).

The short version:

- project register: review active work weekly or fortnightly;
- risk register: review monthly and when a material condition changes;
- policy register: scan monthly for due/overdue reviews and evidence gaps;
- decision register: update when a material decision is made, not retrospectively months later;
- archive: quarterly or whenever the live view becomes noisy.

## Worked example

[`examples/fictional-community-organisation`](examples/fictional-community-organisation/README.md) shows all four registers for **Wattle Creek Community Association**, a fictional volunteer-run organisation managing a small hall, community programmes and a modest technology estate.

The example is deliberately ordinary. The point is to show how the registers work together without requiring a platform or specialist governance function.

## Repository structure

```text
small-organisation-ops/
├── README.md
├── OPERATING-RHYTHM.md
├── VERSION
├── CHANGELOG.md
├── LICENSE
├── project-register/
│   ├── README.md
│   └── template.md
├── risk-register/
│   ├── README.md
│   └── template.md
├── policy-register/
│   ├── README.md
│   └── template.md
├── decision-register/
│   ├── README.md
│   └── template.md
└── examples/
    └── fictional-community-organisation/
        ├── README.md
        ├── project-register.md
        ├── risk-register.md
        ├── policy-register.md
        └── decision-register.md
```

## What this is not

This is not:

- a replacement for regulated records management;
- a full project-management methodology;
- a quantitative enterprise-risk framework;
- a policy authoring standard;
- a legal or compliance system;
- an argument against specialist platforms where scale, regulation or workflow complexity justifies them.

The proposition is narrower: **start with the smallest operating structure that makes ownership, status and follow-through visible. Add machinery only when the work earns it.**

## Licence

MIT. See [LICENSE](LICENSE).
