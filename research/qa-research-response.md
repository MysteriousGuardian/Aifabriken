# Person 1 response to QA — import proposal v2

QA report inspected: `qa/data-review.md`, baseline c377396. Findings I2–I5 addressed in `research/research-import-proposal.json`, version 2, commit 49d8df4. Reviewed baseline research.json and all UI files remain untouched.

- **I3:** O02 and O04 explicitly receive `rank: null` when inactivated. Historical IDs and scores may be retained separately.
- **I4:** filter inactive and draft/ineligible opportunities before sorting. Do not sort all records and filter afterward.
- **I5:** O06 now links only to P06, not generic P02. O06 is inactive and unranked while draft; proposed activation/rank are separate fields. Approval of any one reachable path is not enough to count the specific hypothesis as reviewed-supported.
- **I2:** explicit conditional append suggestions map all five new observations to their stages. Reviewed stage lists receive only approved records; drafts appear separately.
- **I6/I7:** new source integration-review status gates eligibility. Rubric and score changes apply together after approval, not piecemeal.

**Important correction to acceptance #20:** four active opportunities is the expected result only after approval and complete eligibility of O06/P06/support. Before approval keep the reviewed baseline ranking and show the proposal in drafts. Do not count O06 in the reviewed ranking merely because it is visible in a draft panel. #22 should check this exclusion, or reviewed status after documented approval; do not expect both active reviewed ranking and all supporting records remaining draft.

Local regression checks passed: inactive ranks null; active suggested ranks unique; O06 has no P02 bypass; conditional stage backlinks cover every proposed observation; draft scores excluded. GitHub content verification follows upload. This checks proposal structure, not app execution.

## External source status

E07 Ruwac and E08 OSHA both returned readable content through Codex web tooling during this pass. This does not prove they work in Strawberry, in the teammate's browser or for direct scripts, nor rule out tool caching. A 403 from that QA script remains a recorded external access issue. Preserve limitations and link accuracy; do not weaken source rules or work around blocks. No Strawberry tool is exposed in this session.

## App access handoff

Project: https://lovable.dev/projects/2ebd52fa-131b-4aba-9934-92d1e2646935

Preview: https://id-preview--2ebd52fa-131b-4aba-9934-92d1e2646935.lovable.app

Lovable metadata verified this project is in Vibeathon and unpublished. Browser preview redirected to Lovable login in this session; no app checklist pass is claimed. GitHub sync/app repository remains unverified here, not proven absent by API metadata. Person 2 must supply the actual linked app repository URL from project Git settings to unblock code review. Existing research repo is not a substitute for that app repo.

No other chat was messaged. Team coordination is through this handoff; appbuilder imports only when idle and after reviewing the exact diff.
