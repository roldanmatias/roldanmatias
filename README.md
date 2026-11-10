# Matías Roldán

iOS engineer building AI agent tooling for iOS development: agents that fix builds, migrate Swift code and review pull requests, measured with evals and traces.

## Build log

- **2026-11-10 · Swift 6.4 language core** — [swift-mastery](https://github.com/roldanmatias/swift-mastery): 30 advanced Swift exercises plus a booking-engine capstone (StayKit), from value semantics and generics to typed throws, macros and ownership (`~Copyable`, `Span`, `InlineArray`, `UniqueArray`). 160 tests on Swift 6.4.2 (147 on 6.3.2), 25 verified compiler-error checks, and an `InlineArray` + `Span` hot path about 16× faster than a reused `Array`. Found two Swift compiler bugs along the way, with minimal reproducers.
- **2026-10-22 · Agent loop** — [xcfix](https://github.com/roldanmatias/ios-ai-agent-fundamentals/tree/01-agent-loop/01-agent-loop): a hand-written agent that fixes failing Swift builds and tests. Fixed 15/15 seeded bugs at $0.015 and 21.5 s per run on average, with harness-side verification, guardrails, git rollback, prompt caching (about 65% cheaper) and JSONL traces.

## Repositories

| Repository | What it is |
| --- | --- |
| [ios-ai-agent-fundamentals](https://github.com/roldanmatias/ios-ai-agent-fundamentals) | Agent loops from scratch, and study notes on agent design |
| [swift-mastery](https://github.com/roldanmatias/swift-mastery) | Advanced Swift 6.4 exercises with tests, benchmarks and interview notes, plus the StayKit capstone |
