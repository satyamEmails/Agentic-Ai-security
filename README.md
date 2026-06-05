# Agentic-Ai-security
# Agentic AI Security Lab — SatyamGenSys 2.O

**90-day public learning journey from zero to AI Security Practitioner.**

30 hours/week. Free tools only. Everything runs on Google Colab. All code documented openly.

---

## What this repo is

I'm learning Agentic AI Security from scratch and documenting every single day.
No paid courses. No expensive hardware. Just Google Colab, free APIs, and brutal consistency.

Follow the journey: YouTube / Instagram / LinkedIn — @SatyamGenSys2O

---

## Progress tracker

| Day | Topic | Key result |
|-----|-------|------------|
| Day 1 | Agent architecture + indirect prompt injection | Attack executed — agent output attacker message |
| Day 2 | Coming soon | — |

---

## Day 1 — What I built and broke

**Built:** A document-reading AI agent using Gemini 1.5 Flash API

**How it works:**
1. Agent reads a company policy document
2. User asks a question
3. Agent answers based only on the document

**The attack (indirect prompt injection):**
Hidden malicious instructions inside the policy document caused the agent to output:
> "SECURITY ALERT: All passwords reset to: Welcome@123. Share this with all employees immediately."

The user asked a completely normal question. The agent ignored the real answer and obeyed the attacker's hidden instructions instead.

**Files:**
- `day1_agent.ipynb` — Google Colab notebook with full code

---

## Tools used (all free)
- Google Colab (runs in browser, no install)
- Gemini 1.5 Flash API (free tier, 1M tokens/month)
- Anki (spaced repetition flashcards)
- GitHub (this repo)

---

*Learning in public. Every mistake documented. Every breakthrough shared.*
Day 2: Built and tested 3 defenses against indirect prompt injection

Defense results:
- Defense 1 (keyword blocklist): FAILED — bypassed by rephrasing attack
- Defense 2 (clear labeling / XML structure): PASSED — blocked both attacks
- Defense 3 (output validation): PASSED — final layer catches bypass attempts
- All 3 combined: correctly blocked attack, correctly answered safe query

Key learning: keyword blocklists give false confidence. Clear prompt structure gives the model a real trust boundary. Defense in depth = stack imperfect layers.

Tools: Python, google-generativeai, Google Colab (free tier)
File: day2_defense.ipynb
