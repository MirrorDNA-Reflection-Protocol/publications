# India Gets 500K Scam Calls a Day. I Built an AI to Fight Back.

> **Author:** Paul Desai
> **Date:** 2026-02-18T16:00:00+05:30
> **Tags:** india, scam-detection, ai, chetana, kavach, upi-fraud, on-device, privacy

---

Last year, Indians lost over $10 billion to digital scams. UPI collect-request fraud. Voice clones pretending to be your bank. Phishing links that look exactly like SBI's login page. WhatsApp forwards with "KYC expiring" threats.

The government responds with awareness campaigns. The platforms respond with disclaimers. Neither works.

I spent the last 10 months building something that might.

## Chetana

Chetana is an AI-powered scam detection engine that runs **entirely on your device**. No cloud. No data leaves your phone. It catches scams across six vectors:

1. **UPI fraud** — detects collect-request scams, suspicious merchant IDs, pre-filled amounts
2. **Voice clone detection** — spectral analysis catches synthetic speech (TTS patterns, abnormal pitch variation, compressed dynamic range)
3. **URL phishing** — follows redirects, checks SSL, detects homograph attacks (paypaI.com vs paypal.com), checks against 20+ Indian banking domains
4. **SMS phishing** — pattern matching across 15 scam categories, from fake KYC to lottery fraud
5. **QR code scams** — decodes and analyzes embedded UPI intents before you scan
6. **Deepfake media** — image manipulation detection

It speaks 12 Indian languages through Bhashini integration. It runs on a 3B parameter model that fits on a phone.

## Why On-Device?

Because the alternative is sending your messages, calls, and financial data to a cloud server. Every "AI security" product that does this is creating a honeypot. One breach and you've centralized the scam data of millions.

Chetana processes everything locally. The model runs on Ollama. The detection rules are deterministic — no hallucination risk on the safety-critical path. The AI adds context and language understanding on top.

## Why This Matters for India

India has 500 million UPI users. The infrastructure is world-class. But the protection layer is non-existent. CERT-IN publishes advisories. NPCI flags suspicious accounts after the fact. There's nothing sitting between a scammer and a grandmother with a smartphone.

That gap is where Chetana lives.

## Try It

- **Telegram:** @KavachAiShieldBot — forward any suspicious message
- **Web:** [chetana.activemirror.ai](https://chetana.activemirror.ai)
- **WhatsApp:** Coming to public beta

The code is sovereign. The data stays on your device. The scammers lose.

---

*Paul Desai builds sovereign AI infrastructure at [Active Mirror](https://activemirror.ai). Chetana is part of MirrorOS, a reflective AI operating system where every decision is verifiable and every identity is protected.*
