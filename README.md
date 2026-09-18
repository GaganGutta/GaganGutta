# Hi, I'm Gagan Gutta 👋

**Math, CS & AI @ NYU Courant** · Building applied ML systems and the occasional product around them.

**[gagan.cc](https://gagan.cc)** · gg3367@nyu.edu

---

## About Me

I build AI systems, mostly applied machine learning and computer vision, sometimes for research, sometimes for startups. I'm drawn to problems where the gap between state-of-the-art tech and real-world deployment is still wide.

Most recently a research assistant at **Jordaan Labs, UMass Amherst**, where I built HerringNet, a CV model for automated river herring population monitoring, presented at MassURC 2026 with a methods paper in preparation. Lately I've been deep in systems work, writing a durable job queue from scratch in C++20.

---

## Featured Projects

### baton
A durable job queue written from scratch in C++20 — single binary, no dependencies, speaks the Redis wire protocol. Group commit batches concurrent fsyncs behind one `fdatasync`, sustaining 14,148 fsynced enqueues/s at 64 connections against Beanstalkd's 743 at equal durability. Correctness is proven, not claimed: a simulated filesystem that tears and drops un-synced writes, kill -9 chaos rounds checked by an independent model replaying the server's own log, and a mutation harness that breaks 29 invariants one at a time. Recovers 1.24M queued jobs in 0.82s after a crash. Ships with a Python SDK handling leases, heartbeats, retries, and graceful shutdown.

`C++20` `CMake` `Docker` `Python` `GoogleTest` `libFuzzer`

### HerringNet
A two-stage deep learning pipeline for automated fish detection and counting from underwater camera traps. Uses YOLOv12x (pretrained on 1.9M fish images) + frame-residence-rate methodology to eliminate double-counting, reaching 94% precision / 91% recall on a held-out set. Replaced 85% of manual review across 320+ hours of camera-trap footage, deployed behind FastAPI so 12 non-technical researchers use it as their primary workflow. Presented at MassURC 2026.

`Python` `PyTorch` `YOLOv12` `OpenCV` `SAHI` `FastAPI`

### Playable Neural Game Engine
Train a causal transformer over VQ-VAE tokens on VizDoom frames, then throw the game engine away and drive the model with a keyboard. Scaled 2M/8M/26M parameters on a pre-registered 2.9B-token budget; the 26M model closes 83% of the gap between copy-last-frame and the tokenizer's ceiling. KV caching plus a MaskGIT decode path that shares weights with the raster path cut frame time from 1.54s to 28ms (35.47 fps), making it playable on a laptop CPU with no GPU at inference.

`Python` `PyTorch` `CUDA` `Transformers` `Docker`

### attention-emergence
Reproduction and extension of "Emergent Capabilities Arise Randomly from Learning Sparse Attention Patterns" (NYU). Re-implements the paper's synthetic testbeds from scratch in PyTorch, reproduces its core results on a laptop CPU, and extends the analysis with an original early-warning predictor for emergence timing.

`Python` `PyTorch`

### ContextGrade
Co-founded and lead engineering for a B2B brand safety platform: LLM-driven analysis over 40+ risk signals for ad holding companies, driving enterprise pilots with Omnicom and IPG. Schema-constrained prompt pipelines across scraping infrastructure, LLM APIs, and a Supabase backend analyze 12,000+ domains and 85,000+ pages at 420ms median latency.

`Python` `FastAPI` `TypeScript` `LLM APIs` `PostgreSQL/Supabase`

### Personal Website
Source for [gagan.cc](https://gagan.cc) — my portfolio and project showcase.

`HTML`

---

## Tech Stack

**Languages:** C++ (C++20) · Python · JavaScript · TypeScript · SQL

**Systems:** CMake · Concurrency · Write-ahead logging · Network protocols · ASan/TSan/UBSan · Fuzzing

**ML/AI:** PyTorch · YOLOv8/v12 · OpenCV · SAHI · Gradio · Pydantic

**Web:** Next.js · React · Node.js

**Tools:** Git · Linux · Docker

---

## Find Me

Portfolio: [gagan.cc](https://gagan.cc) | LinkedIn: [linkedin.com/in/gagangutta](https://linkedin.com/in/gagangutta) | Email: gg3367@nyu.edu
