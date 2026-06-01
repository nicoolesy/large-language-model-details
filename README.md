# How a Large Language Model Is Built and What It Costs
An infographic that maps the **training pipeline of generative AI large language models** and quantifies the **resources** each model consumes: datasets, compute, energy, water, time, and money.
 
🔗 **Live infographic:** `https://<your-username>.github.io/<your-repo-name>/`

## 1. Summary of Main Points
 
The infographic communicates two linked ideas:
 
**A. The training pipeline (7 stages).** A generative AI LLM is not "written" — it is grown through an industrial process:
 
1. **Data Collection** — gather 10–15+ trillion tokens of web text, books, and code.
2. **Preprocessing & Tokenization** — clean, deduplicate, and filter the data, then convert it into tokens.
3. **Pre-training** — the compute-heavy core; the model learns by predicting the next token across the corpus.
4. **Supervised Fine-Tuning** — teach the base model to follow instructions.
5. **Alignment (RLHF / Constitutional AI)** — use preference feedback to make it helpful, honest, and harmless.
6. **Evaluation & Red-Teaming** — benchmark capability and test for safety and bias.
7. **Deployment & Inference** — serve the model and monitor it; inference cost recurs forever.
**B. The resource bill (6 categories).** I quantified what each model consumes:
 
- **Datasets** — e.g. GPT-4 (~13T tokens), Llama 3.1 (15T+ tokens).
- **Compute** — GPT-4 (~25,000 A100 GPUs, ~100 days); Llama 3.1 405B (16,000 H100s, ~30.8M GPU-hours).
- **Energy** — GPT-3 (1,287 MWh) → Llama 3.1 (~21.6 GWh), a ~17× rise.
- **Water** — GPT-3 training evaporated ~700,000 L of freshwater for cooling.
- **Time** — ~80 days for a single frontier pre-training run.
- **Cost** — GPT-4 (~$63–78M compute, $100M+ all-in); Gemini Ultra (~$192M).
The closing section argues **why this matters**: compute cost is a barrier to entry, energy and water are real environmental externalities, data quality increasingly drives performance, and inference is the long-tail cost.
 
---
 
## 2. Key Considerations
 
- **Audience.** Built for a mixed audience — readers who know AI and readers who don't. Plain-language stage descriptions sit beside hard numbers so both groups get value.
- **Accuracy & honesty.** Frontier-lab figures are inconsistent. I labeled every estimate as an estimate and marked undisclosed values explicitly rather than guessing. The Llama numbers (from Meta's own model cards) are the most reliable; GPT-4, Gemini, and Claude figures are third-party estimates.
- **Comparability.** A single comparison table normalizes five models across the same eight columns so differences — and missing data — are immediately visible.
- **Currency.** All figures reflect the best public reporting available as of 2026.
---
 
## 3. Classification Process & Rationale
 
The core analytical task was **classification**: organizing scattered, uneven information into categories that reveal relationships.
 
- **The process → a linear, numbered pipeline.** Training is inherently sequential and each stage feeds the next, so a numbered flow (01→07) is the most faithful visualization. I color-coded the stages into four phases — *data prep, compute core, align & tune, ship & serve* — to show that seven steps collapse into four conceptual groups.
- **The resources → six parallel categories.** Resources are not sequential; they co-occur, so I used parallel cards rather than a flow. Each card pairs a headline statistic with a short explanation.
- **The models → a normalized comparison matrix.** A table is the clearest way to compare entities across identical attributes. Crucially, I kept "not disclosed" cells visible instead of hiding them — the **pattern of disclosure** (Meta transparent; others opaque) is itself an insight.
**Critical-thinking note:** the most important classification decision was treating *missing data as data*. It would have been easy to fill blanks with guesses; instead, the absence of figures became a finding about industry transparency.
 
---
 
## 4. Design Rationale
 
- **Theme — editorial "field guide."** A warm cream paper with a faint dot grid evokes a printed reference, keeping dense numerical content calm and legible. The format deliberately matches my portfolio's house style so this artifact reads as another volume in the series.
- **Color as a coding system.** Slate-blue = data, terracotta = compute/pre-training, ochre = energy/alignment, teal = water, green = deployment, plum = cost. Color carries meaning, not just decoration — the same hues recur across the legend, pipeline, and resource specimens.
- **Typography.** *Playfair Display* (high-contrast serif) for characterful headlines and big statistics, with terracotta italics for emphasis; *Spectral* for readable serif body text; *Space Mono* for technical labels — reinforcing the printed-field-guide tone.
- **Hierarchy & motion.** Large hero statistics establish scale immediately; staggered scroll-reveal animation guides the eye through the narrative without overwhelming it.
- **Accessibility & portability.** Responsive layout (works on phone and desktop), high-contrast warm tones, semantic headings, and a single self-contained file with no dependencies — so it loads reliably on GitHub Pages.

---

## Sources
 
Figures are drawn from primary model cards and credible reporting; estimates for non-disclosing labs are clearly marked as such.
 
- Stanford HAI — *AI Index Report 2025* (frontier training-cost estimates)
- Epoch AI & SemiAnalysis — GPT-4 compute/hardware estimates
- Meta — Llama 3 / 3.1 official model cards (GPU-hours, energy, CO₂e)
- Li et al., *"Making AI Less 'Thirsty'"*, Communications of the ACM (GPT-3 water footprint)
- Patterson et al. — GPT-3 energy & emissions estimates
- The Register, Galileo, CUDO Compute, UC Riverside — supplementary reporting
> ⚠️ GPT-4, Gemini, and Claude figures are **third-party estimates** — those labs do not publish official training details. Treat all numbers as best-available estimates as of 2026.
