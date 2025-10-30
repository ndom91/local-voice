# HA Local Voice Setup

This is my local voice setup deployed via Docker. The containers here will get you speech-to-text (STT), text-to-speech (TTS) and custom wake-word functionality.

## Containers

1. `wyoming-whisper-cpp` - Wyoming server for the whisper port to C++ (https://github.com/ggml-org/whisper.cpp)
2. `rhasspy/wyoming-piper:latest` - Piper TTS (https://github.com/home-assistant/addons/blob/master/piper/DOCS.md)
3. `rhasppy/wyoming-microwakeword` - Opensource wake word library for detecting wake words on low-power devices (https://github.com/OHF-Voice/micro-wake-word)

## Getting Started

```bash
docker compose up -d
```

## License

MIT
