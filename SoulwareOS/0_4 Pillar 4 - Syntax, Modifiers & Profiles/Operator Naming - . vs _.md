## Soulware Operator Naming: Dot (.) vs Underscore (_)

------

## Overview

Soulware’s protocol language distinguishes between two major naming conventions for operators and entities: the **dot (.)** and the **underscore (_) .** Each serves a distinct role in conveying meaning, structure, and flexibility.

------

## Dot (.) Notation

- **Purpose:**
  Signifies a relationship of **ownership, hierarchy, or structural linkage** (like subject-method or object-property).
- **Usage:**
  Best suited to modeling system-level protocols, methods of objects, or actions relating to a specific domain or entity.
- **Examples:**
  - `body.nourish()` — The `nourish` operation as it applies to the `body`.
  - `user.login()` — A `login` process for the `user` entity.
  - `sensor.measure()` — Triggers measurement functionality for the sensor.

------

## Underscore (_) Notation

- **Purpose:**
  Enables the creation of **unique, composite, or multi-word identifiers and entities**.
  Captures the infinite variability required in naming resources, files, protocols, and actions that do not correspond to a strict hierarchy.
- **Usage:**
  Ideal for:
  - Named instances or objects (files, projects, documented protocols).
  - Multi-word operators that form a single atomic action or identifier.
  - Infinite user-generated variations and contextual entities.
- **Examples:**
  - `project_sanchez()` — A unique project entity.
  - `user_ada_lovelace()` — The profile or instance for a particular user.
  - `meeting_notes_2025_09_10()` — A specific record for a date.
  - `optimize_timeline()` — An atomic multi-word operation.

------

## Combining Both in Practice

You can leverage both conventions together for clarity and expressive power:

- `meta.review(project_sanchez())`
  - Uses `project_sanchez` as a unique entity and passes it to the `review` operator under the `meta` protocol.
- `archive.save(meeting_notes_2025_09_10())`
  - Archives a specific meeting notes file.

------

## Design Benefits

- **Clarity:**
  Dots clarify structure, inheritance, and general protocols; underscores disambiguate unique, multi-word names.
- **Infinite Practicality:**
  **Underscore-style entities and actions** allow for endless, context-rich expansion—any entity or operation relevant to a real domain can be explicitly represented.
- **Consistency:**
  Keeping these conventions clear aids both human and automated parsing within Soulware, promoting scalable, living language for evolving systems.

------

## Best Practices

- Use **dot (.)** for structural operators and method-like actions tied to a system, object, or domain.
- Use **underscore (_) ** for instance naming, files, user- or context-generated identifiers, and composite atomic actions.
- Avoid mixing dots and underscores in the same root segment; reserve combinations for clear structural intentions.
- Document naming choices for major entity types and core system operators to ensure clarity and discoverability.

------

These conventions bring expressive precision to Soulware, supporting the emergence of a living, compositional protocol language ready for evolving domains and infinite creative use.

---

© 2025 by Raiziel

This work is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

Contact: [raizielsoulwareos@gmail.com](mailto:raizielsoulwareos@gmail.com)  
Website: [https://returntoreality.carrd.co](https://returntoreality.carrd.co)

**Soulware™ is intended to be free forever. Commercial use is not permitted without explicit permission.**
