# SONA8 Voice Agent Stack

| Component | Model | Notes |
|-----------|-------|-------|
| ASR       | Whisper Medium | Source of truth transcripts |
| LLM       | `Qwen2.5-7B-Instruct` | Lightweight reasoning agent |
| Sentiment | `distilbert-base-uncased-emotion` | Real-time score per utterance |
| Summaries | `Llama-3-8B` via transformers pipeline | Generate action items |

Next actions:
- Build HF pipeline config for streaming chunks
- Add guardrails to reject PII before LLM stage
- Benchmark end-to-end latency < 1.2s per sentence