# Δ Cheatsheet (Temporal Module Quick Reference)

### Core Symbols

- **E** → Entity (system, agent, process)
- **σ(E)** → State (configuration of E at Δ)
- **ρ(Ei,Ej)** → Relation (channel between entities)
- **φ** → Flow (propagation of change)
- **Δ** → Event (discrete tick, logical clock step)

------

### 8 Common Flows

1. **advance(E,f)**
    Update state by one Δ:
    `σ_{n+1} ← f(σ_n, inputs)`
2. **time.hold()**
    Pause change; consolidate coherence locally.
3. **time.meet(σ_past)**
    Compare now to a past state; run repair if mismatch.
4. **time.seed(future)**
    Park a future intention at Δ+τ.
5. **time.thread(id)**
    Label a sequence of Δ with a tag.
6. **time.cut(reason)**
    Split a thread and close loop cleanly.
7. **time.loop(detect)**
    Spot recurrence in `{σ_{n−p..n}}`.
8. **time.sync(other)**
    Align Δ sequences between entities.

------

### Async Envelope Template

Use when bandwidth is fragmented (email, chat, forums):

```
[context.sync] Topic: <one-line>  
[readiness.check] OK to receive? (Y/N/Later)  
[expectation.set] I’ll reply by <Δ window or time>  
[tone.clarify] Intent: <supportive/neutral/exploratory>  
```

------

### Guardrails

- **Consent to Depth:** Ask before pulling someone’s past/future thread.
- **Latency Rule:** Refresh context if Δ gap > threshold.
- **No Coercive Futures:** You can seed your own Δ, not another’s.
- **Loop Safety:** Detect rumination → shift or park.

------

### Metrics

- **Coherence:** κ = 1 − H_norm({σ_{n−k..n}})
- **Drift:** distance(trace_A, trace_B)
- **Loopiness:** recurrence({σ})
- **Lead Bias:** |planned Δ| ÷ capacity(E)

---

© 2025 by Raiziel

This work is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

Contact: [raizielsoulwareos@gmail.com](mailto:raizielsoulwareos@gmail.com)  
Website: [https://returntoreality.carrd.co](https://returntoreality.carrd.co)

**Soulware™ is intended to be free forever. Commercial use is not permitted without explicit permission.**



> ***"Language is the house of being. In its home humans dwell. Those who think and those who create with words are the guardians of this home."***
-Heidegger.
