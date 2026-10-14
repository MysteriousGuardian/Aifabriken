# Person 2 — remaining QA fixes

Last QA snapshot: app 1b11f9c0ee03d6834a53344af384272944261f67. Read the current app before editing; preserve newer work.

Ready-to-send prompt:

Make one focused UI correction pass in Customer Job Twin. Keep the reviewed baseline, separate draft proposal, candidate exclusion, full support gate and opportunity evidence traces working.

1. In each pain-point evidence panel show separately: eligible reviewed observation count and unique source-family count. P04 and P05 must show 2 observations / 1 family. Use the dataset familyId; exclude candidate/draft/ineligible support. Do not call counts prevalence.
2. Add visible concise disclosure: loading, search, relationship traversal and score arithmetic are automatic; source selection, extraction, interpretation, hypotheses and score inputs are curated. Automatic discovery is not implemented.
3. Add labelled close controls for pain/evidence detail and Escape handling. Return focus to the actual opener; do not leave focus on a removed node. If closing evidence while pain remains, preserve pain context. Test open → Tab → close → focus return, including search and table-trace openers.
4. At 390px prevent PREPARE/OPERATE text spilling outside their step buttons. Keep the five-stage order and all labels available.
5. Treat the literal header-copy difference as P3: preserve meaningful job identification; document intentional acceptance-copy changes.

Acceptance: fresh load/reload, five stages, PLAN/P01/E03a/source/O01, SG13 excluded from selected-job search, skid/handoff search, Reset, baseline 11/10/10/8/8, O06 draft excluded, full review gate, P04/P05 counts, disclosure, keyboard close/focus and laptop/narrow layout all checked.

Do not activate new research or change evidence scores in this UI pass. Use existing components and make the smallest fixes. Send exact commit, preview, checks actually run and remaining gaps to QA. Pause changes during the agreed deployed-preview retest.

QA owns documentation. Person 2 owns production edits. No request from this document has been sent to Lovable by QA.
