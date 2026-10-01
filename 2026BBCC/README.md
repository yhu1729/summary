# 2026BBCC

## ChatGPT (July 2026)

### Summary

Mathlib's rapid growth creates software-engineering and social bottlenecks beyond the correctness guarantees supplied by the Lean proof checker. Drawing on a 1.9-million-line community library, the paper documents mechanisms that keep changes manageable without overwhelming maintainers. A deprecation system preserves renamed declarations and modules temporarily while issuing actionable migration warnings. Syntax and environment linters automate style, import-structure, redundancy, documentation, and maintainability checks, giving contributors immediate feedback and reserving reviewer attention for mathematical and architectural questions. Conscious dependency design, profiling, and specialized data structures control compilation and elaboration costs. Explicit metrics and issue-tracking practices make technical debt visible rather than allowing temporary exceptions to become permanent. Mandatory but decentralized code review spreads knowledge and onboards contributors; bots expose import and debt changes, suggest reviewers, and implement routine maintainer actions. A custom dashboard groups pull requests by state and accumulated review time, supporting systematic triage at scale. The account is primarily qualitative rather than a controlled evaluation, but it turns Mathlib's operational experience into reusable practices for other large formal libraries and open-source projects.

### Contributions

1. Documented a deprecation workflow that permits frequent refactoring without abruptly breaking downstream formalizations.
2. Classified semantic linters that automate local feedback and global coherence checks across a large Lean library.
3. Explained library-design and profiling practices used to contain compilation and elaboration costs.
4. Established measurable technical-debt tracking integrated into issue and pull-request workflows.
5. Presented scalable review and triage automation, including reviewer suggestions, status summaries, and a sortable dashboard.
