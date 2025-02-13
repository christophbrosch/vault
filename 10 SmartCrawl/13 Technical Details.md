
## OpenAI Specific

### Prompt Caching

<mark style="background-color: #ffd400">Quote</mark>
> Many developers use the same context repeatedly across multiple API calls when building AI applications, like when making edits to a codebase or having long, multi-turn conversations with a chatbot. Today, we’re introducing Prompt Caching, allowing developers to reduce costs and latency. By reusing recently seen input tokens, developers can get a 50% discount and faster prompt processing times.

<mark style="background-color: #ffd400">Quote</mark>
> API calls to supported models will automatically benefit from Prompt Caching on prompts longer than 1,024 tokens. The API caches the longest prefix of a prompt that has been previously computed, starting at 1,024 tokens and increasing in 128-token increments. If you reuse prompts with common prefixes, we will automatically apply the Prompt Caching discount without requiring you to make any changes to your API integration.


We will most likely be benefiting from cached input tokens given our input tokens are usually more than 1.024. As shown in the examples:

```json
{
  "text_tokens": 279,
  "completion_tokens": 68,
  "prompt_tokens": 1704,
  "total_tokens": 1772,
  "cached": 1536
}
```

## Repositories

### Pydantic GPC 
[*Link*](https://gitlab.rlp.net/KE3P/pydantic_gpc)

Python repository which generates pydantic classes based on the provided BRICK_CODE. Rendering the code with the usage of jinja2. The generated code has to be executed by the parent. 

##### TODO:
- [ ] Enums have variable names which are naively parsed. A more sophisticated approach could be beneficial. Example:
  ```python
  def replace_digits_with_words(string: str) -> str:
	"""Replace digits with words."""
	return (
		string.replace("0", "ZERO")
		.replace("1", "ONE")
		.replace("2", "TWO")
		.replace("3", "THREE")
		.replace("4", "FOUR")
		.replace("5", "FIVE")
		.replace("6", "SIX")
		.replace("7", "SEVEN")
		.replace("8", "EIGHT")
		.replace("9", "NINE")
	)
```


## Modelle


| Modell | Token Limit | € / 1k Tokens | Supports Caching | Support Batch |
| ------ | ----------- | ------------- | ---------------- | ------------- |
|        |             |               |                  |               |
|        |             |               |                  |               |
