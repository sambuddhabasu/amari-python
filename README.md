# Amari Python Library

Amari connects your OpenAI calls to the internet. It automatically understands when your OpenAI calls need relevant real-time information from the internet and, augments your calls with them.

## Installation

You can install this package by running

```bash
pip install amari-python
```

### Example

```python
from amari import openai
openai.amari_api_key = "..."
openai.api_key = "sk-..."

chat_completion = openai.ChatCompletion.create(
    model="gpt-3.5-turbo", 
    messages=[{
        "role": "user",
        "content": "What's the weather in San Francisco today?"
    }],
    temperature=0,
)

print(chat_completion.choices[0].message.content)
# The current weather in San Francisco is 69°F with mostly sunny conditions.
```
