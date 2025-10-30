# HA Local Voice Setup

This is my local voice setup deployed via Docker. The containers here will get you speech-to-text (STT), text-to-speech (TTS) and custom wake-word functionality.

## Containers

1. `wyoming-whisper-cpp`
    - Wyoming server for the whisper port to C++
    - https://github.com/ggml-org/whisper.cpp
3. `rhasspy/wyoming-piper:latest`
    - Piper TTS
    - https://github.com/home-assistant/addons/blob/master/piper/DOCS.md
5. `rhasppy/wyoming-microwakeword`
    - Opensource wake word library for detecting wake words on low-power devices
    - https://github.com/OHF-Voice/micro-wake-word

## Getting Started

```bash
docker compose up -d
```

In Homeassistant, you will then need to add each service individually. They can each be added by the following steps:

1. Settings -> Integrations -> Add new Integration
2. Select "Wyoming"
3. Enter the host IP address where you are running these containers
4. Each service is running at its own port
    - Piper: `10200`
    - Whisper: `10300`
    - microWakeWord: `10400`

## License

MIT
