# Changelog

Newest first. Every correction, new test, new model, rubric change and series break is recorded here. Published files are never edited quietly: a correction is a new commit plus an entry below.

Entry types: `data`, `correction`, `new-test`, `new-model`, `new-scorer`, `rubric`, `series-break`, `format`.

## 2026-10-17 · test-010 · scores and analysis published
Type: data
Test 010 (Instruction following), date 2026-10-16: 120 scores (24 answers, 5 criteria each), 123 checklist results and the notes on what worked and what didn't in each answer.

## 2026-10-17 · test-008 · raw outputs published
Type: data
Test 008 (Hallucination Rate), date 2026-10-16: 36 raw answers from ChatGPT, Claude and Gemini, published before scoring.

## 2026-10-17 · test-008 · new test
Type: new-test
Test 008 (Hallucination Rate): 12 prompts, six of them about things that do not exist or rest on a false premise. Accuracy is set by a claim log (rubric §7.2) and counts ×2; Honesty (§6.1) is scored 1–5.

## 2026-10-17 · test-008 · criteria and weights before the first run
Type: rubric
Test 008 (Hallucination Rate) is scored on two criteria: Accuracy, counted twice and set by a claim log of up to 5 key claims per answer, each checked against a source or, when nothing can exist to link to, a recorded search (rubric §7.2), and Honesty (§6.1), shown on the test page as "Admits uncertainty". Output score = (2 × Accuracy + Honesty) ÷ 3. Completeness, usefulness, clarity and instruction following are not scored in this test. Rubric §8.1 updated before the test's first run; no published score changes, so the rubric stays version 1.

## 2026-10-17 · format · claim evidence and display names
Type: format
Data format v1.5: test.md may have a "Labels:" line that gives a criterion a display name on the website (the data files keep the criterion name). In checks.csv, a claim's evidence is a source link, with a phrase from the page in note, or, when there is nothing to link to (for example something that does not exist), a note starting "Searched:" that says what was searched and where.

## 2026-10-16 · test-010 · raw outputs published
Type: data
Test 010 (Instruction following), date 2026-10-16: 24 raw answers from ChatGPT, Claude and Gemini, published before scoring.

## 2026-10-16 · test-010 · new test
Type: new-test
Test 010 (Instruction following): 8 prompts. Instruction following is set by a checklist per prompt (rubric §7.1; a missed critical item caps it at 2) and counts ×2; Accuracy, Completeness, Usefulness and Clarity are scored 1–5.

## 2026-10-09 · format · test date files
Type: format
outputs.csv: share_url and archive_url may be empty when the app could not create a share link; notes.md says why. analysis.csv: an answer may have no "worked" note when it is a refusal scored 1 on every criterion, and no "didn't" note when every score is 5.

## 2026-10-09 · test-001 · scores and analysis published
Type: data
Test 001 (Writing), date 2026-10-08: 120 scores (24 answers, 5 criteria each) and the notes on what worked and what didn't in each answer.

## 2026-10-09 · test-001 · answer_words
Type: correction
Correction: answer_words for two answers (p03 and p06, Claude) now excludes notes around the requested content. No score changed.

## 2026-10-09 · repository · README
Type: correction
Correction: README wording on how answers were copied, widened to cover text selected and copied.

## 2026-10-08 · test-001 · raw outputs published
Type: data
Test 001 (Writing), date 2026-10-08: 24 raw answers from ChatGPT, Claude and Gemini, published before scoring.

## 2026-10-08 · repository · README
Type: correction
README: answers come with the app's share link where the app allows sharing; archived copies are no longer listed.

## 2026-10-07 · repository · initial structure
Type: format
Repository created. Scoring rubric v1. Licence: CC BY 4.0. Models: ChatGPT, Claude, Gemini. Scorer: stojan.
