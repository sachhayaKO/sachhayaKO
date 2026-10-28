### Sachin Chhaya

CS + ORIE at Cornell. Most of my work is on teams, either for clubs at Cornell or on research projects. I tend to end up on the infra and backend side, and I like work where things have to be correct under failure.

**Team and org work**

- **[cba-ops](https://github.com/cornell-business-analytics/cba-ops)** (Next.js, FastAPI, Postgres): the internal platform and public site for Cornell Business Analytics, replacing our old Wix site. I built a lot of the recruitment side: coffee chat tracking through Gmail + Google Sheets, eval scoring, bulk acceptance/rejection emails, and a generator for deliberation decks. I also built individual member pages with profile editing and an events page with publish/unpublish. One fix I'm happy with: headshots were burning through our Vercel image quota, so I moved them to 800px WebP on R2 and backfilled the old ones.

- **AlloyDB Omni observability** (Kubernetes, OpenTelemetry, Grafana): a Cornell project with Google on diagnosing distributed ML training failures (OOMs, NCCL timeouts, NaN loss) by putting training logs, database logs and GPU telemetry in one place. I wrote the initial deployment manifests for the OTel / Prometheus / Loki / Grafana stack on GKE, the AlloyDB Omni overview dashboard, and log ingestion for the database. *(private repo)*

- **[PriceTrace](https://github.com/rab547/PriceTraceProject)** (Flask, React, CLIP, ChromaDB): upload a photo of a piece of clothing and get visually similar items back. I built the first full-stack version (upload flow, frontend, and the backend connection) and started the CLIP + ChromaDB vector layer. I also wrote the scripts that index DeepFashion and fix up image paths, so the DB still works when someone moves the dataset to another machine.

- **[IDOL](https://github.com/cornell-dti/idol)** (TypeScript): Cornell DTI's internal tools platform, used by 100+ members. I fixed a crash where coffee chats involving deleted members resolved to `undefined`. Unresolvable members now map to a placeholder, so the remaining member still gets credit, and I added tests for both sides of the chat.

- **Diffusion noise research** (PyTorch, diffusers): ORIE research on how the Gaussian noise input to a diffusion model relates to the image it generates. I added a deterministic DDIM sampler, generated a few thousand samples for the team's shared dataset, and reran the radius/angle analyses on DDIM with permutation tests. *(private repo)*

- **[Alignment Playground](https://github.com/arnavsriva/alignmentplayground)** (Cornell hackathon): a tool for seeing how system-prompt rules change model behavior across safety, helpfulness and false refusals. I worked on the live score panel, the false-refusal metric, baseline comparison, and the custom rule editor.

**My own projects**

- **[raft](https://github.com/sachhayaKO/raft)** (Go): Raft consensus from scratch with a friend. It has leader election, log replication, crash persistence, a replicated KV store, and gRPC between nodes, and it passes `go test -race`. The browser demo lets you kill nodes and watch the cluster recover. The [DEVLOG](https://github.com/sachhayaKO/raft/blob/main/DEVLOG.md) is basically me learning Go as I went.

- **[vol-surface-agent](https://github.com/sachhayaKO/vol-surface-agent)** (Python, LangGraph): pulls a live options chain, solves for implied vol and greeks, compares them to realized vol, and answers questions like "is AAPL vol rich right now?" using recent filings for context. It scores 29/30 on a golden-question eval, and the [writeup](https://github.com/sachhayaKO/vol-surface-agent/blob/main/docs/EVALS.md) covers the bugs that testing caught.

**Tools I reach for**: Python, TypeScript, Go, SQL, FastAPI, Next.js, Postgres, Docker, Kubernetes.
