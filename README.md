### Sachin Chhaya

CS + ORIE at Cornell. Mostly interested in the places where systems work and quant finance meet: making things correct under failure, and making things fast enough to matter.

I learn things by building them from the paper up, so most of what's here started as "I don't actually understand how X works."

**Things I've built**

- **[raft](https://github.com/sachhayaKO/raft)** (Go): Raft consensus from scratch, with a teammate. Leader election, log replication, crash persistence, a replicated KV store on top, and gRPC between nodes. Passes `go test -race`. There's a small browser demo where you can kill nodes and watch the cluster re-elect and catch back up. The [DEVLOG](https://github.com/sachhayaKO/raft/blob/main/DEVLOG.md) is pretty much a record of me learning Go along the way.

- **[vol-surface-agent](https://github.com/sachhayaKO/vol-surface-agent)** (Python): pulls a live options chain, solves for implied vol and greeks, checks them against realized vol (close-to-close and Parkinson), and answers questions like "is AAPL vol rich right now?" using recent 10-K and earnings text for context. It's a custom LangGraph state machine, not the prebuilt agent. It scores 29/30 on a golden-question eval suite, and the [eval writeup](https://github.com/sachhayaKO/vol-surface-agent/blob/main/docs/EVALS.md) covers the bugs that testing caught.

- **[ledger](https://github.com/sachhayaKO/ledger)** (C++): an event-driven backtesting engine (data → strategy → portfolio → execution → metrics), meant for parameter sweeps that would be painfully slow in Python. Still early.

- **[The Workflow Gambit](https://github.com/sachhayaKO/Point72Hackathon)** (Cubist Hackathon 2026): nine of us built chess engines with the same model and the same UCI spec, but each person used a different AI workflow, and then we ran them all through one eval harness. I did the "standard prompting" baseline, which was meant to show what a normal engineer gets by just iterating with the model.

Outside of those: a Dockerized Flask habit-tracker API running on a GCP VM, a CRISPR-Cas9 target-site finder, and some image deblurring with Fourier methods.

**Lately**: distributed systems, options pricing, and figuring out which parts of AI-assisted coding actually help.

**Tools I reach for**: Python, Go, C++, SQL, Docker, gRPC, LangGraph, pandas/numpy.
