# Clayton Lawson

Deaf engineer in Washington, DC. I build AI systems for Deaf people, and I run
most of them on hardware I own.

My last year of work has one shape: Take a real problem in this community, build
the smallest system that actually solves it, and measure it honestly instead of
demoing it once. I have experimented with creating a homelaab purely for the purpose
of local AI and owning my data.

**What I work on**

- **Sign language recognition.** Pose landmarks in, gloss out. Trained up to a
  20B model on a single 8 GB Jetson, and shipped a frozen, signer-disjoint
  evaluation harness so the number means something: 39.78% top-1 across 250 ASL
  signs on five signers the model never saw, against 0.40% chance.
- **Grounded advisors.** A retrieval-augmented advisor for hearing parents of
  Deaf children, with citations that link the notes behind every answer and a
  deterministic crisis path that a ranking score cannot outvote. It is live, it
  answers in 18 languages, and it is built so a clinician can audit what it said.
- **Inference under constraint.** Three models behind one `llama.cpp` router on
  an 8 GB Orin Nano, with measured `ngl` ladders and page-reclaim instead of
  guesses. Electricity for the whole setup runs about $7 a month.

**Repositories worth your time**

| Repo | What it is |
|---|---|
| [sign-stack](https://github.com/claytonvlawson/sign-stack) | ASL recognition end to end, with a frozen signer-disjoint eval, CI, and one-command reproduction |
| [kb-advisor](https://github.com/claytonvlawson/kb-advisor) | Template RAG advisor: drop in client PDFs, get a cited, safety-routed API. 66 tests, no model calls in the suite |
| [learnwithclayparentadvisor](https://github.com/claytonvlawson/learnwithclayparentadvisor) | The advisor's front end: AIM-era chat, 18 languages, 20 Playwright tests running under the deploy's CSP |
| [jetson-orin-nano-models](https://github.com/claytonvlawson/jetson-orin-nano-models) | How three GGUF models fit in 8 GB, with the numbers and the traps written down |
| [neuron-steering-explorer](https://github.com/claytonvlawson/neuron-steering-explorer) | Steering-first neuron explorer for Qwen3.5-4B, derived from an upstream fork and credited |

**How I work**

Commits say why, not what. Tests are part of the change, not a follow-up. If
something is not finished, the README says so in a "what is not done" section
rather than letting you discover it. Most of what I ship runs on a Jetson, a
laptop, or a  VPS, for constraint-driven engineering.

**Elsewhere**

- LearnWithClay.AI: https://learnwithclay.ai
- Email: Claytonvlawson@gmail.com
