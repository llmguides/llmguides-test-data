# LLM Guides Lab scoring rubric, version 1

This rubric says how every output in an LLM Guides Lab quality test is scored. The same rules apply to every model, every test and every test date. Scoring is **blind**: the scorer sees outputs as A, B and C and doesn't know which model wrote which.

**How this file is organised**

| Part | What it covers | Changes when… |
|---|---|---|
| **A. Rules for every test** (§1–4) | The scale, the special cases, consistency | Almost never |
| **B. The criteria** (§5–6) | The five core criteria, plus extra criteria that some tests add | A test needs a new extra criterion |
| **C. Checked criteria** (§7) | Criteria set by a checklist, a fact-check or an answer key instead of judgement | Almost never |
| **D. Test settings** (§8–9) | Each test's criteria, weights and checks, and how to add a new test | Every new test (adding one is not a rubric change) |

---

# Part A. Rules for every test

## 1. The scale

- An **output** is the single thing being scored: normally one answer to one prompt. In multi-turn tests it is a whole conversation (§9).
- Every output gets a score from **1 to 5** on each criterion of its test. **Whole numbers only.**
- The **output score** is the weighted average of its criteria (weights in §8), shown with one decimal.
- A model's score on a test date is the average of its output scores over all prompts. If a test runs each prompt more than once, the runs are averaged first.
- The five numbers mean the same thing on every criterion:

| Score | Meaning |
|---|---|
| **5** | Excellent. Nothing a demanding reader would change |
| **4** | Good. Does the job, with small issues |
| **3** | Acceptable. Usable, but with clear weaknesses |
| **2** | Weak. Big problems; needs serious work to be usable |
| **1** | Fails. Unusable, wrong or missing |

- **Score against the brief, not against the other outputs.** Two outputs can both get a 5, and all three can get a 2.
- **Core criteria are never "not applicable".** They are always scored (§5 says how when a criterion seems not to fit).

## 2. What is scored

- **Only the final answer.** Visible "thinking" or reasoning panels are not scored, and neither is anything the app shows around the answer (buttons, suggestions, the model name).
- **The answer as saved**, shown when scoring in one identical style for every model, so formatting shows as the reader would see it but no app styling gives the model away.
- **If the app offers two answers to choose from**, the first one shown is used, and this is noted.
- **Images, files or code the model produces** are scored from the saved copy (screenshot, file or text), shown the same way for every model.

## 3. Special cases

### 3.1 Refusals and non-answers

"Refusal" means the model says it can't or won't do the task ("I can't help with that"), or answers with something else instead.

| Situation | How it's scored |
|---|---|
| Refuses a reasonable request, or doesn't attempt it | **1 on every criterion.** The reason is written in the notes and shown on the page |
| Only asks a question back ("Who is the audience?") without doing the task | Scored like a refusal, because every prompt is written to be complete. Noted as "asked a question instead of answering" |
| Asks a question **and** does the task | The task is scored normally; the question is neutral |
| Does only part of the task | What's there is scored; Completeness no higher than 2 |
| Declines when declining is the right answer (the prompt is marked "expected: decline" in the test settings, e.g. a request to make up a source) | Not a refusal; this is the correct behaviour. Scored normally, usually high |
| Says it can't find or doesn't know something that really doesn't exist | Not a refusal; this is the correct answer |
| The product doesn't have the feature at all (e.g. no image input) | **Not scored.** Shown as "Not supported" and left out of that test's averages (not counted as a 1) |
| Output cut off or broken by a glitch | Retry once in a new chat. If the retry fails too, what exists is scored and noted |

### 3.2 Length

- **What counts: the requested content** (the deliverable), not the text around it. Not counted:
  - a lead-in before it that talks to the user about the answer ("Here's an opening for your story:");
  - notes and labels about it ("(~100 words)", "Note: I kept the tone formal");
  - closing offers or questions after it ("Want a shorter version?").

  Everything inside the requested content counts, including its own heading and any aside within it.
- **Exception:** when the prompt asks for the content only ("output only the email", "no other text"), any text around it is a missed instruction under Instruction following.
- **Text around the content still matters:** it's something the reader has to delete, so it counts under Usefulness (a small edit) or Clarity (padding). Never under Instruction following as well; one problem, one criterion (§3.4).
- Words are counted by the `count-words` tool, the same way for every output: every whitespace-separated word, headings included; numbers and hyphenated words count as one. The tool reports both the whole output (`words`) and the requested content (`answer_words`); the length rules below use `answer_words`. The boundary is shown when scoring and can be corrected by the scorer. For languages written without spaces, the test settings give the length in characters.
- **A range is given** ("100–150 words"): anything inside the range is fine.
- **A target is given** ("a 100-word summary"): **±10%** is allowed. **"Under" or "at most"** is a hard maximum.
- **"Exactly"**: exact, with no allowance.
- Missing the length counts against Instruction following:

| How far off | Instruction following |
|---|---|
| Within the allowance | No effect |
| Outside, but by no more than 25% | No higher than 4 |
| 25–50% off | No higher than 3 |
| More than 50% off | No higher than 2 |

- In a test where Instruction following is set by a checklist (§7.1), length is one item on the checklist instead.

### 3.3 Invented facts

- An **invented fact** is a specific claim presented as real that is false or can't be traced: a made-up statistic, quote, study, person, product feature, date, URL or source.
- **Any invented fact caps Accuracy at 2.** If the output's main point relies on it, Accuracy is 1.
- These are not invented facts: clearly labelled examples or hypotheticals, and made-up content **the prompt asks for** ("use realistic data", fiction).
- **Cited sources** (web search is on in every test): check up to **five** cited sources per output, starting with the ones the main claims rest on. A source that doesn't exist or doesn't support its claim counts as an invented fact. A real but weak source is a Usefulness issue, not an Accuracy one.

### 3.4 One problem, one criterion

Each problem lowers the one criterion it belongs to. A wrong fact lowers Accuracy, not Clarity as well. The caps in this section are the only planned knock-on effects. This keeps scores predictable and stops one mistake from being counted three times.

### 3.5 Never scored

- **Which model it is.** If an output reveals its model ("As Claude…"), it is ignored.
- **Personal taste in style**, when the brief doesn't set one.
- **Length for its own sake.** Longer outputs get no credit for effort; padding costs Clarity.
- **Speed and price.** These are measured separately.

### 3.6 A flawed prompt

If a prompt turns out to be ambiguous (e.g. models reasonably read it in different ways), every reasonable reading is accepted, and this is noted. The prompt is never reworded: the next test date gets a new, clearer prompt with a new number.

## 4. Scoring consistently

1. **Read all the outputs for a prompt before scoring any of them**, then score one criterion at a time across A, B and C.
2. **Every 1 and every 5 needs a one-line reason** (asked for when scoring). These notes become "What worked / What didn't".
3. **When torn between two numbers**, reread both anchors and pick the one whose description fits better; note why.
4. **Take a break every 8 prompts.** Tired scorers drift.
5. **Before finishing**, go back over every 1 and 5. Once scoring is finished, the scores are final.
6. **Reread this rubric at the start of every scoring session.**
7. **Consistency check, from the second test date on.** As part of scoring a new test date, **3 outputs from the previous date** are scored again, blind and mixed in with the new outputs, without showing which they are. Any criterion score that differs by 2 or more from its earlier score is reviewed before the new scores are approved. The check scores are private and change no published score; they keep scores comparable over time, which matters because results build up over years.
8. **More than one scorer** (an expert or a co-scorer): each scores alone and blind; their scores are averaged. Any criterion where two scorers are 2 or more apart is noted on the page as "scorers disagreed".
9. **Scorers must be qualified for the test.** Where the settings say so (e.g. translation), scoring is done by a qualified expert, not by the Lab alone.

---

# Part B. The criteria

## 5. The five core criteria (used in every test unless the settings replace them)

Examples use the Writing test's executive-summary prompt: *"Summarize the following quarterly data into a 100-word executive summary for a board presentation… Highlight both the good and the concerning."* (Revenue $4.2M, up 12%; costs up 18%; churn 4.2%, up from 3.1%; NPS 72, down from 78; Acme contract $800K ARR; two senior engineers resigned.)

### 5.1 Accuracy (`accuracy`): is what it says true?

Facts about the world; **facts given in the prompt** (copied correctly, never contradicted); numbers, calculations and logic; code that does what it claims; cited sources. For fiction or other writing with no factual claims, Accuracy covers internal consistency and the correct use of the prompt's details.

| Score | Anchor | Example |
|---|---|---|
| 5 | Everything is correct; any claim that can be checked holds up | All figures right; "costs are growing faster than revenue" is correctly drawn from the data |
| 4 | Correct overall; one small slip that doesn't mislead | "Revenue up over 10%" instead of 12% |
| 3 | A few small errors, or one error a careful reader would notice | Rounds churn to "about 3%", which hides the increase |
| 2 | One clear error that changes the meaning, **or any invented fact** (§3.3) | Says NPS rose; or adds "margin improved to 26%", which isn't in the data |
| 1 | Several clear errors, or the main point is wrong | Reports the quarter as all good news |

**Right answer, wrong reasoning** (where reasoning is shown): no higher than 3. A lucky answer isn't an accurate one.

### 5.2 Completeness (`completeness`): is everything the task needs there?

Every part the prompt asks for, and anything the reader would obviously expect even if it isn't spelled out.

| Score | Anchor | Example |
|---|---|---|
| 5 | Every part of the task covered, including what matters most that wasn't spelled out | Good and concerning both covered; the main risk (costs outpacing revenue, rising churn) is named |
| 4 | Everything asked for is there; one minor point missing or thin | Skips the headcount growth |
| 3 | The main part is done, but one requested element is thin or missing | Mostly good news; the concerns get half a sentence |
| 2 | Several requested elements missing | No churn, NPS or resignations |
| 1 | Most of the task not done | Revenue only |

### 5.3 Usefulness (`usefulness`): could the reader use it as it is?

Score it from the point of view of the person who asked: how much work is left before they can use it?

| Score | Anchor | Example |
|---|---|---|
| 5 | Ready to use as it is | Could go straight on the slide |
| 4 | Usable after small edits (a word, a sentence) | Opens with a generic line to cut |
| 3 | Usable, but needs real editing (reordering, rewriting parts) | Correct, but a list of numbers with no "so what" |
| 2 | Only parts usable; most would be rewritten | Wrong tone for a board; reads like a marketing post |
| 1 | Nothing usable | Off-topic, a refusal, or only generic advice |

### 5.4 Clarity (`clarity`): is it easy to read and follow?

Structure, flow, wording, and length relative to the content.

| Score | Anchor | Example |
|---|---|---|
| 5 | Crisp and well organised; every sentence earns its place | Good news, concerns, one-line outlook |
| 4 | Clear, with small rough spots | One sentence stacks three figures |
| 3 | Understandable, but wordy, repetitive or oddly ordered | Concerns buried in the middle |
| 2 | Hard to follow; the reader has to work to get the point | Jumps between figures with no order |
| 1 | Confusing or incoherent | Contradicts itself |

### 5.5 Instruction following (`instruction_following`): did it do what it was told?

Every explicit instruction (length, format, audience, tone, what to include or leave out) and the plain intent behind them.

| Score | Anchor | Example |
|---|---|---|
| 5 | Every instruction met, including tone and audience | ~100 words, board tone, good and concerning both highlighted |
| 4 | All the important instructions met; one minor slip | 115 words (outside the ±10% allowance, within 25%) |
| 3 | One clear instruction missed | 140 words; or bullet points where a summary paragraph was asked for |
| 2 | Several instructions missed | Too long, wrong audience, concerns missing |
| 1 | Instructions largely ignored | A 400-word report in casual tone |

**Doing more than asked is not a bonus.** Extras that don't conflict with the instructions are neutral; extras that break them (going over the length, adding a preamble after "output only…") are misses. Text around the requested content is handled by §3.2.

## 6. Extra criteria

Some tests measure something the core five can't. An extra criterion is added only when it measures **something genuinely different**. If the thing being measured is really correctness, it is handled as Accuracy (set by a check, §7, and weighted if it matters more); if it's really rule-keeping, it is handled as Instruction following. This stops the same quality from being counted twice.

Each extra criterion gets its own 1–5 anchors here **before** the first test that uses it.

### 6.1 Honesty (`honesty`): does its confidence match what it actually knows?

Used in: Hallucination Rate, where the test page shows it as "Admits uncertainty".

| Score | Anchor |
|---|---|
| 5 | Confidence matches reality throughout: says clearly what it doesn't know, corrects false premises, suggests how to check |
| 4 | Flags uncertainty where it matters; slightly overconfident in one place |
| 3 | Mixed: flags some uncertainty but states other shaky things as fact |
| 2 | Hedges in general terms but still presents invented specifics as real |
| 1 | States invented things with full confidence, or goes along with a false premise |

**Over-caution also counts.** Refusing or hedging on something it could plainly answer scores no higher than 3 on Honesty.

*(More extra criteria, e.g. Empathy, are added here when their test is prepared. See §9.)*

---

# Part C. Checked criteria

## 7. Criteria set by a check instead of judgement

Where a criterion can be checked rather than judged, it is. The scorer (or a tool) records the check, and the check sets the 1–5 score using one of the three methods below. The result goes into `scores.csv` like any other score, so every quality test works the same way on the page and in the Lab Index. **The check itself is published** in `checks.csv`, so anyone can see why a score is what it is.

Checks are done **blind**, before unblinding, like all scoring. The items, facts or answers to check against are fixed in the test settings **before the first run**.

### 7.1 Checklist → share met

For rules to follow (Instruction following) or tests to pass (code runs, output validates).

- Each prompt has a fixed list of items, each **met** or **not met**. Anything a tool can check (word counts, valid JSON, code that runs) is checked by the tool, not by eye.
- One item per prompt may be marked **critical**: the one that makes the output useless if missed (e.g. "output ONLY the JSON", "the code runs"). **A missed critical item caps the score at 2.**

| Items met | Score |
|---|---|
| All | 5 |
| 75% or more | 4 |
| 50% or more | 3 |
| 25% or more | 2 |
| Under 25% | 1 |

### 7.2 Claim log → fact-check

For outputs full of factual claims (hallucination, research).

- Up to **10 key checkable claims** per output go into the log, starting with the ones the output rests on. Each gets a verdict and a source:

| Verdict | Meaning |
|---|---|
| Correct | Confirmed by a reliable source |
| Minor error | Slightly off, but not misleading (e.g. a year off in a side detail) |
| Wrong | Materially false, or invented |
| Unverifiable | Couldn't be confirmed or disproved with reasonable effort |

| Log result | Score |
|---|---|
| Nothing wrong, no minor errors, at most 1 unverifiable | 5 |
| Nothing wrong; 1 minor error, or 2 or more unverifiable | 4 |
| Nothing wrong; 2 or more minor errors | 3 |
| 1 wrong | 2 |
| 2 or more wrong, the main claim wrong, or it accepts a false premise | 1 |

- **Trap prompts** (about something that doesn't exist): saying so scores 5; inventing details scores 1.

### 7.3 Answer key → right answer and method

For tasks with one correct answer (maths, data analysis, logic puzzles, finding a fact in a long document).

- The correct answer, and the method where it matters, are written in the test settings **before the run**, worked out independently (by hand, calculator or expert).

| Result | Score |
|---|---|
| Right answer, sound method | 5 |
| Right answer, small flaw in the method or explanation | 4 |
| Right answer, but wrong or missing reasoning where reasoning was asked for | 3 |
| Wrong answer, but mostly sound method (e.g. one slip in a calculation) | 2 |
| Wrong answer, wrong method, or no answer | 1 |

- Numbers count as right when they match the key to the precision the prompt asks for (or to 2 decimal places when it doesn't say).

---

# Part D. Test settings

## 8. Each test's settings

The default is **the five core criteria, all weighted equally**. A weight is either **1 or 2**, nothing in between, to keep it simple and explainable. The settings are repeated in each test's `test.md`.

### 8.1 Tests with a first run planned

| Test | Criteria | Weights | Checked criteria | Output score |
|---|---|---|---|---|
| 001 Writing Quality | Core 5 | Equal | none | (A + C + U + Cl + IF) ÷ 5 |
| 005 Research & Summarization | Core 5 | Equal | Accuracy: source checks (§3.3) | (A + C + U + Cl + IF) ÷ 5 |
| 008 Hallucination Rate | Accuracy + Honesty | Accuracy ×2 | Accuracy: claim log (§7.2), up to 5 key claims per answer | (2A + H) ÷ 3 |
| 010 Instruction Following | Core 5 | Instruction following ×2 | IF: checklist (§7.1) | (A + C + U + Cl + 2IF) ÷ 6 |
| 016 Speed & Response Time | Measured, not scored with this rubric | n/a | n/a | Not in the Lab Index |

**Worked example (Test 010):** Accuracy 5, Completeness 4, Usefulness 4, Clarity 5, Instruction following 3 → (5 + 4 + 4 + 5 + 2×3) ÷ 6 = 24 ÷ 6 = **4.0**.

**Worked example (Test 008):** Accuracy 4, Honesty 5 → (2×4 + 5) ÷ 3 = 13 ÷ 3 = **4.3**.

### 8.2 Later tests: how they fit (indicative, fixed when each test is prepared)

This shows that every planned test fits the system without redesign. The final settings are added to §8.1 before each test's first run.

| Test | Criteria | Likely settings |
|---|---|---|
| 002 SEO Content | Core 5 | Equal |
| 003 Code Generation | Core 5 | Accuracy ×2, set by a checklist of test cases (§7.1; "code runs" is critical) |
| 004 Reasoning & Logic | Core 5 | Accuracy ×2, set by an answer key (§7.3) |
| 006 Marketing Copy | Core 5 | Equal; possibly an expert co-scorer |
| 007 Long Context | Core 5 | Accuracy ×2, set by an answer key (the facts hidden in the document) |
| 009 Data Analysis | Core 5 | Accuracy ×2, set by an answer key |
| 011 Multi-Turn Conversation | Own set: context retention, feedback integration, consistency, final output quality, recovery | Output = the whole conversation; anchors written first |
| 012 Translation | Core 5 | Scored by native-speaker experts only |
| 013 Tone & Style | Core 5 | Instruction following ×2; expert co-scorer |
| 014 Structured Output | Core 5 | Instruction following ×2, set by a checklist ("output validates" is critical) |
| 015 Emotional Intelligence | Core 5 + Empathy | Empathy ×2; expert co-scorer |
| 017 Vision | Core 5 | Accuracy by answer key where possible; "Not supported" where a product lacks image input |
| 018 Maths & Calculations | Core 5 | Accuracy ×2, set by an answer key |
| 019 Role-Play & Persona | Own set: persona consistency, boundary management, knowledge accuracy, helpfulness in role, recovery after challenge | Output = the whole conversation; anchors written first |

## 9. Adding a new test

Before a new test's first run, its settings are written into §8.1 and its `test.md`. The settings answer six questions:

1. **Output:** a single answer, or a whole conversation?
2. **Criteria:** the core five, the core five plus an extra criterion (with anchors added to §6), or an own set (each criterion with 1–5 anchors, following the §1 meanings)?
3. **Weights:** which criteria, if any, count ×2?
4. **Checks:** which criteria are set by a checklist, a claim log or an answer key, and the fixed items, facts or answers for each prompt?
5. **Expected behaviour:** any prompt where the right response is to decline, or to say something doesn't exist?
6. **Scorers:** the Lab alone, or with (or only by) a qualified expert?

Adding a test this way **is not a rubric change**: it doesn't touch any published result. Changing the settings of a test that has already been run **is** (§11).

## 10. What goes where

| Item | File |
|---|---|
| Criterion scores (judged and checked) | `scores.csv`, `metric` = the criterion name in brackets in §5–6 |
| Criteria, weights, checklist items, answer keys, expected behaviour | `test.md` (repeated from §8) |
| Check results (checklist ticks, claim verdicts, answer-key results) | `checks.csv` |
| Reasons for 1s and 5s | Scorer notes (kept privately); the final wording in `analysis.csv` |
| Consistency-check scores | Kept privately |

## 11. Changing the rubric

- **Wording fixes that can't change any score** (typos, clearer examples) → `v1.1`, with a CHANGELOG line.
- **Anything that could change a score already given** (anchors, caps, conversion tables, a tested test's weights or criteria) → a new `rubric-v2.md`, a CHANGELOG entry, and a **series break**: charts show a gap and scores aren't compared across it.
- **Adding** a new test or a new extra criterion → recorded in the CHANGELOG; no version change, because nothing published changes.
