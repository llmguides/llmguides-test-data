## Conditions
- Plans: ChatGPT Plus · Claude Max · Google AI Pro
- Models: ChatGPT "GPT-6" (GPT-6 Sol), effort Medium · Claude "Opus 5.5", effort Medium · Gemini "4 Argon", Medium
- Model choice: the strongest model in each provider's standard paid plan chat, stable, no extra credits. Checked on the providers' official pages on 2026-11-04.
- Settings: Memory, chat history and custom instructions off in all three apps. Web search on. Connected apps off in ChatGPT and Gemini; in Claude connectors are set to "Only when a chat needs them" (the app has no off option). ChatGPT 'Fast answers' off. Claude 'Switch models when a message is flagged' off, permission mode Auto. Each prompt runs in a fresh chat.

## Deviations
None.

## Retries
None.

## Refusals and questions instead of answers
None.

## Anything else
- p03 chatgpt: the tip titles are bold on screen, but ChatGPT's copy button copied them without bold marks. The screenshot shows the formatting.
- p04 gemini: on screen the code terms appear as code chips and the bullets as hollow circles; the copy button copied them as backticks and "*" bullets. Two suggestion cards under the answer were not copied. The screenshot shows the formatting.
- p04 chatgpt: on screen each point starts with a plain "-" typed as text (not a list bullet) and its first sentence is bold. The copy button copied the dashes as "\-" and dropped the bold. The screenshot shows the formatting.
- p05 gemini: under the answer Gemini added a follow-up question with a Yes button; they were not copied. The screenshot shows them.
- p05 chatgpt: the answer was shown in a 'Writing' box with two suggestion buttons under it; the text was copied with the box's copy button, and the buttons were not copied.
- p06 chatgpt: the answer was shown in a 'Writing' box with two suggestion buttons under it; the text was copied with the box's copy button, and the buttons were not copied.
- p07 claude: on screen the JSON shows curly quotes; the copy button copied straight quotes.
- p07 chatgpt: on screen the answer is plain JSON over 12 lines, without a code block. ChatGPT's copy button (the only one) added a backslash at the end of each line and "&#x20;" for spaces, so the copied text does not parse as JSON. The JSON checklist items are judged from the JSON as shown on screen; the screenshot is the record.
- ChatGPT's screenshots show the effort (Medium) but not the model name; GPT-6 was picked in each new chat.
- Gemini 4 Argon API price: $2.00 / $10.00 per million tokens is Google's introductory price until 2026-11-30; from 2026-12-01 it is $4.00 / $20.00 (Gemini API pricing page, linked in prices.csv).
- Token counts: chatgpt: tiktoken (local), encoding o200k_base (tiktoken has no entry for gpt-6-sol); claude: Anthropic token counting API with claude-opus-5-5, message overhead of 8 tokens subtracted; gemini: Gemini countTokens API with gemini-4-argon, message overhead of 31 tokens subtracted. Prompt and published answer only (no hidden instructions, search results or thinking).
