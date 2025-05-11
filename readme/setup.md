# Set up for LLM Engineering

### 1 - Install python and required packages
Install python v3.11.9 => https://www.python.org/
Optionally add the new python version to your path and also as an alias
in .bash_profile:
```
alias virtualenv='python -m venv'
alias python=/Library/Frameworks/Python.framework/Versions/3.11/bin/python3
```
And check:
```
$ python --version
Python 3.11.9
```


Set uyp your virtual environemnt and activate it
```
virtualenv llm_training
source llm_training/bin/activate
```

Install the required packages: 
``` 
python3 -m pip install -r requirements.txt
```


### Start Jupyter lab
```
jupyter lab
```

### 2 - OpenAI key (OPTIONAL but recommended)

Particularly during weeks 1 and 2 of the course, you'll be writing code to call the APIs of Frontier models (models at the forefront of AI).

For week 1, you'll only need OpenAI, and you can add the others if you wish later on.

1. Create an OpenAI account if you don't have one by visiting:
https://platform.openai.com/

2. OpenAI asks for a minimum credit to use the API. For me in the US, it's \$5. The API calls will spend against this \$5. On this course, we'll only use a small portion of this. I do recommend you make the investment as you'll be able to put it to excellent use. But if you'd prefer not to pay for the API, I give you an alternative in the course using Ollama.

You can add your credit balance to OpenAI at Settings > Billing:  
https://platform.openai.com/settings/organization/billing/overview

I recommend you disable the automatic recharge!

3. Create your API key

The webpage where you set up your OpenAI key is at https://platform.openai.com/api-keys - press the green 'Create new secret key' button and press 'Create secret key'. Keep a record of the API key somewhere private; you won't be able to retrieve it from the OpenAI screens in the future. It should start `sk-proj-`.

In week 2 we will also set up keys for Anthropic and Google, which you can do here when we get there.  
- Claude API at https://console.anthropic.com/ from Anthropic
- Gemini API at https://ai.google.dev/gemini-api from Google

Later in the course you'll be using the fabulous HuggingFace platform; an account is available for free at https://huggingface.co - you can create an API token from the Avatar menu >> Settings >> Access Tokens.

And in Week 6/7 you'll be using the terrific Weights & Biases at https://wandb.ai to watch over your training batches. Accounts are also free, and you can set up a token in a similar way.

### 3 - .env file

When you have these keys, please create a new file called `.env` in your project root directory. The filename needs to be exactly the four characters ".env" rather than "my-keys.env" or ".env.txt". Here's how to do it:

1. Open Terminal (Applications > Utilities > Terminal)

2. Navigate to the "project root directory" using `cd ~/Documents/Projects/llm_engineering` (replace this path with the actual path to the llm_engineering directory, your locally cloned version of the repo).

3. Create the .env file with

nano .env

4. Then type your API keys into nano, replacing xxxx with your API key (starting `sk-proj-`).

```
OPENAI_API_KEY=xxxx
```

If you have other keys, you can add them too, or come back to this in future weeks:  
```
GOOGLE_API_KEY=xxxx
ANTHROPIC_API_KEY=xxxx
DEEPSEEK_API_KEY=xxxx
HF_TOKEN=xxxx
```

5. Save the file:

Control + O  
Enter (to confirm save the file)  
Control + X to exit the editor

6. Use this command to list files in your project root directory:

`ls -a`

And confirm that the `.env` file is there.

This file won't appear in Jupyter Lab because jupyter hides files starting with a dot. This file is listed in the `.gitignore` file, so it won't get checked in and your keys stay safe.

### Part 5 - Showtime!!

- Open Terminal (Applications > Utilities > Terminal)
  
- Navigate to the "project root directory" using `cd ~/Documents/Projects/llm_engineering` (replace this path with the actual path to the llm_engineering directory, your locally cloned version of the repo). Do `ls` and check you can see subdirectories for each week of the course.  

- Activate your environment with `conda activate llms` (or `source llms/bin/activate` if you used the alternative approach in Part 2B)

- You should see (llms) in your prompt which is your sign that all is well. And now, type: `jupyter lab` and Jupyter Lab should open up, ready for you to get started. Open the `week1` folder and double click on `day1.ipynb`.

