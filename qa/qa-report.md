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


## Codex executed tests and local browser — 2026-10-14, approximately 12:40–12:45 Stockholm

Pinned local clone: hackathon-mdd d97f7c1aa2a0c9c82d1894aa612c9f6ce726eb1c. Production/source files untouched. This tests a local copy, not the deployed Lovable preview.

### Executed

- npm test: PASS, 2 files / 10 tests, Vitest 4.1.11, 12:42:18 Stockholm.
- npm run build: PASS, client, SSR and Cloudflare-module output. No deployment.
- Dependency caveat: installed with npm install --ignore-scripts --package-lock=false because Bun was unavailable. Repository has bun.lock; this was NOT a frozen Bun-lockfile reproduction. Lockfile and tracked source were not edited.
- Additional direct executions of the actual research.ts module (Node TypeScript erasure; JSON import substituted with the identical file content): PASS baseline order, explicit inactive/draft exclusion, score ties, actual draft O06 exclusion and directObs candidate exclusion.
- QA-06 reproduced: a new ranked record with missing review status is accepted; an O06 copy with top-level gates removed/promoted is accepted while P06 remains draft. This is a negative test of the import gate, not a claim that current baseline is contaminated.
- Existing O06 test only retains active:false/reviewStatus:draft while changing links/rank. It therefore does not prove supporting-record eligibility.

### Local in-app-browser observations at http://127.0.0.1:4173/

| Check | Result / precise scope |
|---|---|
| Initial load | PASS: app renders, PLAN selected |
| All five stages | PASS: clicked PLAN/PREPARE/MOVE/OPERATE/FINISH; corresponding tasks, equipment, dependencies and gaps render |
| PLAN → P01 → E03a | PASS: A/B/C panels and E03a locator, year 2014, actor/task and limitations visible |
| E03 source link | Correct href visible in browser accessibility tree; external destination NOT opened in this local pass |
| P01 → O01 | PASS: clicked hypothesis link; URL becomes /#O01 |
| Baseline comparison | PASS observed order O01/O02/O03/O05/O04, sums 11/10/10/8/8 |
| SG13 candidate search | FAIL QA-05: E10a appears as generic Observation without candidate label in search hit |
| Escape closes panel | FAIL QA-03: Escape leaves selected E03a and P01 panels unchanged |
| No-result query xyzzy | PASS: explanatory empty result; app remains available |
| Reset from FINISH with query | PASS: query cleared, PLAN selected and empty detail restored |
| Deployed preview, reload, full keyboard sequence, exact viewports/zoom, source access and timed demo | NOT TESTED in this pass |

No browser measurements at prescribed viewport/zoom sizes are claimed. No production changes, new app test files, build requests or deploys were made.

### Immediate handoff to Person 2

Fix QA-05 candidate search first. Before approving any merged import, fix QA-06 support eligibility and legacy-baseline scoping. Then resolve QA-01 family counters, QA-02 complete automation disclosure and QA-03 close/focus return. Reuse working ranking and baseline behavior. Request QA rerun on the exact new commit; do not interpret 10 passing tests as coverage of the negative cases above.


## Strawberry independent source/data pass — 2026-10-14, 12:44–12:46 Stockholm

Research repo: MysteriousGuardian/Aifabriken, main. App snapshot independently read: MysteriousGuardian/hackathon-mdd at d97f7c1aa2a0c9c82d1894aa612c9f6ce726eb1c. Synced branch, deployment equivalence, approved data changes and builder freeze are still NOT VERIFIED. No new browser acceptance pass or live demo rehearsal is claimed in this round. The earlier Strawberry run and Codex additions above remain intact and attributed.

Read current data-review, revised acceptance checklist, baseline, proposal v2, QA response and research decision/demo script. Baseline blob remains 3212a9159e69725d56aa74770dbec80ee5fd0082; proposal blob dd023d56c004674cf9640db715b2cb0c5afa2cb1. These are baseline plus separate draft, not documented approved integration.

### Executed checks (this tester, not inherited claims)

JSON parsed locally; assertions evaluated. The inspected pure research.ts module was type-stripped and executed with identical baseline JSON replacing its import. No app code/data was modified and no Vitest/build/deploy is claimed. Synthetic fixtures existed only in local evaluation.

| Check | Result | Detail |
|---|---|---|
| Baseline unique IDs | PASS | 38 records |
| References/backlinks and candidate exclusion | PASS | [] |
| Score inputs 1–3 | PASS | [["O01",11],["O02",10],["O03",10],["O05",8],["O04",8]] |
| P04 family count | PASS | {"observations":2,"families":1} |
| P05 family count | PASS | {"observations":2,"families":1} |
| Draft O06 inactive/unranked/P06 only | PASS | ["P06"] |
| Inactive proposal ranks null | PASS | O02/O04 |
| Proposed observation backlinks complete | PASS | Conditional append suggestions, not applied |
| Actual module baseline ranking | PASS | Pinned d97f7c1 module |
| Actual module excludes inactive/draft before sorting | PASS | Synthetic negative fixtures, no app data changed |
| QA-06 new record missing review rejected | FAIL | Expected false; actual true |
| QA-06 promoted O06 with draft support rejected | FAIL | Expected false while P06/support draft; actual true |
| SG13 candidate excluded from main search predicate | FAIL | Actual matching IDs: E10a |

### Priority handoff and exact retest

- **QA-05, P1, app defect, Person 2:** pinned index.tsx searches all observations and labels hits generically. SG13 predicate returns E10a candidateOnly=true. Expected: exclude candidates from selected-job results or explicitly separate/label candidate hits. Minimum correction: filter candidate-only records out of main search, preserving dedicated candidate view. Exact retest on declared replacement commit: SG13 and PG 540 must not yield ordinary E10a/E09a hits; skid still yields E01b/E02a/E04a/O02/O04; handoff yields P01/O01; xyzzy and Reset still work. **New deployed browser reproduction NOT TESTED**; static predicate reproduced independently.
- **QA-06, P1 before import, app defect, Person 2:** actual isReviewedEligible accepts NEW_UNREVIEWED with rank and missing status; it also accepts O06 after top-level flags are changed while P06/required support remains draft. Expected: missing-status compatibility only for the known reviewed baseline; imported records require explicit review and every mandatory pain/observation/source support gate. Minimum correction: validate full eligibility before ranking, not a some-path existence warning. Exact retest: missing-status new record excluded; promoted O06 plus any required draft pain/observation/source excluded; a reviewed alternate P02 path cannot bypass P06; fully eligible approved O06 admitted; explicit inactive high-score record excluded before sorting; legacy baseline order unchanged. Current separate O06 draft is correctly excluded; this is an integration gate, not proof of contaminated baseline.
- **QA-01/QA-02/QA-03:** family counters, detailed automation disclosure and close/focus return remain absent in inspected snapshot. Prior browser defects are NOT RETESTED on any replacement version. Person 2 fixes; QA independently verifies the new declared commit. Prior exact reproduction/minimal corrections above still apply. QA-04 remains low-priority copy mismatch.

### Demo script preflight (static, not timed live rehearsal)

Person 1's research-decision-update.md includes a three-minute script. In baseline mode its 1:00–1:40 troubleshooting segment must use manual/research fallback because proposed E01e is not reviewed app support. The 2:10–2:40 O06 segment must explicitly show a draft proposal/report, not an active reviewed opportunity. Five baseline opportunities and 11/10/10/8/8 remain correct before approval; do not narrate four active 9/9/9/8 as current app state. Script correctly avoids validated-benefit/automatic-discovery claims. External-source fallback: show inspected app paraphrase, locator and limitation if source page blocks; do not bypass blocks or imply fresh verification.

**Live three-minute rehearsal: NOT TESTED** pending confirmed preview/commit and paused editing window. Full keyboard, required viewport/zoom matrix, every active opportunity browser chain and new E07/E08 access remain NOT TESTED in this round.

### Coordination and recommendation

No approved team messaging channel is available; no Person 2 message sent. One forwardable request supplied in chat: confirm apprepo URL, synced branch, review commit, preview, approved data changes and ready-for-QA paused-edit window. No test-file ownership/path agreement exists; no app test file, branch or PR created. No production/research/UI changes, Lovable build/deploy/project/connection action performed.

**Recommendation:** approved import is BLOCKED by QA-06 until fixed and independently retested. Final demo readiness is not certified: frozen deployed-version match and live rehearsal are missing. Baseline remains a possible demo path with stated limitations, not a new acceptance PASS. At 12:44 Stockholm there were about 3h16 to deadline; prioritize candidate search, import eligibility and evidence/demo chain above cosmetics. Proposed freeze remains 15:15; no routine/reminder scheduled.


## Codex local retest — 2026-10-14 12:52–12:55 Stockholm

Local pinned snapshot: 8008474 (full SHA recorded by local git), fetched from origin/main. Changes since d97f7c1 affect only src/routes/index.tsx: candidate exclusion, selected-panel reset and focus targeting. No app changes by QA.

- npm test: PASS 2 files / 10 tests, 12:52:40. Prior dependency-install caveat applies.
- QA-05 CLOSED for this local version: search SG13 shows no results. Code excludes candidateOnly before building search hits. Dedicated candidate section remains.
- Search handoff: P01/O01 visible. Clicking P01 focuses the observed-evidence DIV; clicking O01 focuses element id O01. Verified in rendered DOM.
- QA-06 remains open before merged import: research.ts and support-eligibility behavior are unchanged. Separate draft continues to protect the present baseline.
- QA-01/02/03 remain open: source changes do not add counters, disclosure detail or close controls.
- Viewport override 1366×768: DOM dimensions match and document scrollWidth 1366; scale 1 reported. Screenshot inspected.
- Viewport override 1280×800: DOM dimensions match, document scrollWidth 1280, Reset right edge 1256. Screenshot inspected.
- 390×844: document scrollWidth 390, no document-wide horizontal overflow. PREPARE and OPERATE button scrollWidth 71 > clientWidth 63; text exceeds allocated button width. Treat as narrow-screen P2 follow-up, not proof that laptop layout fails.
- Viewport override reset after test. Browser 125% zoom and every focusable control remain NOT TESTED. scale 1 is not independent proof of browser zoom percentage.
- Local screenshot timing/rendering may differ from deployed preview; no claim of deployed equivalence or freeze.

### Demo script compatibility review

Reviewed Person 1's three-minute script in research/research-decision-update.md. The script already offers an external research/PDF fallback when import is unavailable. Retain baseline five-opportunity scores in the app; do not narrate four active items or 9/9/9/8 as implemented.

At 1:00–1:40 E01e exists in the separate draft, not a reviewed OPERATE observation. Say that manual troubleshooting exists and use the actual manual locator if showing the source. At 2:10–2:40 the draft O06 display has no complete validation experiment or alternatives UI. Use Person 1's research handoff for that explanation, or choose baseline O01 and its visible validation experiment for an entirely in-app demo. Existing support is not proof of usability, unmet demand or unique diagnosis.

Live spoken three-minute rehearsal is still NOT TESTED; this is a compatibility review and local click/focus retest. Person 1 owns manuscript changes; QA has not edited research files. Prioritize remaining P1 import gate, then P2 counters/disclosure/close controls; preserve working search and baseline.


## Codex gate verification — 2026-10-14 12:54–12:56 Stockholm

App snapshot 8158fec0dcfe5674689dba88a92c7d4e8afab7ed. GitHub origin/main and Lovable latest_commit_sha both reported this SHA at inspection; this is metadata agreement, not deployed-browser verification.

**QA-06 CLOSED for this snapshot's actual reviewed-table path.** The UI now calls rankEligibleOpportunities, which validates every linked pain point, observation and source before applying the existing rank sort. Baseline fallback is scoped by known IDs. The older rankReviewedOpportunities helper remains permissive; app integration must continue using the full gate.

Eight executed direct-module assertions passed:
1. Baseline order O01/O02/O03/O05/O04.
2. Draft P06 rejected even with additional P02 path.
3. Reviewed P06 with draft observations rejected.
4. Reviewed observations with draft new sources rejected.
5. Fully reviewed support admitted.
6. New opportunity with missing review status rejected.
7. Missing observation rejected.
8. Candidate observation rejected.

These scenarios modified only in-memory copies in a separate Node process, not files or actual research statuses. Existing npm test: 10/10 PASS at 12:55:07. npm run build: PASS. git status clean afterward. Dependency-install caveat from earlier applies.

### Current minimum fix list for Person 2

No open P0 or reproduced P1 remains in the exercised baseline paths. QA-05 candidate search and QA-06 support gate are closed at their tested snapshots; keep them in the next regression pass.

Remaining implementation acceptance:
- QA-01: show eligible observation count and deduplicated family count; P04/P05 must show 2 observations / 1 family.
- QA-02: visibly explain automated loading/search/traversal/arithmetic versus curated selection/extraction/interpretation/inputs; discovery is not implemented.
- QA-03: labelled panel close and Escape handling with focus return to opener.
- Narrow-screen P2: avoid PREPARE/OPERATE text exceeding the 390px navigation cells.
- QA-04 exact header wording is cosmetic; resolve criterion or copy consistently.

Do these in one focused UI pass, preserve baseline/draft status and the working full gate. Return exact app commit and accessible preview for retest. QA does not own production fixes.

Still pending: deployed browser accessibility, 125% zoom, full keyboard-only sequence and live spoken three-minute rehearsal. Do not equate a successful build with those checks.


## Codex trace and keyboard retest — 2026-10-14 12:57–13:00 Stockholm

Pinned app snapshot 1b11f9c0ee03d6834a53344af384272944261f67. Source diff adds clickable opportunity-to-observation traces and missing-reference display; full eligibility gate remains in use. npm test PASS 10/10 at 12:57:21.

Local browser:
- Table now visibly shows opportunity → pain-point ID → observation buttons → source IDs.
- Enter on O01 table trace E03a opens correct E03a details and focuses ASIDE labelled Evidence panel.
- Tab from that panel focuses the source anchor with exact URMCA URL.
- Escape leaves E03a details open: QA-03 still open.
- Fresh reload renders PLAN again; first Tab focuses search.
- No full keyboard-only tour, external PDF activation, 125% zoom or live spoken rehearsal claimed.

Current tested baseline has no observed P0/P1 blocker in the exercised paths. Remaining P2 implementation acceptance: source-family counts, automated/curated disclosure, close/focus-return, narrow navigation cells. Person 2 owns these fixes. Ready-to-send acceptance packet is qa/builder-fix-handoff.md. No production files changed by QA.


## Codex counters and close retest — 2026-10-14 13:04–13:07 Stockholm

App snapshot acd6ab0658e36ebf3e3f5dbf0e3d26b7d30cb464. npm test PASS 10/10 at 13:04:32. Source introduces evidenceCounts and panel close/status handling.

Local browser verified:
- Enter on O01 trace E03a → evidence opens; Escape closes → focus returns to E03a opener.
- Space opens P04; Close activated with Return closes pain → focus returns to P04.
- P04 and P05 display Reviewed observations: 2 / Source families: 1.
- Status message updates for opened/closed panels.

QA-03 is closed for these exercised paths; search opener/removal fallback and every control remain untested. QA-01 baseline display requirement passes. QA-02 disclosure detail and narrow navigation remain unchanged/open.

### QA-07 · P1 before mixed-status import · appfel — counters ignore source review eligibility

Owner Person 2. evidenceCounts filters observation.reviewStatus and candidateOnly, but ignores source integrationReviewStatus and even counts a missing source as its own family. In an isolated in-memory execution, setting E01/E04 source integration status to draft leaves P04 count at 2/1 while isPainPointSupportEligible(P04) returns false. Files and actual data were untouched.

Expected: reviewed support counters require an existing review-eligible source; missing/draft/ineligible sources must not inflate counts. Apply the same source-review semantics as the full gate, deduplicate observation IDs before counting, preserve valid baseline family grouping. This does not corrupt current baseline, but must be fixed before mixed-status import. Add regressions for draft source, missing source and duplicate observation reference.

QA demo runbook added as qa/demo-runbook.md: version-aware click sequence and presentation copy for baseline. It is a rehearsal aid, not a claim of live spoken three-minute timing. Person 1 owns the research narrative; team should reconcile this QA runbook with their script.
