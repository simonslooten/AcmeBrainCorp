# TypeSafe AI / Jev — one-pager

Tags: `#onepager #steal-skip #park #typesafe #jev #sdk`
**Date:** 2026-09-20  
**Owner:** GB/CoS (park for later spike)  
**Source:** https://typesafe.ai/ · blog “Introducing System One Models & Jev” · LangChain/Vercel integrations (public)

## What it is
TypeSafe AI (SF, site labels **Version 0.01**). Product = **Jev**, first public **System One** model.

Not a chat LLM. Not a Grok Bot competitor. A **decision model for software**: you send structured state + typed questions; it returns Choice / Score / Boolean with **calibrated confidence**. Training story: **RLCD** (Reinforcement Learning for Calibrated Decisions) instead of RLHF chat preference.

Claimed economics (their workflow proof — **not** our benchmark): up to ~193× faster / ~444× cheaper vs LLMs on System One tasks; list price narrative ~$42 / billion input tokens. Treat marketing math as unverified.

## Thesis (why it exists)
RLHF models are optimized to please humans → strong at instruction-following chat, weak at reliable autonomy (mode drop, overconfidence). So production systems keep humans in the loop. TypeSafe’s bet: a second model class that is **machine-native** (typed, fast, confidence-aware) for the *decision* layer beside a generative LLM.

## What it is good for (documented use)
- Route: which model / tool / subagent next  
- Gate: risk check before shell / send / spend  
- Score: urgency, fit, refund-review, etc.  
- Verify / guardrail: judge LLM outputs without another full chat generation  

LangChain: `TypeSafeClassifier` + experimental `AutoModeMiddleware` (pre-tool risk block). Also exposed via Vercel AI Gateway `evaluate` API.

## Fit vs our GB/GX stack
| TypeSafe idea | Already in our policy |
|---|---|
| Confidence → act or escalate | Interrupt = money/product; do-alone vs park |
| Typed decisions in code | NEVER_FIT / claim rules still mostly LLM prose |
| Cheap classifier beside LLM | Many binary calls still burn full Grok tokens |

**Steal conceptually:** decision layer ≠ draft layer (mirrors GB ops vs GX long-form). Formal confidence thresholds = sharper charters (“if unsure, it qualifies”).

**Near-term cash candidate (only):** LN open-card triage (outplacement vs reintegratie/2e-spoor, size band, claim-or-skip) *before* expensive computerUse — **if** API access + calibration on our labeled cards proves out.

**ABC narrative fuel:** chat as the “puber”; calibrated decisions as governance — fits agency-before-lock-in / anti-FOMO without buying the product.

## What we will not do
- Replace Grok Bot, GX long drafts, or Bonica judgment with Jev  
- Integrate on tip energy (cash-first; Tuesday Optimus + BD stay ahead)  
- Treat their speed/cost multiples as facts until we measure on our workflows  

## Verdict
Interesting **complement** to chat agents; philosophically close to interrupt + reversibility. Park. Reopen only for a bounded LN/CoS spike with success criteria, or if a paying ABC client asks for a decision-layer architecture.

## Tape
- **Sources:** typesafe.ai homepage (fetched 2026-09-20); typesafe.ai/blog introducing System One & Jev; Vercel changelog Jev on AI Gateway; LangChain blog “Building a Harness with Jev”  
- **Guesses:** none on product shape; speed/cost multiples = vendor claim  
- **Skipped:** live API trial, enterprise pricing call, SF team diligence  
- **Evidence:** N/A (no UI session)

## Do / park
- **Do alone:** this note  
- **Park:** any signup, spend, or production wiring — Simon yes required  
