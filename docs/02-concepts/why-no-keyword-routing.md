# Why No Keyword Routing

Keyword routing is brittle. It hides judgement behind words instead of evaluating the real task.

AgentPal forbids:

- `keyword_map`
- `domain_map`
- `role_map`
- direct rules like "code -> Atlas" or "test -> Quinn"

AgentPal allows:

- Pal capability summaries
- explicit `/pal Name` and `@Name` calls
- written owner judgement based on the actual request
- eval cases that prove keyword routing was avoided
