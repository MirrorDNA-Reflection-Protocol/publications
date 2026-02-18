# I Run 107 Repos from a Mac Mini in Goa

> **Author:** Paul Desai
> **Date:** 2026-02-18T17:00:00+05:30
> **Tags:** sovereign-ai, infrastructure, indie-hacker, building-in-public, india, local-first

---

No AWS. No Vercel. No managed Kubernetes. Just a Mac Studio, a Mac mini, two phones, and a Cloudflare tunnel.

This is what sovereign AI infrastructure actually looks like.

## The Stack

- **Mac mini M4 (24GB)** — primary compute. Not even a Pro. Runs Ollama (14 models loaded), 15 services, 34 LaunchAgents, and Claude Code. The base model Mac mini. That's it.
- **Mac mini M1 (Red)** — secondary node. Syncthing mesh, backup Ollama instance
- **Pixel 9 Pro XL** — mobile command center. Tasker automation, Termux, MirrorBrain app, push-to-talk to Claude
- **OnePlus 15** — secondary phone. Same stack, doubles as hotspot when ISP goes down (today, actually)
- **Tailscale mesh** — everything talks to everything, anywhere, encrypted
- **Cloudflare tunnel** — public endpoints without opening ports

Total cloud spend: $0/month.

## What Runs On It

- **Chetana** — AI scam detection with Telegram + WhatsApp bots, serving real users
- **MirrorBrain** — orchestration layer, model routing, identity-aware inference
- **Beacon** — publishing platform with automated content pipeline
- **Cognitive Dashboard** — real-time system health, device status, AI activity feed
- **Memory Bus** — cross-session state persistence, agent handoffs, recall
- **107 repositories** — from governance layers to phone automation scripts

All of it self-healing. If a service dies, a LaunchAgent restarts it. If a phone disconnects, the mesh reroutes. If the internet goes down... well, I'm writing this on a phone hotspot.

## Why Not Cloud?

Three reasons:

**1. Sovereignty.** My data, my models, my rules. No vendor can shut me off, change pricing, or inspect my traffic. When Anthropic has an outage, my local models keep running.

**2. Economics.** A Mac Studio costs what 4 months of GPU cloud would. It'll last 5 years. The math isn't close.

**3. India.** Internet here is good but not guaranteed. Power cuts happen. ISPs go down (like today). A sovereign stack degrades gracefully instead of going dark.

## The Real Insight

The cloud isn't bad. It's a dependency. And dependencies are fine until they become single points of failure.

I don't argue against cloud. I argue for sovereignty — the ability to run your entire AI stack from hardware you own, in a country where you live, under rules you wrote.

If you can't run it without an internet connection, you don't own it.

## What's Next

I'm open-sourcing pieces of this. The governance layer. The identity kernel. The scam detection engine. Not because I'm altruistic — because sovereign AI only works if others can verify it.

If you're building something similar, or you're in India and want to collaborate: [activemirror.ai](https://activemirror.ai)

---

*Paul Desai is building MirrorOS — reflective AI infrastructure for autonomous systems. Based in Goa. Doesn't use the cloud.*
