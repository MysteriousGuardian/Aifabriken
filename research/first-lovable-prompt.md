# First Lovable build prompt — ready to send after scope is settled

Use the Vibeathon workspace (`workspace_01kexpath1epn88ffspx08xzzf`). Attach `research.json` from this research package. This prompt has not been sent.

---

Build an engineer-facing interactive demonstrator titled “Customer Job Twin: Early-entry Concrete Joint Cutting.” The customer job is a professional operator cutting initial contraction joints in one fresh outdoor concrete slab. Use the attached reviewed research JSON as the source of truth. This first increment is a curated evidence explorer.

Create one clean desktop-friendly page with five selectable stages in this exact order: PLAN → PREPARE → MOVE → OPERATE → FINISH. Explain that real work can revisit stages. Each stage shows its actors, tasks, equipment, dependencies, pain points and evidence gaps. Default to PLAN.

When a pain point is selected, open a panel with three explicitly separate sections: “Observed evidence,” “Interpretation,” and “Response hypotheses.” Resolve links from pain point to observations to sources, and from pain point to opportunities. Evidence cards must display stable IDs, paraphrase, source title/type, publication date or “Unknown,” locator, actor/task/conditions, and limitations. Provide an “Open source” link in a new tab; use the exact supplied URL. No embedded copyrighted source text or video claims.

Add a compact opportunity comparison view using the supplied four 1–3 score inputs. Compute total as their sum and display components and the rubric. Label every response “Untested hypothesis” and every score “Provisional judgment.” Show the validation experiment. Tie-break with supplied rank. Add text search over reviewed observations, pain points and opportunities, and stage filtering. Show unique source-family counts separately from observation counts; never label them prevalence.

Display “Curated public research · reviewed 14 October 2026” and a visible explanation: loading, search, relationship traversal and scoring are automatic; research selection, extraction and interpretation are curated. Keep evidence gaps visible. Distinguish low/medium confidence from observed/validated outcomes; none of these proposals is validated.

Use a lightweight React/TypeScript implementation with local JSON. Keep data in `src/data/research.json`; keep relation lookup/validation in a small separate module. No login, cloud database, crawler, paid API, generated research claims, telemetry, physical simulation or automatic safety/start-time recommendations in this increment. Do not replace the supplied dataset with mock findings. Missing references must show a clear error instead of fabricated content.

Acceptance criteria:
1. All five stages are navigable and show tasks plus gaps, including MOVE and FINISH.
2. PLAN → P01 → E03 → its source and O01 is fully traversable in the UI.
3. Every opportunity has at least one valid pain-point path to a reviewed observation and source.
4. Unknown dates render as unknown; no invented savings, costs, injury rates, ROI or prevalence.
5. Scores equal the sum of the four supplied values; rank labels match the dataset.
6. Search has a useful empty state, filters can be cleared, and evidence links open the exact supplied URLs.
7. Observation, interpretation and response remain visually distinct; hypotheses and automation limits are visible.
8. Source E08 clearly says its wet-saw fact sheet does not establish suitability of this dry setup.
9. Keyboard focus and readable contrast support the demo; no horizontal overflow at a normal laptop viewport.

After building, report changed files, how you checked these criteria, and remaining limitations. Stop after this increment so we can inspect the preview and code before requesting further work. Preserve working features in follow-up requests.
