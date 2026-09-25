# Intro to Topic Structures and Wildcards

- **Course:** Solace Essentials
- **Syllabus order:** 03
**Academy status:** Completed on 2026-09-24

## Step 1 of 4 — objectives

The lesson aims to explain topic structures in more detail and introduce wildcard options available to consumer applications.

## Step 2 of 4 — Solace topic structure

Topics are UTF-8 strings used for dynamic message routing and filtering. Their hierarchy resembles a file path, with segments separated by `/`; the structure can be shallow or deep. The diagram identifies levels 1–4 and the forward-slash delimiter, which separates topic segments.

A topic can be at most 250 bytes. Topic length has little effect on broker routing efficiency, though it can affect network efficiency. Example: `region/northAmerica/usa/sales` can target subscribers interested in US sales within North America.

Topics are matched dynamically at runtime rather than pre-created. Publishers can send to a topic, and consumers can subscribe with wildcards for flexible matching.

## Step 3 of 4 — Solace wildcards

Wildcards let consumers subscribe to groups of topics without listing each topic. `*` matches one topic level; `>` matches one or more following levels. For example, `sports/tennis/*` can match `sports/tennis/player1` and `sports/tennis/player2`, but not `sports/football/player1`. `sports/>` can match topics under `sports/`, including tennis and football topics.

A wildcard in a published topic is treated as a literal character, so the lesson recommends using wildcards in consumer subscriptions rather than producer publications.

## Step 4 of 4 — topic matching quiz

Both multiple-response questions were eventually answered correctly after retries using the system feedback.

**Question 1:** The producer publishes to `system/status/host1/statistics`. Which subscriptions match? Select all that apply.

- `*/host1/statistics`
- `system/Status/>`
- `*/status/host1/>` — correct
- `sys*/status/*/statistics` — correct

System feedback: `*` matches one topic level, so the first pattern cannot cover both `system` and `status`. Topic matching is case sensitive, so `Status` does not match `status`.

**Question 2:** The producer publishes to `addr/req/jon/billing/get`. Which subscriptions match? Select all that apply.

- `addr/req/*/billing/*` — correct
- `addr/req/j*/*/get/>`
- `addr/req/j*/>` — correct
- `addr/req/jon/*`

System feedback: `>` matches one or more following levels, so the second pattern would require a level after `get`. `*` cannot span the `billing` and `get` levels.
## Key visual asset recovery

The archived lesson describes a topic hierarchy diagram showing levels 1-4 and the forward-slash delimiter. That course visual could not be recovered from the completed Academy page.

No local course image was available to link from this lesson. The course page currently confirms completion, and reopening completed SCORM content exposes a retake action rather than its lesson screens. The lesson image folder is ready for source assets; no substitute images were fabricated.
