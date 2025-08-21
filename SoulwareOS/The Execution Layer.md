## The Execution Layer: Channels & Profiles

To understand how SoulwareOS runs, we need to look at its two primary execution maps. As a simple summary:

- **Channels** = *where* meaning flows (inner / outer / mediator).
- **Profiles** = *how* meaning flows (baseline / autopilot / custom).

Think of it like driving a car: **Channels** are the different roads you can drive on (a private road, a public highway), while **Profiles** are the driving modes you select (eco mode, sport mode). Together, they give you conscious control over the entire context of your communication.

------



### Cognitive Channels

In SoulwareOS, communication is not just about the content of what you say, but also about the channels through which it flows. This model provides a conscious framework for managing the flow between your internal world and your shared reality, turning reactive communication into an executable process.

**1. Inner Channel (Self)** This is the private domain of your own thoughts, sensations, feelings, and internal rehearsals.

- **Purpose**: To run internal checks, name your own states, sketch drafts of what you might say, and align your internal stance before expressing anything.
- **Typical Ops**: `presence.check`, `stance.align`, `energy.scan`.
- **Visibility**: This channel is not shared by default. Its contents are private unless deliberately routed outward by the Mediator.

**2. Outer Channel (Shared Field)** This is the intersubjective space—the shared reality between you and others.

- **Purpose**: To signal to others, coordinate actions, repair misunderstandings, and co-create shared meaning.
- **Typical Ops**: `presence.ping`, `context.sync`, `consent.check`, `repair.try`.
- **Visibility**: This channel is public to the participants of the conversation and is subject to the system's Guardrails.

**3. Mediator Channel (Control Plane)** The Mediator is the silent observer and operator that stands between the Inner and Outer worlds.

- **Purpose**: To route information, select an Execution Profile, enforce Guardrails, and compile your internal state into a clear external expression.
- **Functions**:
  - **Route**: Decides whether an inner thought should remain private or be expressed.
  - **Select Profile**: Chooses the appropriate Execution Profile (Baseline, Autopilot, or Custom) for the situation.
  - **Enforce Guardrails**: Actively protects the interaction by running safety checks like `consent.check`.
  - **Compile**: Translates a complex internal state into a minimal, clear external signal (e.g., turning a feeling of anxiety into the words, "I'm feeling overwhelmed").
  - **Log & Learn**: Observes the results of communications and updates its own processes for the future.

**Common Dysfunctional Patterns**

- **The Leaky Channel (Weak Mediator)**: The Inner channel spills directly into the Outer without being routed or compiled, resulting in unfiltered and often harmful communication.
- **The Over-Filtered Channel (Overactive Mediator)**: The Mediator is so restrictive that the Outer expression becomes robotic or inauthentic, draining the `Trust-Reserve`.

------



### Execution Profiles

Execution Profiles are **parameter bundles** that set the defaults for how operators execute. They don't add new verbs to the language, but rather change the thresholds, timeouts, and automated responses to suit a specific conversational context.

**1. Baseline Profile (Ambient / Low-Effort)** The lightest touch, for when SoulwareOS is present but running quietly in the background.

- **Purpose**: To keep the vibe steady with minimal effort during casual conversation, stable relationships, or moments of ambient connection.
- **Defaults**: The presence threshold is lowered (`θ_presence=0.4`), timeouts are extended, and the system prefers light operators like `vibe.keep`, `spark.seed`, and `exit.clean`.
- **Behavior**: The system remains in this low-effort state by default and will only escalate if a specific trigger (like a state of `ache` or a `misread`) is detected.
- **Guardrail Bias**: Safety > Change.

**2. Autopilot Profile (Light Reactive Safety)** This profile runs routine, semi-automated patterns to handle predictable flows and reduce cognitive load.

- **Purpose**: To manage daily rituals, group coordination, or operational chatter with high efficiency.
- **Core Logic**: It operates on simple **event-action rules** to handle common, minor misalignments (e.g., `tone.mismatch` → triggers `tone.clarify`; `lag > Δ_max` → triggers `expectation.set`).
- **Guiding Principle**: The profile is fundamentally **conservative**. It will never deepen a conversation without an explicit `consent.check` and will default to safely parking the conversation (`pause.offer`) if it encounters complexity.
- **Guardrail Bias**: Efficiency > Novelty.

**3. Custom Profile (Deliberate / High-Intent)** A profile that is deliberately tuned by the Mediator for a specific, high-stakes context.

- **Purpose**: To adapt the language's full potential to a unique situation.
- **Use Case**: Therapy sessions, project sprints, conflict navigation, or complex asynchronous workflows where specific operators and Guardrails need to be emphasized.
- **Guardrail Bias**: Context-specific.
