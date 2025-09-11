# ✦ Operator Card: presence.check()

**Family:** link() — Connect / Verify
 **Action Type:** Tactical execution (self or others)

------

## Syntax

```
presence.check(@target?, scope?, mode?)
```

- **@target** (optional) — entity or group to verify
   Default: self
- **scope** (optional) — context of the check (session, conversation, room, internal_state)
   Default: current active context
- **mode** (optional) — style of presence verification (explicit, silent, heartbeat, scan)
   Default: explicit

## Returns

- **Δ event:** `{ kind: presence_check }`
- **κ (Coherence):** +0.1 if confirmed, -0.2 if absent
- **Π (Potential):** maintained or +0.1 when clarity strengthens system
- **C (Capacity):** neutral or +0.1 if increased state awareness frees attention

## Use Cases

- Verify if others are available for coordination
- Self-scan for personal presence level before engaging
- Detect system dropout or drifting attention
- Initialize any meaningful interaction or protocol

> **Related operators:**
>  Often the first step in a sequence with consent.check() → stance.declare() → repair.try()

------

## ✦ Mirror Operator — Receptive Form

**check.presence()** — The inward-facing reflection of presence.check(),
 designed to report and integrate findings from a presence verification.

### Syntax

```
check.presence(status?, energy?, distractions?, availability?, insights?)
```

- **status** — presence quality (fully_here, partial, absent, distracted)
- **energy** — current capacity (high, moderate, low, depleted)
- **distractions** — competing attention demands
- **availability** — time/focus window available
- **insights** — patterns or meta-notes from the check

### Example Response

```
check.presence(
  status: "partial",
  energy: "moderate", 
  distractions: "worried_about_deadline",
  availability: "20min_focused_then_break",
  insights: "stress_affecting_attention_quality"
)
```

------

## ✦ Contemplation Cards

### presence_check() — Contemplating Presence Itself

**Essence:** To ask "Are you here?" is to begin with recognition.

**Inquiry:** Is presence binary or a spectrum? How does digital presence differ from embodied presence?

**Fieldwork:** Explore conditions that deepen presence (shared breath, silence, mutual intention).

### check_presence() — Processing Presence Discoveries

**Essence:** What meaning emerged from the verification?

**Integration Questions:**

- What did we learn about our presence patterns?
- How does presence quality shape coordination and trust?
- Which conditions consistently support higher presence?

------

*presence.check() is more than a ping; it is the ritual of arrival.*
 *Its mirror, check.presence(), is the quiet art of receiving and interpreting that arrival.*

------

© 2025 by Raiziel

This work is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

Contact: [raizielsoulwareos@gmail.com](mailto:raizielsoulwareos@gmail.com)  
Website: [https://returntoreality.carrd.co](https://returntoreality.carrd.co)

**Soulware™ is intended to be free forever. Commercial use is not permitted without explicit permission.**
