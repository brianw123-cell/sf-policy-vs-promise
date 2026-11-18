# Submission

Pencils down at 8:30. Before then:

1. **Push your repo** with this file filled in. No API keys, no private data.
2. **Fill in your team card**: team name, statement number, first names, and the six short answers below.
3. **Hand the card to a judge.** Judges pick six finalists from the cards.
4. **Be ready to demo.** Three minutes, no extra prep time: the concern, the thing working on real data, one honest limit.

## Team card

**Team name:** WatchTheFlock

**Statement number** (the card your corner wrote): [FILL IN CORNER CARD #]

**First names:** Manvi, [ADD TEAMMATES' FIRST NAMES]

**Statement:** How might we help **SF residents, commuters, and oversight auditors** do **a side-by-side audit of what surveillance tech covers the Bay Area and where official SF policies leave data-sharing limits vague** so that **hidden multi-agency sharing gaps are caught before deployment**? Build idea: **A + B (What's watching the Bay? + Policy versus promise)**. We'll know it worked if **anyone can cross-check a Bay Area commute and 7 real SF surveillance policies against verbatim source quotes in under 30 seconds**.

## Six short answers

**1. The concern:** SF residents and commuters crossing Bay Area jurisdictions (driving or on transit) are captured by ALPRs, cameras, and drones governed by unread PDF policies—a neighbor would recognize reading that SFPD ALPR data leaked to out-of-state agencies via regional hubs despite local sanctuary/SB 34 rules.

**2. What we built,** and the one command that runs it: **WatchTheFlock** — a 3-panel web app combining a Jurisdiction-Level `A → B` Commute & Surveillance Density Heatmap, an SF Policy-vs-Promise Matrix with a Verbatim Source Quote Drawer, and a 4-Tier Data-Flow Lineage Graph + 1-click Sunshine Request drafter. Run with: `cd manvi && PORT=3005 npm run dev`

**3. Data we used:** dataset ids from `datasets.json`, how many rows, date range: `eff-atlas-of-surveillance` (**297** Bay Area rows across 9 counties out of 15,135 US rows, 2012–2026) and `sf-surveillance-inventory` (**7** SF department policy & biannual inventory `.txt` files: SFPD ALPR & Amendment, SFMTA, SFO Airport, Public Works, Rec & Park, and Sept 2026 inventory; 2020–2026).

**4. What it found:** one measured result, with sample size: Across **7** SF surveillance policy/inventory files, **6 of 7** contain vague or open-ended outside-agency sharing language (e.g., referencing regional hubs/authorized requests without hard downstream query caps); across **297** Bay Area Atlas deployments, only **9.1% (27/297)** have source citations from the last 2 years.

**5. One honest limitation:** what it cannot tell you, what breaks: Automated text extraction can miss nuances in scanned tables, footnotes, or later Board of Supervisors amendments—and Atlas data is at the agency/city level, so it cannot tell you exact street-corner camera locations or real-time query counts. Every extracted claim must be spot-checked in the inline Verbatim Quote Drawer.

**6. If this were deployed and it failed,** who is accountable, and how would they find out? The **SF COIT (Committee on Information Technology) Privacy Officer / Department Surveillance Liaison** is accountable before any audit report is published; extraction errors are surfaced immediately via the inline Verbatim Quote Drawer (which shows the exact source text next to every cell) and public Sunshine/CPRA feedback.

## How judges score

Each card is scored 1 to 3 on the first three.

1. **Real concern.** It came from the room, with a specific who and a failure a neighbor would recognize.
2. **Works on real data.** Something runs on real data, and you can show what it found.
3. **Honest.** It names a limitation and says who is accountable if it fails.
4. **Tiebreak.** Would someone outside this room use it?
