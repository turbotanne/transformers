# Streaming Config

- Model: `distil-whisper-large-v3`
- Chunk overlap: 1.5s
- Post-processor: regex cleanup + spaCy NER
- Output bus: Kafka topic `sona8.voice.events`
- Retry policy: exponential backoff, max 3 tries