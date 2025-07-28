<!--
Awesome‑LLM‑Reverse‑Engineering
A curated list of resources at the intersection of large language models (LLMs)
and reverse engineering / binary analysis.  PRs are welcome!
-->

# Awesome‑LLM‑Reverse‑Engineering

Large‑language models are rapidly reshaping low‑level program analysis.  
LLMs can now:

* recover **function names** & **variable types**
* **summarise** whole binaries
* **decompile** machine code back to C‑like source
* power vulnerability research & offensive security tooling

This list tracks tools, datasets, papers and learning resources.  
Long explanations stay in prose; tables use *≤ 3 columns* and short phrases.

---

## Table of Contents
- [Tools & Plugins](#️tools--plugins)
- [Datasets](#datasets)
- [Papers](#papers)
- [Tutorials & Courses](#tutorials--courses)
- [CTFs & Benchmarks](#ctfs--benchmarks)
- [Blogs & Write‑ups](#blogs--write‑ups)
- [Contributing](#contributing)
- [License](#license)
- [See Also](#see-also)

---

## Tools & Plugins
| Tool | Focus | Link |
|------|-------|------|
| **LLM4Decompile** | ASM→C decompilation | 🔗 [code](https://github.com/cascadium/LLM4Decompile)<br>![GitHub stars](https://img.shields.io/github/stars/albertan017/LLM4Decompile?style=social) |
| **CFADecLLM** | CFG‑aware decompiler | 🔗 [paper](https://arxiv.org/abs/2405.17963) |
| **WaDec** | WebAssembly → C | 🔗 [paper](https://arxiv.org/abs/2404.06145) |
| **DeGPT** | Decompiler refinement | 🔗 [paper](https://www.ndss-symposium.org/ndss-paper/de-gpt-optimizing-decompiler-output-with-llm/) |
| **SLaDe** | 200 M parameter decompiler | 🔗 [paper](https://arxiv.org/abs/2306.10604) |
| **LmPa** | Var‑name recovery | 🔗 [paper](https://arxiv.org/abs/2309.06871) |
| **Nova** | Assembly generation | 🔗 [paper](https://arxiv.org/abs/2312.06261) |
| **ReCopilot** | Binary‑analysis LLM | 🔗 [paper](https://arxiv.org/abs/2501.02513) |
| **ByteCodeLLM** | Python `.pyc` → .py | 🔗 [code](https://github.com/cyberark/ByteCodeLLM)<br>![GitHub stars](https://img.shields.io/github/stars/cyberark/ByteCodeLLM?style=social) |
| **GptHidra** | Explain functions (Ghidra) | 🔗 [code](https://github.com/evyatar9/GptHidra)<br>![GitHub stars](https://img.shields.io/github/stars/evyatar9/GptHidra?style=social) |
| **GhidraChatGPT** | Vuln finder (Ghidra) | 🔗 [code](https://github.com/likvidera/GhidraChatGPT)<br>![GitHub stars](https://img.shields.io/github/stars/likvidera/GhidraChatGPT?style=social) |
| **GhidrAssist / BinAssist** | Local LLaMA in Ghidra / BN | 🔗 [code](https://github.com/jasontang-ghidrassist/GhidrAssist)<br>![GitHub stars](https://img.shields.io/github/stars/jasontang-ghidrassist/GhidrAssist?style=social) |
| **Binary Ninja Sidekick** | AI index & insights | 🔗 [docs](https://sidekick.binary.ninja/) |
| **r2ai / decai** | AI‑assisted decompilation (Radare2) | 🔗 [code](https://github.com/radareorg/r2ai)<br>![GitHub stars](https://img.shields.io/github/stars/radareorg/r2ai?style=social) |
| **FuzzDriverGPT** | GPT‑based fuzz driver generator | 🔗 [code](https://github.com/occia/fuzzdrivergpt)<br>![GitHub stars](https://img.shields.io/github/stars/occia/fuzzdrivergpt?style=social) |
| **ReverserAI** | Offline BN plugin | 🔗 [code](https://github.com/reflare/ReverserAI)<br>![GitHub stars](https://img.shields.io/github/stars/reflare/ReverserAI?style=social) |
| **GPT‑WPRE** | Whole‑program summary | 🔗 [code](https://github.com/moyix/gpt-wpre)<br>![GitHub stars](https://img.shields.io/github/stars/moyix/gpt-wpre?style=social) |

---

## Datasets
| Dataset | Purpose | Link |
|---------|---------|------|
| **Decompile‑Eval** | Re‑compilability benchmark | 🔗 [repo](https://github.com/cascadium/Decompile-Eval)<br>![GitHub stars](https://img.shields.io/github/stars/cascadium/Decompile-Eval?style=social) |
| **DeBinVul** | 150 k vuln / safe samples | 🔗 [paper](https://arxiv.org/abs/2403.05366) |
| **WaDec** | WAT↔C pairs | 🔗 [paper](https://arxiv.org/abs/2404.06145) |
| **NYU CTF Bench** | 200 CTF tasks | 🔗 [repo](https://github.com/NYU-LLM-CTF/NYU_CTF_Bench)<br>![GitHub stars](https://img.shields.io/github/stars/NYU-LLM-CTF/NYU_CTF_Bench?style=social) |
| **ReCopilot set** | Data‑flow graphs | 🔗 [paper](https://arxiv.org/abs/2501.02513) |

---

## Papers
> *Chronological — newest first.*

| Year | Title (link) | Notes |
|------|--------------|-------|
| 2025 | **An Empirical Study on the Effectiveness of LLMs for Binary Code Understanding** | new benchmark 🔗 [2504.21803](https://arxiv.org/abs/2504.21803) |
| 2025 | **D‑LiFT: Improving LLM‑based Decompiler Backend via Code Quality‑driven Fine‑tuning** | RL‑guided backend, D‑Score metric 🔗 [2506.10125](https://arxiv.org/abs/2506.10125) |
| 2025 | **CFADecLLM** | CFG tokens boost accuracy 🔗 [2405.17963](https://arxiv.org/abs/2405.17963) |
| 2025 | **ReCopilot** | domain‑specific LLM 🔗 [2501.02513](https://arxiv.org/abs/2501.02513) |
| 2024 | **Exploring the Efficacy of GPT‑4 in Binary RE** | GPT‑4 limitations 🔗 [2406.06637](https://arxiv.org/abs/2406.06637) |
| 2024 | **LLM4Decompile** | end‑to‑end model 🔗 [2403.06795](https://arxiv.org/abs/2403.06795) |
| 2024 | **DeGPT** | multi‑role prompting 🔗 [NDSS ’24](https://www.ndss-symposium.org/ndss-paper/de-gpt-optimizing-decompiler-output-with-llm/) |
| 2024 | **DeBinVul** | vuln dataset 🔗 [2403.05366](https://arxiv.org/abs/2403.05366) |
| 2024 | **WaDec** | WebAssembly decompiler 🔗 [2404.06145](https://arxiv.org/abs/2404.06145) |
| 2024 | **FuzzGPT: Crafting Unusual Programs for Fuzzing Deep Learning Libraries** | LLM‑driven fuzzing 🔗 [2304.02014](https://arxiv.org/abs/2304.02014) |
| 2024 | **LLM‑Guided Protocol Fuzzing** | NDSS ’24 protocol fuzzer 🔗 [PDF](https://abhikrc.com/pdf/NDSS24.pdf) |
| 2023 | **SLaDe** | small model, big gains 🔗 [2306.10604](https://arxiv.org/abs/2306.10604) |
| 2023 | **LmPa** | var‑name recovery 🔗 [2309.06871](https://arxiv.org/abs/2309.06871) |
| 2023 | **Nova** | hierarchical assembly model 🔗 [2312.06261](https://arxiv.org/abs/2312.06261) |
| 2023 | **Refining Decompiled C with LLMs** | 2‑stage pipeline 🔗 [2307.04118](https://arxiv.org/abs/2307.04118) |

---

## Tutorials & Courses
- **Applied AI/LLM for Android APK RE** – 16 h Ringzer0 workshop (Jadx + Ghidra MCP).  
- **Automating Reverse Engineering with AI/ML & LLMs** – 4‑day Recon training (Blackfyre, BinaryRank).

---

## CTFs & Benchmarks
- **NYU CTF Bench** – 200 Jeopardy tasks + tool‑calling framework.  
- **Flare‑On** – annual RE contest; good real‑world testbed for LLM tools.

---

## Blogs & Write‑ups
- *Reverse Engineering is Not Hard with LLM Tools* – Reflare overview of Sidekick, ReverserAI, LLM4Decompile.  
- *Supercharging Ghidra with Local LLMs* – step‑by‑step GhidraMCP guide.  
- *AI‑Assisted Decompilation in Radare2* – `decai` + `r2ai` walk‑through.  
- *GhidrAssist in Action* – offline Mixtral / LLaMA chat inside Ghidra.  

---

## Contributing
1. Add a short entry (≤ 3 columns) **+** paragraph summary *with a working link*.  
2. Open a pull‑request — we merge fast! 🏎️

---

## License
MIT

---

## 🔗 See Also
- [Awesome‑Reverse‑Engineering](https://github.com/wtsxDev/reverse-engineering)
- [Awesome‑Binary‑Analysis](https://github.com/enaqx/awesome-binary-analysis)
- [Awesome‑Large‑Language‑Models](https://github.com/huggingface/awesome-large-language-models)
- [Awesome‑AI‑Cybersecurity](https://github.com/Artificial-Engineering/awesome-ai-cybersecurity)
