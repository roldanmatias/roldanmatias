# Matías Roldán

iOS engineer building AI agent tooling for iOS development: agents that fix builds, migrate Swift code and review pull requests, measured with evals and traces.

## Repositories

| Repository | What it is |
| --- | --- |
| [ios-ai-agent-fundamentals](https://github.com/roldanmatias/ios-ai-agent-fundamentals) | Agent loops from scratch, and study notes on agent design |
| [swift-mastery](https://github.com/roldanmatias/swift-mastery) | Advanced Swift 6.4 language and concurrency exercises with tests, benchmarks and interview notes, plus the StayKit capstone |
| [swiftmigrator](https://github.com/roldanmatias/swiftmigrator) | An agent pipeline for large-scale Swift migrations: a 25-rule playbook and two modules (FeedKit and BookingSync) migrated by hand as ground truth. The scanner, pipeline and evals are next |

## Build log

- **2026-11-11 · Swift concurrency in depth** — [swift-mastery](https://github.com/roldanmatias/swift-mastery): 20 concurrency exercises covering isolation, actor reentrancy, `Sendable` and `Mutex`, regions and `sending`, isolated conformances, approachable concurrency (default `MainActor` isolation, `nonisolated(nonsending)`, `@concurrent`), structured concurrency, cancellation, streams, injected clocks and Swift 6.4's async `defer`. 75 deterministic tests (none sleep), green 10 runs in a row on Swift 6.4.2, plus 16 new verified compiler-error checks and an interview theory guide. Found that `withTaskCancellationShield` stops a binary from launching on macOS 26, even behind `#available`. In [swiftmigrator](https://github.com/roldanmatias/swiftmigrator): migrated a harder module, BookingSync (actors, async streams, two reentrancy bugs, a leaked polling task), by hand from 36 warnings to 0, and wrote playbook v2 (R17–R25). A regression test caught a thread-pool deadlock that the obvious `@unchecked Sendable` fix introduced.
- **2026-11-10 · Swift 6.4 language core** — [swift-mastery](https://github.com/roldanmatias/swift-mastery): 30 advanced Swift exercises plus a booking-engine capstone (StayKit), from value semantics and generics to typed throws, macros and ownership (`~Copyable`, `Span`, `InlineArray`, `UniqueArray`). 160 tests on Swift 6.4.2 (147 on 6.3.2), 25 verified compiler-error checks, and an `InlineArray` + `Span` hot path about 16× faster than a reused `Array`. Found two Swift compiler bugs along the way, with minimal reproducers.
- **2026-11-05 · Swift 6 migration playbook** — [swiftmigrator](https://github.com/roldanmatias/swiftmigrator): 16 numbered migration rules written to be loaded as agent prompt context, with a diagnostic-to-rule lookup table, guardrails and a JSON report format. Backed by FeedKit, a module migrated by hand from 18 complete-checking warnings to 0.
- **2026-10-22 · Agent loop** — [xcfix](https://github.com/roldanmatias/ios-ai-agent-fundamentals/tree/01-agent-loop/01-agent-loop): a hand-written agent that fixes failing Swift builds and tests. Fixed 15/15 seeded bugs at $0.015 and 21.5 s per run on average, with harness-side verification, guardrails, git rollback, prompt caching (about 65% cheaper) and JSONL traces.
