# LLM Engineering
## Master AI, Large Language Models & Agents



This repo includes notes and code from Udememy course: 

[LLM Engineering: Master AI, Large Language Models & Agents](https://www.udemy.com/course/llm-engineering-master-ai-and-large-language-models/learn/lecture/46867711#overview)

See also [Github repo](https://github.com/ed-donner/llm_engineering/tree/main)


### Install
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
pip install -r requirements.txt
```


### Trying out Llama 3.2
Download [Ollama](https://ollama.com/download)
In terminal, run:  
```ollama run llama3.2```

And interact with Llama 3.2
Example
```
>>> I am trying to learn Spanish. I am a conmplete beginner. Please have a conversation with me to teach me Spanish
¡Hola! (Hello!) I'd be happy to help you learn Spanish. Don't worry if you make mistakes - it's all part of
the learning process.

Let's start with something simple. Can you tell me your name? ¿Cómo te llamas?

(Note: Don't worry about using English words, we can translate them later.)

>>> My name is Fabrice
¡Hola, Fabrice! (Hello, Fabrice!) My name is Leo.

Now, let's try to introduce ourselves a bit more. In Spanish, it's common to ask someone "¿Cómo estás?" which
means "How are you?"

So, I'll say: ¿Cómo estás, Fabrice?

(And don't forget, we're speaking in Spanish from now on.)

Can you respond with how you're doing today?

>>> I am doing well
Estoy muy bien también. (I'm very good too.) That's a common way to say "I'm fine" or "I'm okay".

Let's try something else. Can you ask me where I'm from? In Spanish, we use the word "origen" or "país" for
this.

For example: ¿De dónde eres?

(Note: "Dónde" is a common question that means "where", and "eres" is the second person singular form of the
verb "ser", which means "to be".)
...
>>>/bye
```

Ollama has a catalog of models that can be tried for Embedding, Text and Vision - accessible at: https://ollama.com/search


Trying another model
```
ollama run deepseek-r1:7b
>>> hola, como estas?
<think>
Okay, someone just said "hola" which means hello in Spanish. I should respond politely.

They also asked "como estas?" which is "how are you?" in Spanish. I'll need to answer that.

I should keep it friendly and maybe add a question about them.

So, something like "Estoy bien, gracias. ¿Cómo estás? ¿Cuál has hecho esta noche?"

That sounds natural.
</think>

¡Hola! Estoy bien, gracias. ¿Cómo estás? ¿Cuál has hecho esta noche?
```

This course's journey towards mastery LLM will focus on:
- Frontier models with UIs, Agentization and Multi-modality
- Open source with Hugging Face
- Selecting LLMs and code generation
- RAG and questions and answering
- Fine tuning a frontier model
- Fine tuning an Open Source model
- Fully autnomous agentic ai solutions, with 7 agents collaborating (Scan internet for things, sned push notifications,...)
