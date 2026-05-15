# Contributing to AuraBrain Pro

Thank you for your interest in AuraBrain Pro!

## Model Contributions

We welcome:
- **System prompt improvements** — better prompts make the model smarter
- **Modelfile optimisations** — parameter tuning for better outputs
- **Benchmark results** — share your eval results
- **Bug reports** — model behaviour issues

We do NOT accept:
- Model weight modifications (use Qwen2 fine-tuning tools)
- Re-quantised variants (we standardise on Q4_K_M)
- Proprietary model merges

## How to Contribute

1. Fork this repository
2. Create a feature branch (`git checkout -b feature/better-prompt`)
3. Test with `ollama create aurabrain-pro-test -f Modelfile`
4. Submit a pull request

## Testing

```bash
# Create test model from your modified Modelfile
ollama create aurabrain-pro-test -f Modelfile

# Test tool-calling
curl -X POST http://localhost:11434/v1/chat/completions \
  -H "Content-Type: application/json" \
  -d '{"model":"aurabrain-pro-test","messages":[{"role":"user","content":"What is 2+2?"}]}'

# Test with brain server
aurabrain serve &
# Open https://aurabrain.io/app
```

## License

By contributing, you agree that your contributions will be licensed under the
MIT License (code) and Qwen RESEARCH LICENSE (model weights).