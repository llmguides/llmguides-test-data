## Conditions
- Plans: ChatGPT Plus · Claude Max · Google AI Pro
- Models: ChatGPT "GPT-6" (GPT-6 Sol), effort Medium · Claude "Opus 5.5", effort Medium · Gemini "4 Argon", Medium
- Model choice: the strongest model in each provider's standard paid plan chat, stable, no extra credits. Checked on the providers' official pages on 2026-10-15.
- Settings: Memory, chat history, custom instructions and connected apps off in all three apps. Web search on. ChatGPT 'Fast answers' off. Claude 'Switch models when a message is flagged' off, permission mode Auto. Prompts run app by app in parallel windows, each in a fresh chat.

## Deviations
None.

## Retries
None.

## Refusals and questions instead of answers
None.

## Anything else
- p03 chatgpt: the tip titles are bold on screen, but ChatGPT's copy button copied them without bold marks. The screenshot shows the formatting.
- p04 chatgpt: on screen each point starts with a plain "-" typed as text (not a list bullet) and its first sentence is bold. The copy button copied the dashes as "\-" and dropped the bold. The screenshot shows the formatting.
- p07 chatgpt: on screen the JSON is shown over 12 lines (no code box); the copy button copied it as one line, with spaces in place of the line breaks. The content is the same and the screenshot shows the layout.
- Gemini 4 Argon API price: $2.00 / $10.00 per million tokens is Google's introductory price until 2026-11-30; from 2026-12-01 it is $4.00 / $20.00 (Gemini API pricing page, linked in prices.csv).
- Token counts: chatgpt: tiktoken (local), encoding o200k_base (tiktoken has no entry for gpt-6-sol); claude: Anthropic token counting API with claude-opus-5-5, message overhead of 8 tokens subtracted; gemini: Gemini countTokens API with gemini-4-argon, message overhead of 31 tokens subtracted. Prompt and published answer only (no hidden instructions, search results or thinking).
