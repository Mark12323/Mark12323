<div align="center">

# Hey, I'm Mark

<a href="https://github.com/Mark12323/GemmaLingua">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=18&pause=1200&color=58A6FF&center=true&vCenter=true&width=640&lines=Fine-tuning+LLMs+for+Nigerian+languages;Java+orchestration+%C3%97+PyTorch+training;Building+things+to+understand+them" alt="Typing intro" />
</a>

AI engineer & Java developer · Port Harcourt, Nigeria · Founder of **Spavecraft**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/odike-mark-chinedu-51a0bb23a)
[![X](https://img.shields.io/badge/@mark__odike-000000?style=flat-square&logo=x&logoColor=white)](https://x.com/mark_odike)
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=flat-square&logo=youtube&logoColor=white)](https://www.youtube.com/@em_demiurge4868)
![Open to roles](https://img.shields.io/badge/open%20to-AI%20%2F%20backend%20roles-2ea44f?style=flat-square)

</div>

---

Most of my time goes into one question: **why do language models still struggle with the languages people around me actually speak?** I've been fine-tuning them on Igbo, and building tooling to make that repeatable for other Nigerian languages.

I also like knowing how things work underneath. When something feels like magic — tensors, memory allocation — I usually end up writing my own version just to understand it.

## Now: GemmaLingua

**[GemmaLingua](https://github.com/Mark12323/GemmaLingua)** teaches Google's Gemma 4 to read and write Igbo. Training is Python (PyTorch, Hugging Face, QLoRA on a single GPU); the pipeline around it is a Java orchestrator I wrote.

```mermaid
flowchart LR
    cfg[/"Language config<br/>(Igbo → Yoruba / Hausa<br/>is a 4-line change)"/] --> val

    subgraph orch["Java orchestrator"]
        direction LR
        val["Validate data"] --> s1["Stage 1<br/>Continued pretraining<br/>~66M Igbo tokens"]
        s1 --> s2["Stage 2<br/>EN → IG translation"]
        s2 --> s3["Stage 3<br/>Masked-word infilling"]
        s3 --> exp["Export model"]
    end

    exp --> eval{{"Eval vs base Gemma 4<br/>on held-out Igbo"}}
```

**Status:** training pipeline done · evaluation harness in progress — comparing fine-tuned vs. base on unseen Igbo text so the improvement is measured, not claimed.

<!-- When the eval lands, replace the line above with a small results table, e.g.
| Model | Perplexity ↓ | chrF (EN→IG) ↑ | Infill accuracy ↑ |
|---|---|---|---|
| Gemma 4 (base) | … | … | … |
| GemmaLingua | … | … | … |
-->

## Shipped

| Product | What it does |
|---|---|
| [**QuietInflame**](https://quietinflame.com) · [![Live](https://img.shields.io/badge/live-quietinflame.com-2ea44f?style=flat-square)](https://quietinflame.com) | Healthcare navigation platform for people living with chronic inflammation. A provider directory built on official US registries (NPPES & CMS), plain-language condition guides, a personal care organizer and an AI Navigator assistant. |
| [**Craftviewpro**](https://github.com/Mark12323/Craftviewpro) | Enterprise surveillance network backend |

## Built to understand

| Project | What it is | What I learned |
|---|---|---|
| [**JTensor**](https://github.com/Mark12323/JTensor) | Dependency-free tensor library in plain Java | Strides, views, and why a reshape doesn't have to copy |
| [**Java-Arena**](https://github.com/Mark12323/Java-Arena) | Bump-pointer memory arena | Detecting use-after-reset — the hardest part to get right |

## Other work

| Project | Description |
|---|---|
| [debug.io](https://github.com/Mark12323/debug.io) | Debugging assistant built on Gemini |
| [Sent_analysis](https://github.com/Mark12323/Sent_analysis) | Sentiment analysis in Java |
| [ent_manager](https://github.com/Mark12323/ent_manager) | Enterprise management software |

<sub>Much of my client work at Spavecraft is private and doesn't show up here.</sub>

## Toolbox

<p>
  <img src="https://skillicons.dev/icons?i=java,py,pytorch,maven,linux,bash,git&theme=dark" alt="Java, Python, PyTorch, Maven, Linux, Bash, Git" />
</p>

![Hugging Face](https://img.shields.io/badge/Transformers%20·%20PEFT%20·%20TRL-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![JUnit](https://img.shields.io/badge/JUnit-25A162?style=flat-square&logo=junit5&logoColor=white)
![QLoRA](https://img.shields.io/badge/QLoRA-single--GPU%20fine--tuning-6f42c1?style=flat-square)

## Activity

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api?username=Mark12323&show_icons=true&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=58a6ff&text_color=c9d1d9" />
    <img height="165" src="https://github-readme-stats.vercel.app/api?username=Mark12323&show_icons=true&hide_border=true" alt="GitHub stats" />
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=Mark12323&layout=compact&hide_border=true&bg_color=0d1117&title_color=58a6ff&text_color=c9d1d9" />
    <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Mark12323&layout=compact&hide_border=true" alt="Top languages" />
  </picture>

  <br/><br/>

  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Mark12323/Mark12323/output/github-snake-dark.svg" />
    <img src="https://raw.githubusercontent.com/Mark12323/Mark12323/output/github-snake.svg" alt="Contribution snake" />
  </picture>
</div>

---

<div align="center">
  <b>Working on NLP for African languages?</b> I'd love to hear from you — reach out on
  <a href="https://www.linkedin.com/in/odike-mark-chinedu-51a0bb23a">LinkedIn</a> or
  <a href="https://x.com/mark_odike">X</a>.
</div>
