# Test 010: Instruction Following
Slug: llm-instruction-following-test
Type: rubric
Surface: app
Counts toward Lab Index: yes
Rubric: rubric-v1
Output: answer
Criteria: accuracy, completeness, usefulness, clarity, instruction_following
Weights: instruction_following 2
Checked: instruction_following checklist
Runs per prompt: 1
Scorers: lab

## Prompts

### p01: Exact word count
Tests: precise count adherence
Expected: answer
Length: exactly 75 words
Checklist:
- c1 [critical] [tool]: exactly 75 words
- c2 [tool]: one paragraph
- c3: about the benefits of reading
Scoring:
- Must include: one paragraph about the benefits of reading, exactly 75 words.
- Invented: any statistic, study or named research not asked for counts as invented (Accuracy ≤ 2) unless it is real and correct.
- 5 looks like: exactly 75 words, one paragraph, concrete benefits (vocabulary, focus, empathy, stress), no filler.
- 3 looks like: on topic and one paragraph, but generic ("reading is important for everyone").
- Watch for: a lead-in or a word-count note around the paragraph ("Here's a 75-word paragraph:", "(75 words)"). It doesn't count toward the 75, but it's something to delete, so it costs Usefulness or Clarity.

```text
Write a paragraph about the benefits of reading. It must be EXACTLY 75 words. Not 74, not 76. Count carefully before submitting.
```

### p02: Vocabulary restriction
Tests: simplicity under constraint
Expected: answer
Length: max 99 words
Checklist:
- c1 [tool]: under 100 words
- c2 [critical]: no technical terms (names of engine parts or processes a 7-year-old wouldn't know, e.g. piston, cylinder, combustion, crankshaft, ignition, fuel injection)
- c3: no word longer than 3 syllables
- c4: explains how the engine makes the car move
Scoring:
- Must include: what goes in (fuel and air), what happens (it burns or goes "boom" and pushes), and how that turns the wheels, in a 7-year-old's words.
- Invented: none expected. A simplification is fine; a false statement is not (e.g. "the engine runs on water").
- 5 looks like: under 100 words, everyday words only, a picture a child can hold (tiny pushes, many times a second), and the chain from fuel to wheels is complete.
- 3 looks like: simple words, but the explanation stops halfway (the fuel burns, then nothing about the wheels), or one technical word slips in.
- Watch for: syllables are counted by eye, not by the tool. "Gasoline", "energy" and "explosion" are 3 syllables (fine); "electricity", "automobile" and "mechanical" (4 or more) are not. "Under 100 words" means 99 at most. Text around the explanation doesn't count toward the length.

```text
Explain how a car engine works using only words that a 7-year-old would understand. No technical terms whatsoever. No words longer than 3 syllables. Keep it under 100 words.
```

### p03: Strict format compliance
Tests: template adherence
Expected: answer
Checklist:
- c1 [tool]: exactly 5 tips
- c2: each tip starts with one emoji
- c3 [tool]: each tip's title is in all capitals
- c4: each tip's title is bold
- c5: an em dash (—) between the title and the explanation, as in the format
- c6: each explanation is one sentence in regular text (not bold, not capitals), ending with a period
- c7 [tool]: no introduction, conclusion or numbering
Scoring:
- Must include: 5 productivity tips, every one in the format "[emoji] [TITLE IN BOLD CAPITALS] — [one sentence.]", and nothing else.
- Invented: a statistic or study used to support a tip counts as invented unless real and correct.
- 5 looks like: all 7 items met, and 5 distinct, practical tips with a concrete explanation each.
- 3 looks like: the format is followed, but the tips are generic or overlap ("stay focused", "avoid distractions").
- Watch for: an item is met only if all 5 tips meet it. Bold and other formatting are judged from the screenshot, because copy buttons copy formatting differently; everything else from the saved text. Reusing the example tip (batch similar tasks) is allowed but adds nothing: Usefulness, not Instruction following.

```text
List 5 productivity tips. Each tip MUST follow this exact format with no deviations:

[EMOJI] [TIP IN ALL CAPS BOLD] — [One sentence explanation in regular text, ending with a period.]

Example:
🔥 BATCH SIMILAR TASKS — Group emails, calls, and admin work into dedicated time blocks to reduce context switching.

Do not add any introduction, conclusion, or numbering.
```

### p04: Multiple simultaneous constraints
Tests: handling stacked rules
Expected: answer
Checklist:
- c1 [critical] [tool]: exactly 7 reasons
- c2: each reason is exactly 2 sentences
- c3: the first sentence states the reason
- c4: the second sentence gives a specific real-world example (a named company, product, project or field use, not "many companies use it")
- c5 [tool]: bullet points, no numbering
Scoring:
- Must include: 7 bullets, each one reason in one sentence plus one specific, real example in a second sentence.
- Invented: every example is a factual claim. A wrong one (a company that doesn't use Python as described, an invented project) counts as invented: Accuracy ≤ 2.
- 5 looks like: all 5 items met; 7 distinct reasons (not "it's popular" twice in other words); examples that are real and checkable (e.g. Instagram's Django backend, NumPy and pandas in data science).
- 3 looks like: the structure is right, but the examples are vague ("used by top tech firms") or two reasons repeat.
- Watch for: a heading or a closing line around the list doesn't break c1–c5; it costs Usefulness or Clarity. A sentence joined with a semicolon still counts as one sentence.

```text
Give me exactly 7 reasons to learn Python. Not 6, not 8 — exactly 7. Each reason must be exactly 2 sentences long. The first sentence states the reason. The second sentence gives a specific real-world example. Do not number them — use bullet points instead.
```

### p05: Negative constraints (exclusion)
Tests: avoiding specified content
Expected: answer
Length: target 100 words
Checklist:
- c1 [tool]: 90–110 words (100 words, ±10%)
- c2 [critical] [tool]: none of the six excluded items is mentioned (the Eiffel Tower, croissants, fashion, romance, the Seine, the Louvre)
- c3: written for a travel website (it invites the reader to visit)
- c4: offers specific alternative angles (named places, food or experiences), not generic praise
Scoring:
- Must include: a 100-word travel description of Paris built on other angles, with none of the six excluded items.
- Invented: every named place, dish or event must be real and in Paris; an invented or misplaced one counts as invented (Accuracy ≤ 2).
- 5 looks like: around 100 words, nothing excluded, 3 or more specific angles (e.g. Canal Saint-Martin, Père Lachaise, a market, a neighbourhood), and it makes you want to go.
- 3 looks like: no excluded item, but generic ("charming streets, great food, rich history").
- Watch for: the tool finds the names and their word families ("romantic" counts as romance, "fashionable" as fashion, "croissanterie" as croissants). An indirect reference counts only when it unmistakably points to an excluded item ("the famous iron tower", "the river that runs through the city"); every other reasonable reading is accepted. Shopping or boutiques are not fashion unless clothes or designers are the point.

```text
Write a 100-word description of Paris, France for a travel website. You CANNOT mention any of the following: the Eiffel Tower, croissants, fashion, romance, the Seine River, or the Louvre. Find completely different angles that would still make someone want to visit.
```

### p06: Persona and rules stacking
Tests: keeping a persona while following rules
Expected: answer
Length: range 80-100 words
Checklist:
- c1: pirate voice from the first line to the last
- c2: exactly 3 project management terms
- c3: each of the 3 terms used correctly
- c4 [tool]: 80–100 words
- c5 [tool]: ends with exactly one hashtag
- c6 [tool]: neither "ahoy" nor "matey" (in any form)
- c7: reads as a LinkedIn post about project management best practices
Scoring:
- Must include: a LinkedIn-style post in a consistent pirate voice, about project management best practices, with exactly 3 real PM terms used correctly, 80–100 words, one hashtag at the end, no "ahoy" or "matey".
- Invented: none expected; the post is fiction by request. A PM term used with the wrong meaning is a c3 miss, not an invented fact.
- 5 looks like: all 7 items met, and the pirate imagery actually carries the advice (charting the critical path, scope creep as barnacles), not pirate words sprinkled on a plain post.
- 3 looks like: the rules are mostly met, but the voice fades mid-post or the advice is thin.
- Watch for: what counts as a PM term: an established term of the discipline (e.g. critical path, scope creep, sprint, milestone, stakeholder, backlog, deliverable, retrospective, Gantt chart, risk register). Everyday words (team, deadline, plan, goal, project) don't count. Write down which terms you counted. The hashtag counts as a word and as the post's end; text after the hashtag (a note, a word count) is outside the post.

```text
You are a pirate captain writing a LinkedIn post about project management best practices. Requirements:
1. Maintain the pirate voice consistently throughout
2. Include exactly 3 legitimate project management terms used correctly (e.g., 'critical path', 'scope creep', 'sprint')
3. Post must be 80–100 words
4. End with exactly one relevant hashtag
5. Do NOT use the words 'ahoy' or 'matey' — find other pirate expressions
```

### p07: JSON-only output
Tests: format compliance with zero prose
Expected: answer
Checklist:
- c1 [critical] [tool]: the response is only the JSON object: it parses as JSON, the first character is { and the last is }, with no text before or after
- c2: no Markdown code block
- c3 [tool]: exactly the six fields, with these exact names, and no others
- c4 [tool]: types as asked: name and cuisine are strings, rating is a number from 1 to 5, is_open is a boolean, top_dishes is an array of strings
- c5 [tool]: price_range is one of "$", "$$" or "$$$"
- c6 [tool]: top_dishes has exactly 3 items
Scoring:
- Must include: one valid JSON object with the six fields, and nothing else.
- Invented: a made-up restaurant is what the prompt asks for ("realistic data"), so it isn't invented. If it names a real restaurant, the details must be true.
- 5 looks like: all 6 items met, and the data is realistic: the dishes belong to the cuisine and the rating fits the 1–5 scale.
- 3 looks like: valid and complete, but the data doesn't hang together (sushi dishes for an Italian restaurant).
- Watch for: whether a code block was shown is judged from the screenshot, because copy buttons add or strip the backticks; c1 is judged from the saved text with any code fence removed. A rating given as a string ("4.5") fails c4.

```text
Create a JSON object for a restaurant. Use these EXACT fields:
- name (string)
- cuisine (string)
- rating (number, 1–5)
- price_range (must be one of: "$", "$$", "$$$")
- is_open (boolean)
- top_dishes (array of exactly 3 strings)

Use realistic data. Output ONLY the JSON. No explanation, no markdown code blocks, no commentary before or after. The first character of your response should be { and the last should be }
```

### p08: Alphabet, length and fact constraints
Tests: three rule systems at once
Expected: answer
Checklist:
- c1 [tool]: exactly 5 sentences
- c2 [tool]: the sentences start with A, B, C, D and E, in that order
- c3 [tool]: no sentence longer than 12 words
- c4: each sentence contains a specific, verifiable fact (a number, date, name or measurable claim)
- c5 [tool]: nothing but the 5 sentences (no introduction, explanation or closing)
Scoring:
- Must include: 5 sentences about climate change, A to E, each 12 words or fewer, each with one specific, checkable fact, and nothing else.
- Invented: every fact is checked. One false or untraceable fact caps Accuracy at 2 (c4 can still be met: it was specific and verifiable, just wrong).
- 5 looks like: all 5 items met, and all 5 facts are true and precise (e.g. a CO₂ concentration with its source year, a named agreement with its year).
- 3 looks like: the form is right, but two sentences are vague claims rather than facts ("Emissions keep rising worldwide").
- Watch for: the prompt asks for the sentences only, so any text around them is an Instruction following miss (c5), not a Usefulness one (rubric §3.2 exception). Numbers count as one word each; "CO₂" is one word.

```text
Write exactly 5 sentences about climate change. All three rules must be followed simultaneously:
Rule 1: Each sentence must start with the next letter of the alphabet (start with A, then B, C, D, E)
Rule 2: No sentence may be longer than 12 words
Rule 3: Each sentence must contain a specific, verifiable fact
Do not explain your approach — just write the 5 sentences.
```
