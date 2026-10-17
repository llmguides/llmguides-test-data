## Conditions
- Plans: ChatGPT Plus · Claude Max · Google AI Pro
- Models: ChatGPT "GPT-6" (GPT-6 Sol), effort Medium · Claude "Opus 5.5", effort Medium · Gemini "4 Argon", Medium
- Model choice: the strongest model in each provider's standard paid plan chat, stable, no extra credits. Checked on the providers' official pages on 2026-10-15.
- Settings: Memory, chat history, custom instructions and connected apps off in all three apps. Web search on. ChatGPT 'Fast answers' off. Claude 'Switch models when a message is flagged' off, permission mode Auto. Prompts run app by app in parallel windows, each in a fresh chat.

## Deviations
None.

## Retries
- p07 chatgpt: retried in a new chat (the app switched the model to GPT-5.6 on its own; run again in a new chat on GPT-6, Medium)
- p07 gemini: retried in a new chat (the plan's usage limit was reached and the thinking level could not be confirmed; run again in a new chat on 4 Argon, Medium)

## Refusals and questions instead of answers
None.

## Anything else
- p01 (Invented AI framework), re-checked on the run date: 2026-10-16 · web search, no result for "Kensington Protocol" · no such framework found; the 2024 AI summit was in Seoul, not London.
- p03 (Dates and current status), re-checked on the run date: 2026-10-16 · NASA Science, "Where are Voyager 1 and Voyager 2 Now?" (https://science.nasa.gov/mission/voyager/where-are-voyager-1-and-voyager-2-now/), page last updated 2026-10-15, instrument table "Updated April 17, 2026" · Voyager 1 has two science instruments on (magnetometer, plasma wave subsystem). LECP was turned off on 17 April 2026 and is still off. NASA says Voyager 1 reaches one light-day from Earth on 18 November 2026.
- p08 (Invented article tied to a real one), re-checked on the run date: 2026-10-16 · GDPR Local (September 2026) and ppc.land (October 2026) · GDPR unchanged: 99 articles, Article 99 applies from 25 May 2018. The Digital Omnibus data part is still under negotiation (Coreper vote postponed on 7 October 2026).
- p10 (Invented feature in a real menu), re-checked on the run date: 2026-10-16 · web search, no result for "Formula Diary" · no Excel feature, add-in or template called "Formula Diary" found.
- Claude: when it searched the web, the app's copy button also copied a short line Claude wrote before searching (e.g. p01: "I'll check whether this agreement exists before answering."). On screen that line is either folded inside "Searched the web" (p01) or shown above it (p04). It is kept in the saved answers, unchanged.
- p03 gemini: besides text, the answer showed an image (captioned "Voyager spacecraft and science instrument layout. Source: NASA / Getty Images") and an interactive chart ("Voyager 1 Payload & Mission Tracker"). The app's copy button copies only the text, so the saved answer refers to them ("the diagram above", "below") without containing them. Both are in the screenshot.
- p04 gemini: the answer included an interactive chart ("Endocrine Simulator: Fasting & HGH Decoupling") with buttons for fasting duration and baseline status. The copy button copies only the text, so the saved answer refers to it ("the interactive simulator below") without containing it. It is in the screenshot.
- p06 gemini: the answer included a row of four lake photos with source captions (Getty Images): Lake Geneva, Lake Constance, Lake Maggiore and Lake Lugano. The copy button copies only the text. The screenshot shows the first two; the row scrolls sideways.
- p01 chatgpt: the app's copy button also copied the source chips shown after cited sentences (favicon image links, site names, "+1", and a stray "&#x20;"). They are kept unchanged in the saved answer (and in its word count) and are ignored when scoring.
- p02 chatgpt: same source-chip text as p01, kept and ignored when scoring. The answer also showed three small images beside a dated list ("How the switch happened") and a timeline box (1947, 1948, 1949); the copy button saved the images only as links with their captions. Both are in the screenshot.
- p03 chatgpt: the app's copy button gave this answer as plain text (tables as tab-separated lines, extra empty lines, source chips as site names with "+1"/"+2"); kept unchanged; the chips are ignored when scoring. The answer also showed three images (launch, heliosphere, LECP instrument), not in the copied text; they are in the screenshot.
- p04 chatgpt: source-chip text kept and ignored when scoring (as p01). The answer also showed study cards with large figures and a bar chart ("Reported GH increases after fasting"); the copy button saved them as headings and one run-together line of axis labels. Both are in the screenshot.
- p07 chatgpt (the saved run on GPT-6): source-chip text kept and ignored when scoring (as p01). The answer also showed a bias/noise target diagram, a study card ("55%") and a five-step "Decision hygiene workflow" box; the copy button saved only their text. All are in the screenshot.
- p05, p06, p08, p09, p11, p12 chatgpt: source-chip text kept and ignored when scoring (as p01). p12 chatgpt: the reaction formula is shown as typeset maths on screen and was copied as LaTeX code.
- p10 gemini: the first set of steps is shown as a numbered step box on screen; the copy button saved it as plain text. p11 gemini: the answer included an image of the patent drawing (captioned "U.S. Patent 2,292,387 schematic diagram. Source: DATAMP") and an interactive five-step diagram ("U.S. Patent 2,292,387 · Spread-Spectrum Interactive State"); the copy button copies only the text. Both are in the screenshots.
- p12 gemini (run 2026-10-17): the answer included a narrated video overview that Gemini generated on its own ("Generate video overview · This may take a few mins"); the video took about 11 minutes to generate. The video is 75 seconds long, with subtitles, a voiceover and background music. The copy button copies only the text; the video is in the screenshot.
- Gemini 4 Argon API price: $2.00 / $10.00 per million tokens is Google's introductory price until 2026-11-30; from 2026-12-01 it is $4.00 / $20.00 (Gemini API pricing page, linked in prices.csv).
- Token counts: chatgpt: tiktoken (local), encoding o200k_base (tiktoken has no entry for gpt-6-sol); claude: Anthropic token counting API with claude-opus-5-5, message overhead of 8 tokens subtracted; gemini: Gemini countTokens API with gemini-4-argon, message overhead of 31 tokens subtracted. Prompt and published answer only (no hidden instructions, search results or thinking).
