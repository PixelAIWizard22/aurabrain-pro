# 🧠 AuraBrain Pro

**3B parameter LLM with tool-calling. Runs locally. Zero cloud.**

[Q4_K_M] [Ollama] [Tool-Calling] [Brain-Enhanced]

---

## Why AuraBrain Pro?

Most "small" models can't do anything useful alone. AuraBrain Pro is different:

1. **Tool-calling native** — calls functions, APIs, and brain endpoints out of the box
2. **Brain-enhanced** — connects to AuraBrain memory server for persistent knowledge
3. **8.5MB server** — the smallest full-featured LLM inference engine
4. **Zero cloud** — runs on your machine, your internet for web search
5. **Q4_K_M quantised** — 1.9GB download, runs on any laptop

**Small model + web search + brain memory beats big model alone.**

---

## Quick Start

```bash
# Option 1: Pull from Ollama Registry
ollama pull aurabrain-pro
ollama run aurabrain-pro

# Option 2: Install from GitHub Release
# 1. Download the GGUF from Releases tab
# 2. Create from Modelfile:
ollama create aurabrain-pro -f Modelfile
ollama run aurabrain-pro

# Option 3: With Brain Server (full experience)
pip install aurabrain
aurabrain serve
# Then open https://aurabrain.io/app
```

## Model Specs

| Property | Value |
|----------|-------|
| Parameters | 3B |
| Quantisation | Q4_K_M |
| Download size | 1.9GB |
| RAM usage (mmap) | ~2.4GB |
| Context length | 4096 |
| Tool-calling | Yes |
| Base model | Qwen2 |
| License | Qwen RESEARCH LICENSE (non-commercial) |

## Model Family

| Model | Params | Size | Use Case |
|-------|--------|------|----------|
| aurabrain-micro | 0.5B | 397MB | Phone, IoT, embedded |
| aurabrain-light | 1.5B | 986MB | Tablet, lightweight tasks |
| **aurabrain-pro** | **3B** | **1.9GB** | **Full tool-calling + brain** |

## Brain-Enhanced Inference

AuraBrain Pro isn't just a chatbot. Connected to the brain server, it:

- **Recalls** — searches 892+ knowledge atoms before answering
- **Stores** — saves new facts, lessons, and decisions as brain atoms
- **Verifies** — cross-checks claims against verified knowledge (CoVe + SAVeR)
- **Self-corrects** — detects fabrication and replaces with facts
- **Searches the web** — Wikipedia + Wikidata, free, on your internet

```bash
# Run with full brain stack
ollama serve aurabrain-pro &
aurabrain serve
# Open https://aurabrain.io/app for Brain Search + Notepad
```

## Files

- `aurabrain-pro-q4_k_m.gguf` — The model weights (1.9GB)
- `Modelfile` — Ollama configuration with system prompt and parameters
- `aurabrain-micro-q4_k_m.gguf` — 0.5B model (397MB, Releases)
- `aurabrain-light-q4_k_m.gguf` — 1.5B model (986MB, Releases)

## License

- **Code & configuration**: MIT License — see [LICENSE](LICENSE)
- **Model weights**: Qwen RESEARCH LICENSE — non-commercial use only
  - For commercial licensing, contact [Alibaba Cloud](https://qwenlm.github.io/)

## Links

- 🧠 [AuraBrain](https://aurabrain.io) — The brain is the product
- 📖 [Architecture](https://aurabrain.io) — How it works
- 🔄 [Changelog](CHANGELOG.md) — Version history
- 🤝 [Contributing](CONTRIBUTING.md) — How to help