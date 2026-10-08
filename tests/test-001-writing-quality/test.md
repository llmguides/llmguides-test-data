# Test 001: Writing Quality
Slug: llm-writing-quality-test
Type: rubric
Surface: app
Counts toward Lab Index: yes
Rubric: rubric-v1
Output: answer
Criteria: accuracy, completeness, usefulness, clarity, instruction_following
Weights: equal
Runs per prompt: 1
Scorers: lab

Everyday writing tasks a professional actually hands to an AI assistant: blog, email, product, fiction, board summary, social, explanation and landing page copy. Every answer is scored with the five core criteria of rubric v1, all weighted equally.

## Prompts

### p01: Blog introduction
Tests: hook quality, narrative flow, use of data, a clear promise to the reader
Expected: answer
Length: target 150 words
Scoring:
- Must include: about 150 words (target 150, ±10%: 135–165) · written for mid-career professionals who moved to remote work recently · confident, not preachy · at least one statistic or data point · ends with a clear promise of what the reader will learn.
- Invented: a statistic presented as fact that no trustworthy source supports → invented fact (Accuracy ≤ 2). If the answer names a source, the figure is checked in that source; a real source that doesn't contain it counts as invented. If no source is named, the trusted sources are searched; not found = invented. A clearly marked placeholder ("[insert statistic]") or a clearly labelled hypothetical is not invented, but it fulfils the request less well (Completeness).
- Accuracy: claim log for each statistic: the figure, what it measures, the source. Statistics are estimates: correct if a trustworthy source says it.
- 5 looks like: an opening that speaks to this reader's situation, a real and correctly attributed statistic that supports the argument, a confident tone without lecturing, and a specific promise at the end ("you'll learn three habits that…").
- 3 looks like: right length and a statistic, but a generic opening ("In today's fast-paced world…"), the statistic dropped in without use, or a vague promise ("let's explore").
- Watch for: a lecturing "you must" tone (Usefulness); the promise missing, or buried mid-paragraph instead of at the end (Instruction following); a title, headline or notes around the intro (not counted for length; Usefulness); a real study given the wrong year or source (minor if it's clearly the same study, wrong if it's a different one).

```text
Write a 150-word introduction for a blog post about remote work productivity. The audience is mid-career professionals who transitioned to remote work in the last 2 years. Tone should be confident but not preachy. Include at least one data point or statistic. End with a clear promise of what the reader will learn.
```

### p02: Professional email
Tests: tone, diplomacy, practical structure
Expected: answer
Length: max 200 words
Scoring:
- Must include: under 200 words · the two-week delay stated clearly · the cause (a vendor dependency) explained honestly, without blaming the client · a revised timeline (a date or concrete milestones) · a tone that keeps the relationship.
- Invented: not a fact-checking prompt. Names, dates and project details the brief doesn't give are fine as placeholders ([Client name], [new date]) or plainly generic wording. Promises the writer can't make for the company (a discount, a refund, free extra work) aren't invented facts, but they're a risky email to send (Usefulness).
- 5 looks like: a clear subject line; the delay and the new date in the first lines; a short, honest reason; what is being done to limit the impact; a concrete next step (a call or a check-in date); warm but not grovelling; ready to send once the placeholders are filled.
- 3 looks like: all parts present, but the new timeline is vague ("in the coming weeks"), the tone over-apologises, or the bad news is buried under pleasantries.
- Watch for: no new date at all (Instruction following); harsh blame on the vendor by name (Usefulness); several alternative versions or notes around the email (not counted for length; Usefulness).

```text
Draft a professional email to a client explaining that their project will be delivered 2 weeks late due to a vendor dependency. Maintain the relationship. Propose a revised timeline. Keep it under 200 words.
```

### p03: Product description
Tests: persuasion, feature highlighting, concision, call to action
Expected: answer
Length: max 150 words
Scoring:
- Must include: at most 150 words · written for frequent travellers · exactly 3 key features highlighted · a call to action · the price, if mentioned, stated as $299.
- Invented: *product attributes* are allowed fill-ins, since the brief gives none (battery hours, comfort, fold-flat design, controls). *Claims about the outside world* are invented facts (Accuracy ≤ 2): awards, reviews, star ratings, "best-selling", customer counts, "trusted by X", expert or airline endorsements, and offers the brief doesn't give (discounts, free shipping, trials, bundles). A price other than $299 is wrong.
- 5 looks like: every feature tied to a traveller's moment (engine noise on a long flight, a battery that outlasts a long-haul trip, packing light), concise and confident, and a call to action that fits the audience ("Pack them for your next flight").
- 3 looks like: features that would fit any audience, features listed without benefits, or a flat call to action ("Buy now").
- Watch for: more or fewer than 3 features clearly highlighted (Instruction following); invented social proof such as "loved by 50,000 travellers" (Accuracy ≤ 2); notes or alternative versions around the description (not counted for length; Usefulness).

```text
Write a compelling product description for wireless noise-canceling headphones priced at $299. Target audience: frequent travelers. Highlight 3 key features. Include a call-to-action. Maximum 150 words.
```

### p04: Story opening
Tests: voice, sensory detail, tension, originality
Expected: answer
Length: range 100-150 words
Scoring:
- Must include: one paragraph, 100–150 words · set in Tokyo · during a rainstorm · a character receives an unexpected text message · sensory detail · the character is not named.
- Invented: not applicable. Fiction is asked for; invented details are the point.
- 5 looks like: vivid detail from several senses, real tension around the message, at least one original image, reads like a published opening.
- 3 looks like: all elements present but generic (stock images like "neon reflected in puddles"), little tension, or the message is only mentioned.
- Clarity: can the reader follow what happens? Vivid language is not a clarity problem unless it confuses.
- Watch for: a named character; more than one paragraph; text around the story (it doesn't count toward the length, but it's an edit for the reader: Usefulness).

```text
Write the opening paragraph (100–150 words) of a short story set in Tokyo during a rainstorm. A character receives an unexpected text message. Use sensory detail. Don't name the character yet.
```

### p05: Executive summary
Tests: data synthesis, concision, insight, board-level communication
Expected: answer
Length: target 100 words
Scoring:
- Must include: about 100 words (target 100, ±10%) · the key figures (revenue, operating costs, new customers, churn, NPS, headcount, the Acme contract, the two resignations) · both the good and the concerning · written for a board.
- Invented: any figure not in the given data. Own calculations (e.g. margin, growth) are allowed if correct and clearly derived; a wrong calculation is an Accuracy issue.
- 5 looks like: every key figure correct, a clear interpretation (costs growing faster than revenue, customer health weakening), and one line on what the board should watch or decide.
- 3 looks like: figures listed correctly but barely interpreted, or one important figure missing.
- Watch for: omitted figures (e.g. the 340 new customers, the 3.1% previous churn); labels like "(~100 words)" or notes around the summary (not counted for length; an edit for the reader: Usefulness).

```text
Summarize the following quarterly data into a 100-word executive summary for a board presentation:

Q4 2025 Performance:
- Revenue: $4.2M (up 12% QoQ)
- Operating costs: $3.1M (up 18% QoQ)
- New customers: 340 (down 5% QoQ)
- Customer churn: 4.2% (up from 3.1%)
- NPS score: 72 (down from 78)
- Headcount: 85 (up from 71)
- Key win: Enterprise contract with Acme Corp ($800K ARR)
- Key risk: Two senior engineers resigned

Focus on what the board needs to know. Highlight both the good and the concerning.
```

### p06: LinkedIn hooks
Tests: engagement writing, variety, platform awareness, brevity
Expected: answer
Scoring:
- Must include: exactly 3 hooks on how AI is changing hiring · each 1–2 sentences · hook 1 opens with a surprising data point · hook 2 opens with a provocative question or contrarian take · hook 3 opens with a brief personal story or observation · written for LinkedIn.
- Invented: hook 1's data point (and any other statistic) presented as fact must be real: if a source is named, the figure is checked in it; if not, the trusted sources are searched; not found = invented → Accuracy ≤ 2. A clearly marked placeholder ("[X]% of recruiters…") is not invented, but it fulfils the request less well (Completeness). Hook 3's personal story is a writing device written for the user, not a fact; real people, companies or events named in it are checked like any claim.
- Accuracy: claim log for each statistic: the figure, what it measures, the source. Statistics are estimates: correct if a trustworthy source says it.
- 5 looks like: three clearly different approaches, each one would make a reader stop scrolling, a real and checkable data point stated without distortion, short punchy sentences, no hashtag or emoji clutter.
- 3 looks like: the approaches blur together, the data point is vague ("studies show…"), or one hook is weak or generic ("AI is changing everything").
- Watch for: a hook longer than 2 sentences, or full posts instead of hooks (Instruction following); a real statistic exaggerated to sound more surprising (Accuracy: wrong claim); notes or explanations around the hooks (Usefulness).

```text
Write 3 different LinkedIn post opening hooks about how AI is changing the hiring process. Each hook should be 1–2 sentences maximum. Make them stop-the-scroll compelling. Use varied approaches:

Hook 1: Lead with a surprising data point
Hook 2: Lead with a provocative question or contrarian take
Hook 3: Lead with a brief personal story or observation
```

### p07: Technical explanation
Tests: simplification, analogy, accuracy, audience awareness
Expected: answer
Length: max 200 words
Scoring:
- Must include: under 200 words · how DNS works (it turns domain names into the numeric addresses computers use to find a site) · an analogy · no jargon (technical terms avoided or explained in plain words) · ends with one specific reason a marketing manager should care when managing the website.
- Invented: not applicable as such; technical facts are settled and checked under Accuracy.
- Accuracy: claim log of up to 5 key claims: what DNS does, how a lookup works (if described), any claim about caching or how long changes take to spread, and the reason to care. Wrong examples: DNS stores the website; DNS is the same as hosting; DNS changes always take effect instantly.
- 5 looks like: one clear analogy carried through (a phone's contact list, a directory), accurate in plain words, and a concrete reason tied to the manager's job (moving the site to a new host, setting up email for the domain, a lapsed domain renewal taking the site down).
- 3 looks like: accurate, but the analogy is muddled or dropped halfway, a technical term is left unexplained ("resolver", "TTL", "A record"), or the closing reason is generic ("it's important for your website").
- Watch for: several reasons at the end instead of one (Instruction following); simplification that becomes wrong (Accuracy); plain terms like "IP address" are fine if explained.

```text
Explain how DNS (Domain Name System) works to a non-technical marketing manager who manages their company's website. Use an analogy to make it intuitive. Keep it under 200 words. No jargon. End with one specific reason they should care about DNS when managing their website.
```

### p08: Landing page hero
Tests: value proposition, benefit-led writing, structure, call to action
Expected: answer
Parts: headline ≤ 10 words · subheadline ≤ 25 words · 3 bullets ≤ 8 words each · CTA ≤ 5 words
Scoring:
- Must include: all four parts, each within its word limit · focus on time saved and frustration removed, not features · urgent but not pushy.
- Invented: *product attributes* (what the tool does: books meetings, syncs calendars, sends reminders) are allowed fill-ins. Any number, statistic, price, offer ("free", "14-day trial") or customer claim not in the brief → invented fact (Accuracy ≤ 2).
- 5 looks like: every part within its limit, benefit-led, specific to small-business booking pain, ready to paste.
- 3 looks like: all parts present but generic ("Save time today"), or one part over its limit.
- Watch for: feature lists instead of benefits; urgency that turns pushy; invented numbers in the headline ("Save 5 hours a week").

```text
Write a landing page hero section for an AI-powered scheduling tool aimed at small business owners who waste time on back-and-forth booking emails. Include:

- Headline (max 10 words)
- Subheadline (max 25 words)
- 3 bullet points (max 8 words each)
- CTA button text (max 5 words)

Focus on time saved and frustration eliminated, not features. Make it feel urgent but not pushy.
```
