# Changelog

Newest first. Every correction, new test, new model, rubric change and series break is recorded here. Published files are never edited quietly: a correction is a new commit plus an entry below.

Entry types: `data`, `correction`, `new-test`, `new-model`, `new-scorer`, `rubric`, `series-break`, `format`.

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
