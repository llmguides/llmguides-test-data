## Conditions
- Plans: ChatGPT Plus · Claude Max · Google AI Pro
- Models: ChatGPT "GPT-6" (GPT-6 Sol), effort Medium · Claude "Opus 5.5", effort Medium, permission mode Auto · Gemini "3.8 Flash", Extended thinking off
- Model picker checked before every answer: ChatGPT "GPT-6" with Medium, Claude "Opus 5.5" with Medium, Gemini "3.8 Flash" with Extended thinking off.
- Model choice: the strongest model in each provider's standard paid plan chat, stable, no extra credits. Checked on the providers' official pages on 2026-10-08.
- Settings: memory, chat history, custom instructions and connected apps off; web search on; a fresh chat for every prompt.

## Deviations
None.

## Retries
- p02 gemini: retried in a new chat (first attempt asked to connect Gmail and gave no email). Both attempts asked to connect Gmail; after "No thanks" Gemini gave no email. The second attempt is the saved answer. No share link: Gemini returned "Something went wrong (13)" when creating it.

## Refusals and questions instead of answers
- p02 gemini: asked to connect Gmail instead of answering (see Retries).

## Anything else
- ChatGPT: since 2026-10-07, ChatGPT Plus uses GPT-6 Sol in Chat, per OpenAI's ChatGPT release notes, entry "October 7, 2026": https://help.openai.com/en/articles/6825453-chatgpt-release-notes
- Gemini 3.8 Flash API prices are promotional: $0.75 / $3.75 per 1M tokens through 2026-12-31, $1.50 / $7.50 from 2027-01-01, per Google's pricing page (link in prices.csv).
- Some answers showed part of the text in a separate box with its own copy button; those parts were copied separately and saved in on-screen order, unchanged.
- Token counts: chatgpt: tiktoken (local), encoding o200k_base (tiktoken has no entry for gpt-6-sol); claude: Anthropic token counting API with claude-opus-5-5, message overhead of 8 tokens subtracted; gemini: Gemini countTokens API with gemini-3.8-flash, message overhead of 1 token subtracted. Prompt and published answer only (no hidden instructions, search results or thinking).
