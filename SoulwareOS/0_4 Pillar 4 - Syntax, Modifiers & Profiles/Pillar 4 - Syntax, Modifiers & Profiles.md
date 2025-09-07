## Pillar 4: Syntax, Modifiers, & Profiles

## Introduction

Soulware’s power comes alive in its syntax—the grammar for composing, chaining, and tracking operator moves.
Layer 4 gives clear, minimal rules for writing, modifying, and adapting operators, plus tools for creating profiles that tune system response to different agents, groups, or contexts.

------

## 1. Core Syntax Patterns

Operators are called using **subject.verb(args)** or **verb.subject(args)**—expressive and receptive polarity.

- Standard formats:
  - Express: `stance.declare("I’m here for repair.")`
  - Receive: `declare.stance("received")`
  - Async: `presence.check(channel: async, eta: Tue 10a)`
- Chaining:
  - Multiple moves in sequence:
    `consent.ask().sync.readiness().repair.try()`
- Nesting:
  - Operators as arguments:
    `repair.try(intent.verify("is this honest?"))`
- Aliasing:
  - Shortcuts for common operators:
    `ping` (for `presence.check()`), `rest` (for `pause.offer()`)

------

## 2. Modifiers: Shaping Operator Dynamics

Modifiers are keywords or argument flags that adjust operator “flavor.”

- Examples:
  - Duration/Window: `pause.offer(5min)`
  - Intensity: `sync.readiness(level: high)`
  - Scope: `context.sync(scope: group)`
  - Feedback/closure: `repair.try(callback: reflect.meta())`
- Special tags for edge cases or meta:
  - `boundary.hold(strict)` vs. `boundary.hold(soft)`
  - `loop.close(silent)` vs. `loop.close(alert)`
  - `consent.ask(conditional)`

**Modifiers let one canonical operator work flexibly in any situation.**

------

## 3. Profiles: Contextualizing Operators

Profiles are custom “views” specifying how Soulware’s language/behavior adapts to user roles, groups, contexts, or ecosystems.

- **Individual**:
  - `profile.user1:`
    Defaults: `readiness.sync(level: low)`, `pause.offer(5min)`
- **Group**:
  - `profile.team:`
    Protocol: `context.sync(scope: group, frequency: weekly)`
    Modifiers: `boundary.hold(strict)`, `thread.cut(on conflict)`
- **Situation (ritual, repair, governance):**
  - `profile.ritual:`
    Sequenced protocol:
    - `stance.declare()`
    - `intent.verify()`
    - `repair.try()`

Profiles are defined as dictionaries or config lists, then called to inform which operators are run, how, and with what modifiers.

------

## 4. Example Section: Real-World Compositions

Sample “moves” for common scenarios—showing combos of syntax, modifiers, and profiles in action.

| Context         | Syntax Call                                        | Outcome                                     |
| :-------------- | :------------------------------------------------- | :------------------------------------------ |
| Check-in Ritual | `profile.team: stance.declare().pause.offer()`     | Group opens, checks readiness, offers pause |
| Energy Audit    | `energy.scan(level: all).repair.try()`             | System checks energy, initiates repair      |
| Async Exit      | `exit.clean(channel: async, eta: tonight)`         | System processes clean async closure        |
| Personal Pause  | `profile.user1: pause.offer(10min, style: silent)` | Offers soft, time-bound pause               |

------

## 5. Parallel Processing & Await States (`@` Marker)

## Overview

Soulware protocols often require gathering multiple pieces of information—sometimes from many, sometimes as several independent queries to one person or system.
**The `@` marker embedded in operator calls signals an “await point”: an action pending a reply from a specific agent, group, or component.**

------

## Syntax

- Basic: `operator(..., @Target, ...)`
- Each call with `@Target` is open until that target responds.
- Works for single or multiple awaits—any mix of parties/queries.

------

## Single-Party, Multi-Request Example

A coach or app initiates a parallel check-in with a client:

```
textreadiness.sync(@Client, window: 5min)
intent.verify(@Client)
boundary.hold(@Client)
```

All three requests are “pending” for `@Client`.

## Client responds, individually or as a batch:

```
textsync.readiness(response: "low", @Client)
verify.intent(response: "clarify goals", @Client)
hold.boundary(response: "need 45min only", @Client)
```

Each response closes one “await”; protocol state updates as data arrives.

------

## Multi-Party, Multi-Query Example

Facilitator runs a protocol for two team members:

```
textreadiness.sync(@Alice)
intent.verify(@Alice)
boundary.hold(@Alice)
readiness.sync(@Bob)
intent.verify(@Bob)
```

- Awaiting three responses from Alice and two from Bob.
- They reply at their own pace; the protocol process is non-blocking.

------

## Mixed/Async Example

For remote or async workflows, await points are tracked in background—
*e.g., a system polls for status:*

```
textprogress.track(@Uploader1)
progress.track(@Uploader2)
```

When uploaders reply:

```
texttrack.progress(percent: 40, @Uploader2)
track.progress(percent: 100, @Uploader1)
```

Each completion triggers logic as needed.

------

## Why It Matters

- **Full modularity:** Any party/context can receive tailored requests, as many as needed.
- **Non-blocking:** Inputs can arrive in any order, tracked and processed as soon as they’re available.
- **Clean traceability:** Nothing gets lost—every request/response is uniquely mapped by its `@`-target.

------

## Best Practice

- Consider batching requests where contexts overlap, but preserve individual tracks for critical protocols.
- Always log which awaits are open, and finalize every `@` with a clear, matching response.
- Combine with modifiers and profiles as needed (e.g. `sync.readiness(@Alice, level: deep)`).

------

**The `@`-marker approach is Soulware’s native solution for real-world concurrency, async, and multi-party flows—making protocol both powerful and reliably auditable at all scales.**

---

## 6. How to Extend Syntax & Profiles

- Keep syntax simple and consistent—always `subject.verb(args)`
- Modifiers use plain key-value pairs or flags, no nested complexity
- Profiles are readable, modular configs—document all defaults
- Always audit for Mirror Rule consistency and K4 primitive grounding
- Share extensible templates and invite community feedback

------

## Closing

Layer 4 is **your toolkit for composability, context sensitivity, and live protocol design**.
Master it, and you can build custom Soulware flows for any person, team, or situation—always rooted in the K4 kernel, never locked to rigid scripts.
---

© 2025 by Raiziel

This work is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

Contact: [raizielsoulwareos@gmail.com](mailto:raizielsoulwareos@gmail.com)  
Website: [https://returntoreality.carrd.co](https://returntoreality.carrd.co)

**Soulware™ is intended to be free forever. Commercial use is not permitted without explicit permission.**


