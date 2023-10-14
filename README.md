# Jupyter-Notebook-GPT-Integration

This repo showcases the integration of OpenAI's GPT with Jupyter Notebook for chat interactions. Dive into real-time code, visualizations, and harness the power of conversational AI seamlessly in an interactive environment.


# OpenAI GPT-3 Integration with Python


This guide provides step-by-step instructions on how to integrate OpenAI's GPT-3 API into a Python environment to generate natural language responses.

## Prerequisites

- An API key from OpenAI (you'll need to sign up on the OpenAI platform and accept their terms).
- Python installed.
- `openai` Python package installed (you can install it via `pip install openai`).

## Step 1: Import the necessary module

```python
- import openai
```

## Step 2: Setting up the API Key

```python
openai.api_key = 'Enter Key'
```

## Step 3: Define the function to get a response from GPT-3

```python
def get_gpt_response(prompt, max_tokens = 200):
    prompt = f"Answer the following question: {prompt}\nAnswer:"
    response = openai.Completion.create(
        engine = "text-davinci-003",
        prompt = prompt,
        max_tokens=500,
        n=1,
        temperature = 0.7
    )
    return response.choices[0].text.strip()

  
This function sends a prompt to the GPT-3 API and retrieves a response.

- `engine` is set to `text-davinci-003`, which is one of OpenAI's GPT-3 engines.
- `max_tokens` is set to 500, which means the response will be up to 500 tokens long.
- `n=1` indicates that we want one response.
- `temperature` is set to 0.7, influencing the randomness of the output.

   ```

## Step 4: Use the function to get a response </h>

```python
prompt = "What are the key benefits of using renewable energy?"
response = get_gpt_response(prompt)
print(response)
```

## Sample Output

The key benefits of using renewable energy are:

1. Reduced dependence on non-renewable energy sources such as fossil fuels, which are finite and polluting.
2. Reduced emissions of greenhouse gases, which are contributing to global warming and climate change.

## Sample Code

![Image displaying sample code in VS code.](images/API.png)

