# LLM Guides Lab: test data

This repository holds the raw data behind the hands-on model tests published by the **LLM Guides Lab** at [llmguides.ai/lab/](https://llmguides.ai/lab/): the exact prompts, every answer exactly as the model gave it, the model versions, prices and every score. How we test and score is explained at [llmguides.ai/methodology/](https://llmguides.ai/methodology/).

The website doesn't compute anything you can't recompute from these files.

## How a test works

1. **Fixed prompts.** Each test has a `test.md` with its prompts and scoring guide, written before the first run. A prompt is never reworded; a changed prompt gets a new number.
2. **Same conditions for every model.** A paid plan (listed per test date in `models.csv`), the model picked by name, and a fresh chat for every prompt. Memory, chat history, custom instructions and connected apps are off. Web search is on. Everything else stays at the app's defaults. All answers are collected within two days.
3. **Answers saved exactly.** Each answer is copied with the app's copy button and saved unchanged, typos included, with the app's share link where the app allows sharing.
4. **Answers published before scoring.** The commit history shows the answers were not changed after scoring.
5. **Blind scoring.** Answers are scored as A, B and C, in a shuffled order, without knowing which model wrote which, against the rubric in `rubric/rubric-v1.md`.
6. **Scores published.** The scores follow, with short notes on what worked and what didn't in each answer. Where a test uses a fact-check, a checklist or an answer key, every check is published in `checks.csv`.

## What's where

```
README.md          this file
CHANGELOG.md       every correction, new test, new model and rubric change
LICENSE            CC BY 4.0 legal code
models.csv         every model ever tested (product, provider, first tested, active or retired)
scorers.csv        who scores, and their qualification
rubric/            the scoring rules (1–5 scale, criteria, special cases, checks)
tests/
  test-NNN-name/
    test.md        the test: criteria, weights, every prompt verbatim, its scoring guide
    YYYY-MM-DD/    one folder per test date (the first day of the run)
      models.csv   exact model versions, plans, run dates
      prices.csv   API prices used for cost (US dollars per million tokens)
      outputs.csv  one row per answer: time, word and token counts, share links
      scores.csv   one row per score (1–5)
      checks.csv   the evidence behind checked scores (only in tests that have them)
      analysis.csv the "what worked / what didn't" notes shown on the page
      notes.md     the test conditions, and anything that went differently
      outputs/     the answers, one file per prompt and model (p01-claude.md)
```

The columns of each file follow a fixed format. Changes to it are recorded in `CHANGELOG.md` and are additive only, so old test dates always stay readable.

Not in this repository: the screenshot of each answer, which is shown on the test page.

## How scores are calculated

- Every answer gets a whole-number score from 1 to 5 on each criterion of its test.
- The **answer score** is the weighted average of its criteria (weights are in `test.md`), shown with one decimal.
- A model's score on a test date is the average of its answer scores.
- A prompt "winner" needs a lead of at least 0.2; otherwise the top spot is shared.
- **Cost** is input tokens × input price + output tokens × output price, summed over all prompts. Token counts cover the prompt and the published answer only, not hidden instructions, web search results or hidden "thinking".
- Some criteria are set by a check instead of a judgement: a checklist, a fact-check or an answer key. Each check is listed in `checks.csv`, and the score follows from it by the rules in rubric §7.

## Limits, stated plainly

- Answers vary from run to run. A test date is a snapshot of how each product behaved on those days, in its app, under the conditions above.
- Blinding removes most bias but not all: some models have recognisable habits.
- Scores are judgements made against a published rubric. The rubric, the answers and the scores are all here so you can disagree with specifics.

## Citing

"According to LLM Guides Lab testing…", with a link to the test page on llmguides.ai. Each test page links to the exact version of these files it was built from.

## Licence

Our files in this repository (README, rubric, test definitions, scores, notes and the other data we wrote) are licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). You may reuse them, including commercially, if you credit LLM Guides with a link to https://llmguides.ai.

Model answers (in the outputs folders) were written by the AI apps we tested and are published as received. To the extent we hold any rights in them, they are also shared under CC BY 4.0.

## Corrections and contact

Found an error? Email contact@llmguides.ai. Every correction is recorded in `CHANGELOG.md`.
