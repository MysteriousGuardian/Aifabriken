# Customer Job Twin — Browser QA report

## Run identity

- Tester: Pip / Strawberry Browser
- Run: 2026-10-14, approximately 11:55–11:59 Europe/Stockholm; final fingerprint recorded at 2026-10-14T09:59:01.560Z.
- Preview: https://id-preview--2ebd52fa-131b-4aba-9934-92d1e2646935.lovable.app/
- Tested deployment fingerprint: `/assets/index-DO3HIn-1.js`; commit/version not exposed and not verified. This identifies the observed bundle name, not a source-code review or cryptographic digest.
- UI state: reviewed baseline dated 2026-10-14; Draft import proposal v2 visibly pending integration review, not applied.
- Browser-reported app viewport: **876×799 CSS px**. Required 1366×768 and 1280×800 at 100%/125% zoom were **NOT TESTED**. No horizontal overflow measured at the observed width (`documentElement.scrollWidth = innerWidth = 876`). Zoom reset was attempted, but its effective percentage was not verified.
- Prior login blocker: resolved before this run by user-provided accessible tab. It no longer blocks the tested paths.

## Summary

Core five-step navigation and PLAN → P01 → E03a → source → O01 passed. No P0/P1 defect was observed in the exercised paths. Three P2 gaps and one P3 exact-copy mismatch were found. Full layout acceptance remains NOT TESTED. The current baseline correctly retains five opportunities while the draft is unapproved; four active opportunities must not be demanded yet.

No app source-code review, validator, local regression script, post-approval integration test, or research/UI modification was performed. Reading research.json for expected source URLs is not reviewing app implementation. Report ownership below is by team role, not a verified named assignee.

## Acceptance results

| # | Result | Observed result / qualification |
|---|---|---|
| 1 | FAIL | Initial attached app had PLAN selected. Required literal title/review line differ: heading `Early-entry Concrete Joint Cutting` with separate `Customer Job Twin`; document title uses an em dash; review line uses `(reviewed 2026-10-14)`. Cosmetic exact-copy mismatch, QA-04. |
| 2 | PASS | All five steps clickable in exact order; each showed actors, tasks, equipment, dependencies, pain points and evidence gaps. MOVE: P04 and transport/posture gaps. FINISH: P05 and disposal/acceptance/reporting gaps. |
| 3 | PASS | P01 has green A Observed evidence, blue B Interpretation and orange C Untested R&D hypothesis blocks, visually separated. |
| 4 | PASS | E03a shows ID, paraphrase, NRMCA CIP 6 title, industry association guidance type, 2014, `PDF p.2: item c and rules 1–3`, actor/task, conditions, tools, reviewed status and limitations. |
| 5 | PASS | E03a source click opened a separate tab at the exact URMCA PDF URL; original app remained open. |
| 6 | PASS | P01 hypothesis link has `#O01`; click reached O01 Readiness and handoff support, marked untested hypothesis with validation experiment and no predicted safe start time. |
| 7 | PASS | Reviewed baseline order O01/O02/O03/O05/O04; components and displayed sums 11/10/10/8/8 match 3+3+3+2, 3+2+2+3, 3+2+2+3, 2+1+2+3, 2+1+2+3. Provisional judgment and scale visible. |
| 8 | PASS | E04/E05/E06/E07 display `unknown date` rather than fabricated dates, blanks or epoch dates. Literal capitalization differs from `Unknown`, but missing-date semantics are preserved. |
| 9 | PASS | E02 2007; E08 2017-12; E10 2010-04. No day invented and no month/year shift. |
| 10 | PASS | E08 limitation explicitly says US wet-saw guidance, not suitability/compliance of dry Soff-Cut setup, not Swedish legal advice. |
| 11 | FAIL | P04/P05 panels show two observation IDs each, but no separate source-family and observation counters; cannot see required 1-family count. No counts labelled prevalence. QA-01. |
| 12 | PASS | Search `skid` result list contains E01b/E02a/E04a/O02/O04, no pain-point result or candidate observation result; `handoff` returns P01/O01. Main stage and previously open detail remain below the search results; E09/E10 are clearly candidate-only there, not counted as direct search hits. |
| 13 | PASS | `xyzzy` shows a helpful no-results statement including that absence in curated data is not absence in the field; Reset available, no crash/white page observed. |
| 14 | PASS | With PREPARE selected and query present, Reset clears query, restores PLAN, restores stage content and clears selected panels. |
| 15 | FAIL | Header says curated public research and no automatic discovery, but does not disclose which loading/search/traversal/arithmetic operations are automated versus source selection/extraction/interpretation being curated. QA-02. |
| 16 | PASS | Exercised visible UI contained no numerical savings, costs, injuries, ROI or prevalence claims. `Prevalence: unknown` / `not established` are uncertainty disclosures, not metrics. This is a visible-UI assessment, not a code/data exhaustive scan. |
| 17 | FAIL | Tabbing reached search, Reset, stages, observations, pain point, A evidence buttons, hypothesis link, source link and draft summary. Focus outlines observed; Space/Enter activated PLAN/PREPARE and P01. Escape did not dismiss P01; no focusable panel close control found. QA-03. Source link was keyboard-reachable; outbound activation used clicks in the source tests. Fresh keyboard-only reload and every interactive activation were not independently verified. |
| 18 | NOT TESTED | Exact required viewport/zoom combinations were not established. At observed 876×799 no document-wide horizontal overflow; panels inline, not overlaying navigation. This is not a substitute for prescribed layout acceptance. |
| 19 | PASS | Source links E01–E10 were clicked and each opened the exact URL in research.json, including E07/E08. External accessibility: E07 blocked by Cloudflare; E08 PDF rendered. Other source content availability not comprehensively assessed. |
| 20 | NOT TESTED | Conditional post-approval integration test is not applicable to pending draft state. Current five-item reviewed baseline is expected, not a failure. |
| 21 | NOT TESTED | Approved active tie-break behavior cannot be exercised before integration. Proposed policy is visibly labelled pending, not applied. |
| 22 | PASS | Current draft state: O06 only in draft proposal, from P06, `rank: none`, no reviewed score, ineligible while draft, with full observation/source review gate and explicit rejection of generic P02 substitution. Not in reviewed ranking. No reviewed counters are exposed, so underlying counter arithmetic is not verified. |
| 23 | PASS | Draft observations show explicit stage labels: E01e PREPARE/OPERATE; E01f OPERATE; E18a PLAN/PREPARE/OPERATE; E18b MOVE/FINISH; E19a PREPARE/OPERATE/FINISH. Reviewed stage lists were not promoted with these IDs. Post-approval bidirectional integration remains untested. |

## Defects and smallest fixes

### QA-01 · P2 · app/UI omission — missing source-family counters

- Criteria: #11.
- Reproduce: select MOVE → P04; inspect A and B; then FINISH → P05.
- Expected: separate reviewed observation count and deduplicated source-family count, each panel showing 2 observations from 1 family (E01/E04 shared family).
- Actual: observation buttons visible, no numerical observation/family counters.
- Owner: Person 2 / UI builder; Person 1 / research owner confirms family grouping semantics.
- Smallest fix: show two labelled counters derived only from eligible reviewed observations and deduplicated familyId; never name the counts prevalence. Keep draft/candidate records out.

### QA-02 · P2 · app disclosure omission — partial automation explanation

- Criterion: #15.
- Reproduce: inspect header disclosure and opportunities rubric; search page for automation/curation explanation.
- Expected: automated loading, search/filter, relationship traversal, score arithmetic; curated source selection/extraction/mapping/interpretation/hypotheses/score inputs; no automatic discovery.
- Actual: only curated-public-research/review date/no automatic discovery/prevalence-not-established are explained.
- Owner: Person 2 / UI builder, with copy confirmation from Person 1.
- Smallest fix: add concise visible automated-versus-curated disclosure using the existing research meta semantics, without suggesting AI discovery or validation that does not exist.

### QA-03 · P2 · app accessibility — panels cannot be dismissed with Escape/close

- Criterion: #17.
- Reproduce: PLAN → focus P01 → Space; panel opens; press Escape. Tab through evidence/hypothesis/source controls looking for a close action.
- Expected: Escape or a focusable close control dismisses panel and returns focus to opener.
- Actual: Escape leaves A/B/C panel unchanged; no focusable close control observed. Reset clears state, but is not a panel close-and-focus-return behavior.
- Owner: Person 2 / UI builder; Person 3 / QA retests focus return.
- Smallest fix: add labelled close buttons for pain-point/evidence panels and Escape handling, preserve opener reference and return focus on close. Retest Tab/Shift+Tab and Enter/Space.

### QA-04 · P3 · app copy — literal heading/review line mismatch

- Criterion: #1.
- Reproduce: view header/document title.
- Expected literal copy: `Customer Job Twin: Early-entry Concrete Joint Cutting` and `Curated public research · reviewed 14 October 2026`.
- Actual: product name split above heading; document title uses em dash; header review line uses ISO date in parentheses.
- Owner: Person 2 / UI builder, Person 1 accepts any intentional copy change.
- Smallest fix: use acceptance copy, or document team-approved updated criterion. This does not break the demo path.

## External-source observations — not app defects

- **E07 Ruwac:** exact app URL opens, then Cloudflare `Sorry, you have been blocked` / `You are unable to access ruwac.com`. Do not mislabel as wrong app link. For demo use visible locator/paraphrase with its commercial/no-exposure-measurement limitation; do not imply fresh page verification.
- **E08 OSHA:** exact PDF URL opens and renders `Walk-Behind Saws`, two pages. No access blocker in this pass. App retains wet-versus-dry applicability limitation.

## Exact source link verification

All links below were observed in the app and clicked to a new tab; each matches the reviewed dataset.

| Source | URL |
|---|---|
| E01 | https://content.tdr.dss.husqvarnagroup.net/pub000081368/doc000216012 |
| E02 | https://www.fhwa.dot.gov/pavement/concrete/pubs/07031/07031.pdf |
| E03 | https://urmca.org/wp-content/uploads/2018/09/06pr.pdf |
| E04 | https://www.speedcrete.co.uk/media/mageplaza/product_attachments/attachment_file/g/u/guide_to_soft_cut.pdf |
| E05 | https://orcaconcrete.com/services/ |
| E06 | https://fandsmasonry.com/concrete-services/saw-cutting/ |
| E07 | https://www.ruwac.com/concrete-saw-dust-control-early-entry-sawing/ |
| E08 | https://www.osha.gov/sites/default/files/publications/OSHA_FS-3633.pdf |
| E09 | https://content.tdr.dss.husqvarnagroup.net/pub000076326/doc000130319 |
| E10 | https://www-static-nw.husqvarna.com/hbd/tdrdownload/v2/pub000046120/doc000082649/OM/fhYKSGqA9fJVgwr93CWJsRwNP14 |

## Reference versions

- acceptance-checklist.md blob: `2934b31388b56e2b998f23cdb794ba542d100ffc`.
- research.json blob: `3212a9159e69725d56aa74770dbec80ee5fd0082`.
- qa-research-response.md blob: `d252c30093da2391051ec236539ce4396b6aef2e` (corrects #20/#22; baseline before approval must be retained).

Visual evidence of A/B/C separation captured locally as `qa/abc-panel.png` in the Strawberry chat workspace; not committed to the repo. All findings are browser observations, not implementation assertions.


## Codex follow-up — 2026-10-14 12:28–12:31 Europe/Stockholm

This section is an independent structural-data check. The Strawberry results above remain attributed to their original tester and bundle. They are not retested or claimed as Codex browser results.

### Blockers and current scope

- No newly verified P0/P1 app defect. Current app behavior cannot be certified in this session.
- Fresh in-app-browser preview attempt redirected to Lovable login. This is a test-access blocker, not evidence of an app regression or an external research-source failure. Strawberry is not exposed in this tool session. No authentication bypass attempted.
- App repository, synced branch and builder freeze are not verified. Installed-repository searches for Hackathon and public commit search did not identify a repo. This does not contradict the team's report that sync is connected.
- Lovable metadata at 12:26 reported ready/agentFinished and commit d97f7c1aa2a0c9c82d1894aa612c9f6ce726eb1c. It is NOT a verified tested deployment commit, and does not identify the earlier Strawberry bundle.
- Owner of access/version handoff: Person 2. Supply repository, branch, deployed commit/preview correspondence and a paused test window.

### Independently executed structural checks

Inputs: research.json blob 3212a9159e69725d56aa74770dbec80ee5fd0082; proposal v2 blob dd023d56c004674cf9640db715b2cb0c5afa2cb1. JSON parsed and assertions evaluated in Codex tool execution against fetched GitHub contents.

| Check | Result |
|---|---|
| Global unique IDs | PASS |
| All references | PASS |
| Stage backlinks excluding candidates | PASS |
| Candidate exclusion | PASS |
| Four integer scores 1..3 | PASS |
| P04 one source family | PASS |
| P05 one source family | PASS |
| O06 gated, P06 only | PASS |
| Inactive ranks null | PASS |
| All proposed observation stage backlinks covered | PASS |

Baseline sums recomputed as O01 11, O02 10, O03 10, O05 8, O04 8. There are 10 sources, 13 observations, 5 stages, 5 pain points and 5 baseline opportunities. Structural PASS does not validate customer need, source meaning, app filtering or runtime rendering.

### QA documentation correction completed

Updated acceptance-checklist.md in commit 95ce56ec6e78c42ffc76965569c2ee201ae25bf8:
- #20/#22 now distinguish baseline, separate draft and complete approved integration.
- Four active opportunities are conditional on documented approval and full O06 eligibility.
- Added concrete regression cases for inactive high scores, draft exclusion, P02 bypass, baseline compatibility, ties, backlinks, date precision and family counts.
- No research, UI or app data changed.

### Pending verification and ownership

| Work | Result | Owner / next action |
|---|---|---|
| App source review and filtering-before-sort | NOT TESTED | Person 2 supplies linked repo/branch; QA reads code |
| App regression tests | NOT TESTED | Agree exact test-file ownership before adding tests |
| Earlier QA-01/02/03 fixes | NOT RETESTED | Person 2 fixes/confirms; QA checks same declared version |
| Latest search/reset/navigation | NOT TESTED | Accessible preview and paused version required |
| Exact viewport/zoom and keyboard focus return | NOT TESTED | QA performs prescribed layout and keyboard cases |
| E07/E08 new browser check | NOT TESTED | Prior Strawberry results above remain attributed; no new access claim |
| Three-minute live demo rehearsal | NOT TESTED | Run Person 1's version-matched script against accessible frozen app |

Recommended retest sequence: fresh load/reload → five stages → PLAN/P01/E03a/source/O01 → ranking and draft exclusion → search/reset → family counters/disclosure → panel close/focus → required viewport/zoom combinations → timed demo. Preserve the existing report's external-source limitations. No deploy, build request or production-code change was made.


## Codex source review — repository access restored

Reviewed app snapshot: MysteriousGuardian/hackathon-mdd, main snapshot d97f7c1aa2a0c9c82d1894aa612c9f6ce726eb1c. Read AGENTS.md, package.json, src/lib/research.ts, src/routes/index.tsx, src/components/DraftProposal.tsx and src/data/research.json through GitHub. This confirms code access; synced-branch configuration, a builder freeze and current deployed-version equivalence are still not independently verified.

### Verified from code

- App research.json blob is exactly baseline 3212a9159e69725d56aa74770dbec80ee5fd0082.
- Main table calls rankReviewedOpportunities: filters before sorting; sum is calculated from four fields, rank breaks ties.
- DraftProposal is a separate component reading a separate file, outside the reviewed table.
- Dates render as original strings with an unknown fallback.
- Evidence panel has aria-live and focus handling for observation search selection.
- Earlier QA-01 family counters, QA-02 detailed automation disclosure and QA-03 close/focus-return controls remain absent in this reviewed snapshot. This is static confirmation, not browser retest.

### QA-05 · P1 · appfel — candidate observations enter unlabelled search results

Owner: Person 2. Location: src/routes/index.tsx:50 and the search result renderer.

Reproduction to run in browser: search SG13 (or PG 540). Expected: candidate-only records excluded from selected-job search, or explicitly separated and labelled candidate-only in the result itself. Actual code searches all observations and renders only generic Observation label. Evaluating the exact JSON substring predicate against the pinned dataset returns E10a with candidateOnly=true for SG13. The later evidence panel does label it correctly; that does not label the search hit.

Smallest fix: exclude candidateOnly observations from main search, preserving the dedicated candidate section. Regression: SG13/PG 540 must not surface E10a/E09a as ordinary selected-job hits; skid/handoff must continue to work. The earlier skid test did not exercise this failure because neither candidate matched that query.

### QA-06 · P1 before integration · appfel — review eligibility does not validate support

Owner: Person 2. Locations: src/lib/research.ts:25–35 and 48–52.

The eligibility function checks only opportunity flags/rank and an ineligible text prefix. It does not examine pain-point, observation or source review. Missing status is accepted for every record, not only the known legacy baseline. opportunityChainValid uses some() over paths and checks existence, not full support eligibility; its result only controls a warning, not ranking.

Current baseline and separately rendered O06 draft are not shown to be incorrectly ranked. This becomes an integration blocker if records are merged or promoted. Test: a new ranked record lacking explicit review must be excluded; a reviewed opportunity backed by draft P06/observations/source must be excluded even if another reachable path is reviewed. Preserve the known baseline compatibility, and validate required support before ranking. A mock test of the top-level flag alone cannot prove this gate.

### Execution limits

No Vitest/build/browser test run is claimed. package.json exposes vitest run, but tests were not located or executed in this pass. No app files, test files, research data or Lovable build state were modified. Person 2 owns minimal fixes; exact test-file ownership remains to be agreed before QA adds app tests.
