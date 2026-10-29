# Hey, I'm Mark

I'm an AI engineer and Java developer from Port Harcourt, Nigeria, and I run a small company called Spavecraft.

Most of my time right now goes into one question: why do language models still struggle with the languages people around me actually speak? So I've been fine-tuning them on Igbo, and building the tooling to make that repeatable for other Nigerian languages.

I also like knowing how things work underneath. When something feels like magic, like tensors or memory allocation, I usually end up writing my own version just to understand it.

## What I'm working on

**[GemmaLingua](https://github.com/Mark12323/GemmaLingua)** is my main project. It's a pipeline for teaching Google's Gemma 4 model Igbo. Training happens in three stages that build on each other. First the model reads about 66 million tokens of plain Igbo text. Then it learns English-to-Igbo translation. Finally it practises filling in missing words in Igbo sentences.

The training itself is Python (PyTorch, Hugging Face, QLoRA so it fits on a single GPU), but the whole pipeline is run by a Java orchestrator I wrote. It handles data validation, each training stage, and exporting the model. Everything language-specific lives in one config file, so pointing it at Yoruba or Hausa should be a four-line change.

Right now I'm building the evaluation side: comparing the fine-tuned model against the base model on Igbo text it has never seen, so I can say with real numbers whether it actually got better.

## Other things I've built

[JTensor](https://github.com/Mark12323/JTensor) is a small tensor library in plain Java with no dependencies. I wrote it to properly understand strides, views, and why reshaping a tensor doesn't have to copy anything.

[Java-Arena](https://github.com/Mark12323/Java-Arena) is a bump-pointer memory arena. It also catches you if you try to use memory after the arena has been reset, which turned out to be the most interesting part to get right.

[debug.io](https://github.com/Mark12323/debug.io) is a debugging assistant built on Gemini, and [Sent_analysis](https://github.com/Mark12323/Sent_analysis) is a sentiment analysis project in Java.

On the backend side there's [Craftviewpro](https://github.com/Mark12323/Craftviewpro), an enterprise surveillance network, and [ent_manager](https://github.com/Mark12323/ent_manager), enterprise management software. A lot of my client work at Spavecraft is private, so it doesn't show up here.

## Tools I use

Java and Python mostly. PyTorch, Hugging Face Transformers, PEFT and TRL for training, Maven and JUnit on the Java side, and Linux for everything.

## Say hi

I'm open to AI engineering and backend roles, and I'd love to hear from anyone working on NLP for African languages.

You can find me on [LinkedIn](https://www.linkedin.com/in/odike-mark-chinedu-51a0bb23a), [X](https://x.com/mark_odike), or [YouTube](https://www.youtube.com/@em_demiurge4868).
