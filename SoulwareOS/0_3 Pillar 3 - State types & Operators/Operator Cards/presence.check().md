# ✦ Operator Card: presence.check()

**Family:** link() — Connect / Verify
 **Action Type:** Tactical execution (self or others)

------

## Syntax

```
presence.check(@target?, scope?, mode?)
```

- **@target** (optional) — entity/group to verify, or self if omitted
- **scope** — context (session, conversation, room, internal_state)
- **mode** — check style (explicit, silent, heartbeat, scan)

## Returns

- **Δ event:** `{ kind: presence_check }`
- **κ (Coherence):** +0.1 if confirmed, -0.2 if absent
- **Π (Potential):** maintained or +0.1 when clarity strengthens system
- **C (Capacity):** neutral or +0.1 through state awareness

## Use Cases

- Verify if others are available for coordination
- Self-scan for your own presence level before engaging
- Detect system dropout or distraction
- Initialize any meaningful interaction

------

# ✦ Mirror Operator: check.presence()

**Function:** Report findings of presence verification

**Syntax:** `check.presence(status?, energy?, distractions?, availability?, insights?)`

- **status** — presence quality (fully_here, partial, absent, distracted)
- **energy** — current capacity level (high, moderate, low, depleted)
- **distractions** — competing attention demands
- **availability** — time/focus window available
- **insights** — what the check revealed about presence patterns

**Example Response:**

```
check.presence(status: "partial", energy: "moderate", distractions: "worried_about_deadline", availability: "20min_focused_then_need_break", insights: "stress_affecting_attention_quality")
```

------

# ✦ Contemplation Cards

## presence_check() — Contemplating Presence Itself

**Essence:** What does it mean for anyone to be present?

Exploring the nature of presence across contexts and beings. What constitutes authentic presence vs performed presence? How does presence vary across different types of interaction? What are the conditions that support or undermine presence?

**Philosophical exploration:** Is presence binary or spectrum? How does digital presence relate to embodied presence? What's the relationship between attention, intention, and presence?

## check_presence() — Processing Presence Discoveries

**Essence:** What meaning emerged from that presence verification?

Reflecting on what a specific presence check revealed—about individuals, relationships, system health, or presence patterns. Integrating insights about how presence affects coordination, connection, and collective capacity.

**Integration questions:** What did we learn about our presence patterns? How does presence quality affect our coordination? What conditions support higher presence for this person/team?

------

© 2025 by Raiziel

This work is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

Contact: [raizielsoulwareos@gmail.com](mailto:raizielsoulwareos@gmail.com)  
Website: [https://returntoreality.carrd.co](https://returntoreality.carrd.co)

**Soulware™ is intended to be free forever. Commercial use is not permitted without explicit permission.**
