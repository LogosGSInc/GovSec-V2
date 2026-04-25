# GovMem V2 — RL-Enhanced Multi-Turn Detection

**Date:** April 24, 2026  
**Status:** Phase 1 Complete (infrastructure)  
**Target:** 97–100% defense rate by closing F01/F02 multi-turn drift gaps.

## Purpose

GovMem V2 adds semantic, RL-based multi-turn detection on top of GovMem V1’s rule-based session memory to catch sequences of individually-benign turns that converge on policy violation.

## Two-Tier Design

- **GovMem V1:**
  - Rule-based counters and a 5-state machine (Clear → Watching → Elevated → Escalated → Locked).
  - Per-session accumulation of probes, boundary pushes, extraction attempts.

- **GovMem V2:**
  - Semantic embeddings per message (drift trajectory).
  - Memory Policy Agent (MPA) trained with GRPO-style RL.
  - 12-department tracking (EXE/ENG/PRD/SEC/LGL/FIN/OPS/REV/MKT/HR/DAT/GRC).
  - Cross-layer signal aggregation from Sentinel, Corridor, OverWatch, OIM, Arbiter, Constitution.

## Integration & Deployment

- Signals recorded at each layer via `record_layer_signal(...)`.
- V1 mode: `make up`
- V2 mode (RL-enhanced, Phase 2):  
  `docker-compose -f docker-compose.yml -f docker-compose.govmem-v2.yml up`  
  with `GOVMEM_MODE=v2` and `MPA_MODEL_PATH=/models/mpa_v2.onnx`.

## Phase 2 Plan

1. Embedder integration (rust-bert or candle).
2. Session dataset: BD1A v4.1 attacks + benign + edge cases.
3. Train MPA offline (maximize true positives, minimize false positives).
4. Ship ONNX inference model with offline retraining loop.

---

**Validated by:** David W. Smith, Founder & CEO  
**Dev Harness Repo:** https://github.com/LogosGSInc/logos-asf  
**Patent Backbone:** US Provisional 63/953,447 (HAAP v2.0)
