# LLMs & Civic Discourse — Full Literature Review Notes
> Source: [Penn MEDIATED — LLM Civic Discourse Dashboard](https://infodem.upenn.edu/llm-civic-discourse/)
> Data from: [GitHub: Penn-MEDIATED/LLM-Civic-Discourse](https://penn-mediated.github.io/LLM-Civic-Discourse/)
> Total papers: **71** | Compiled: May 2026

---

## How to Navigate This Document

Papers are grouped by the dashboard's own thematic tags. Many papers appear under multiple themes.

| # | Theme | Count |
|---|---|---|
| A | [Political Bias & Ideology](#a-political-bias--ideology) | 20 |
| B | [Content Moderation](#b-content-moderation) | 22 |
| C | [Persuasion & Political Influence](#c-persuasion--political-influence) | 9 |
| D | [Misinformation & Fact-Checking](#d-misinformation--fact-checking) | 18 |
| E | [User Behavior & Information Effects](#e-user-behavior--information-effects) | 6 |
| F | [Democracy & Public Deliberation](#f-democracy--public-deliberation) | 5 |
| G | [Benchmarks & Evaluation](#g-benchmarks--evaluation) | 10 |

> Papers marked **[Penn]** are from Penn-affiliated researchers.

---

## A. Political Bias & Ideology

---

### A1. Large Language Models Reflect the Ideology of Their Creators
| | |
|---|---|
| **Authors** | Buyl, M., Rogiers, A., Noels, S., Bied, G., Dominguez-Catena, I., Heiter, E., et al. & De Bie, T. |
| **Year** | 2026 |
| **Journal** | *npj Artificial Intelligence* |
| **Link** | https://www.nature.com/articles/s44387-025-00048-0 |

**What it's about:** This paper investigates how the institutional origin of an LLM — the company and country that built it — shapes its political outputs. Rather than relying on standard opinion polls administered to models, the authors take a behavioral approach: asking 19 popular LLMs to *describe* 3,991 politically prominent persons and then measuring how positively or negatively those descriptions are framed.

**How they did it:** They assembled a diverse set of 19 LLMs spanning different developers, geographies, and languages. For each model, they prompted it to produce descriptions of real-world political figures, then scored the sentiment and framing of those descriptions. Differences across models were analyzed in relation to developer characteristics (country of origin, language of training data, institutional mission).

**Key findings:**
- Design choices by LLM developers demonstrably shape how models portray political actors
- Clear differences emerge along both **language used** and **geographic origin** of the developer
- Models do not present a neutral "view from nowhere" — they carry ideological fingerprints traceable to their creators

**Implications:** Any deployment of LLMs in political journalism, AI-written summaries, or civic chatbots carries embedded ideological assumptions from whoever built the model.

**Tags:** `Political Bias & Ideology` `Benchmarks & Evaluation`

---

### A2. What Large Language Models Do Not Talk About: An Empirical Study of Moderation and Censorship Practices
| | |
|---|---|
| **Authors** | Noels, S., Bied, G., Buyl, M., Rogiers, A., Fettach, Y., Lijffijt, J., & De Bie, T. |
| **Year** | 2025 |
| **Journal** | *Joint European Conference on ML & KDD* |
| **Link** | https://link.springer.com/chapter/10.1007/978-3-032-05962-8_16 |

**What it's about:** An empirical audit examining whether LLMs *refuse* to answer or *omit* information on political topics, and whether those refusal patterns are consistent or biased.

**How they did it:** The authors systematically queried multiple LLMs about a large set of political topics and prominent individuals, then analyzed refusal and omission rates. They coded whether avoidance was more common for figures that were domestic to the model developer vs. foreign.

**Key findings:**
- Refusal and censorship patterns vary widely across models — there is no industry standard
- Censorship is **more common for prominent individuals who are domestic** to the LLM developer's country, suggesting politically motivated suppression of locally sensitive content
- Different models make very different decisions about what is "too political" to discuss

**Implications:** LLM silences are not neutral — they are shaped by developer interests and may encode geographic and political blind spots.

**Tags:** `Content Moderation` `Political Bias & Ideology` `Benchmarks & Evaluation`

---

### A5. Assessing Political Bias in Large Language Models
| | |
|---|---|
| **Authors** | Rettenberger, L., Reischl, M., & Schutera, M. |
| **Year** | 2025 |
| **Journal** | *Journal of Computational Social Science* |
| **Link** | https://link.springer.com/article/10.1007/s42001-025-00376-w |

**What it's about:** A systematic assessment of political bias in open-source LLMs available in the EU, focusing on whether model *scale* predicts ideological lean.

**How they did it:** The authors administered political opinion prompts to open-source LLMs (including Llama3 and smaller variants), mapping their responses to the EU political party spectrum.

**Key findings:**
- **Larger models** (e.g., Llama3) align more closely with left-leaning political parties
- **Smaller models** remain comparatively neutral
- Scale and ideological lean are correlated — a finding with implications for which models institutions choose to deploy

**Tags:** `Political Bias & Ideology`

---

### A7. Political Censorship in Large Language Models Originating from China
| | |
|---|---|
| **Authors** | Pan, J., & Xu, X. |
| **Year** | 2026 |
| **Journal** | *PNAS Nexus* |
| **Link** | https://academic.oup.com/pnasnexus/article/5/2/pgag013/8487339 |

**What it's about:** A cross-national comparison examining government censorship as a systematic source of LLM bias, focusing on Chinese-origin models.

**How they did it:** The authors compared Chinese-origin LLMs to non-Chinese LLMs across 145 political questions, varying both the content of the questions and the language (Chinese vs. English) used to ask them.

**Key findings:**
- Chinese-origin LLMs had **more inaccurate responses** and **higher refusal rates** than non-Chinese models on politically sensitive questions
- All models — not just Chinese ones — showed higher refusal rates for **Chinese-language prompts**, suggesting that language activates censorship heuristics
- Language-based differences are less pronounced than the difference between China-origin and non-China-origin models overall

**Implications:** State-level political censorship propagates into LLM behavior in ways that can be empirically measured and compared across models.

**Tags:** `Content Moderation` `Political Bias & Ideology`

---

### A13. On the Relationship Between Truth and Political Bias in Language Models
| | |
|---|---|
| **Authors** | Fulay, S., Brannon, W., Mohanty, S., Overney, C., Poole-Dayan, E., Roy, D., & Kabbara, J. |
| **Year** | 2024 |
| **Journal** | *EMNLP 2024* |
| **Link** | https://arxiv.org/html/2409.05283 |

**What it's about:** This paper investigates a troubling trade-off: optimizing LLMs for factual accuracy tends to introduce left-leaning political bias.

**Key findings:**
- Training reward models for **truthfulness** systematically produces **left-leaning outputs**
- This creates a dilemma: if truth-tracking causes ideological lean, it may be structurally impossible to align a model to be both truthful and politically neutral
- The finding has significant implications for RLHF (Reinforcement Learning from Human Feedback) and other alignment techniques

**Tags:** `Political Bias & Ideology` `Misinformation & Fact-Checking`

---

### A15. Large Language Models Polarize Ideologically but Moderate Affectively in Online Political Discourse
| | |
|---|---|
| **Authors** | Wang, G., Anbudurai, S., Sun, O., Li, X., & Wu, L. |
| **Year** | 2026 |
| **Journal** | *Preprint* |
| **Link** | https://arxiv.org/abs/2601.20238 |

**What it's about:** A natural experiment examining how the introduction of ChatGPT changed ideological and emotional patterns on Reddit's r/politics community.

**How they did it:** The authors used the public availability of ChatGPT as an exogenous shock and compared posting patterns on Reddit before and after its release, identifying posts with AI-generated characteristics.

**Key findings:**
- ChatGPT-influenced posts **intensified ideological polarization**: liberals became more liberal, conservatives more conservative
- This effect was *not* driven by more extreme or persuasive content — it came from **sycophancy**: AI-generated comments tend to echo and reinforce the viewpoint of the post they reply to
- Emotionally, AI-generated content was more moderate and calm, even as it amplified ideological positions

**Tags:** `Political Bias & Ideology` `User Behavior & Information Effects`

---

### A16. CIVICS: Building a Dataset for Examining Culturally-Informed Values in Large Language Models
| | |
|---|---|
| **Authors** | Pistilli, G., Leidinger, A., Jernite, Y., Kasirzadeh, A., Luccioni, A. S., & Mitchell, M. |
| **Year** | 2024 |
| **Journal** | *AAAI/ACM Conference on AI, Ethics, and Society* |
| **Link** | https://ojs.aaai.org/index.php/AIES/article/view/31710 |

**What it's about:** Introduction of the CIVICS dataset — a multilingual, multicultural benchmark designed to evaluate how LLMs handle socially sensitive topics across different cultural contexts.

**Key contribution:** The dataset (Culturally-Informed & Values-Inclusive Corpus for Societal Impacts) fills a gap in existing benchmarks, which are predominantly English-language and Western-centric.

**Tags:** `Political Bias & Ideology` `Benchmarks & Evaluation`

---

### A17. The Language You Ask In: Language-Conditioned Ideological Divergence in LLM Analysis of Contested Political Documents
| | |
|---|---|
| **Authors** | Smirnov, O. |
| **Year** | 2026 |
| **Journal** | *Preprint* |
| **Link** | https://arxiv.org/abs/2601.12164 |

**What it's about:** Demonstrates that the *language* used to prompt an LLM — not just the content of the question — shapes the ideological framing of its responses.

**Key findings:**
- Using Russian vs. Ukrainian to ask identical questions about contested political documents produced different rhetorical positioning, ideological conclusions, and interpretive framings
- Language functions as an implicit cultural cue that activates different patterns in the model

**Tags:** `Political Bias & Ideology`

---

### A19. Large Language Models' Detection of Political Orientation in Newspapers
| | |
|---|---|
| **Authors** | Buscemi, A., & Proverbio, D. |
| **Year** | 2024 |
| **Journal** | *Preprint* |
| **Link** | https://arxiv.org/abs/2406.00018 |

**What it's about:** Tests whether LLMs can reliably identify and agree on the political lean of newspaper articles, and whether their assessments are consistent across models.

**Key findings:**
- Different LLMs position the same newspapers very differently on the political spectrum
- Hints at "inconsistent training or excessive randomness in the algorithms" underlying political assessments
- Models cannot be reliably used as neutral political-lean detectors

**Tags:** `Political Bias & Ideology` `Benchmarks & Evaluation`

---

### A21. Prioritize Economy or Climate Action? Investigating ChatGPT Response Differences Based on Inferred Political Orientation
| | |
|---|---|
| **Authors** | Karadal, P., & Kekulluoglu, D. |
| **Year** | 2025 |
| **Journal** | *Preprint* |
| **Link** | https://arxiv.org/abs/2511.04706 |

**What it's about:** Explores how ChatGPT's outputs shift when it infers different political identities from user personas, globally.

**Key findings:**
- ChatGPT's reasoning and language choices are shaped by inferred political identity
- The "democratic" persona elicited responses closest to the neutral baseline — consistent with left-leaning tendencies in the model
- Effects were observed across different countries and languages

**Tags:** `Political Bias & Ideology` `User Behavior & Information Effects`

---

### A24. Whose Opinions Do Language Models Reflect?
| | |
|---|---|
| **Authors** | Santurkar, S., Durmus, E., Ladd, F., Han, E., Jurafsky, D., & Hashimoto, T. |
| **Year** | 2023 |
| **Journal** | *ICML 2023* |
| **Link** | https://dl.acm.org/doi/10.5555/3618408.3619652 |

**What it's about:** A foundational paper using public opinion survey data to ask whose views LLMs actually represent.

**How they did it:** The authors created a framework comparing LLM responses on a large set of social and political questions against actual U.S. population opinion surveys.

**Key findings:**
- Significant variation between LLMs and the general U.S. population
- LLMs do not represent the American public's views — they represent a skewed subset
- Produced a dataset for evaluating LLM opinion alignment that has been widely cited

**Tags:** `Political Bias & Ideology` `Benchmarks & Evaluation`

---

### A25. More Human Than Human: Measuring ChatGPT Political Bias
| | |
|---|---|
| **Authors** | Motoki, F., Pinho Neto, V., & Rodrigues, V. |
| **Year** | 2024 |
| **Journal** | *Public Choice* |
| **Link** | https://link.springer.com/article/10.1007/s11127-023-01097-2 |

**What it's about:** Uses a political compass-style survey instrument to measure ChatGPT's position on social (authoritarian/libertarian) and economic (left/right) dimensions.

**Key findings:**
- ChatGPT's responses most often align with Democrats on both social and economic axes
- The degree of left-libertarian lean is stronger than that of many human users

**Tags:** `Political Bias & Ideology`

---

### A29. Hidden Persuaders: LLMs' Political Leaning and Their Influence on Voters
| | |
|---|---|
| **Authors** | Potter, Y., Lai, S., Kim, J., Evans, J., & Song, D. |
| **Year** | 2024 |
| **Journal** | *EMNLP 2024* |
| **Link** | https://aclanthology.org/2024.emnlp-main.244/ |

**What it's about:** Two-part study: first establishing that LLMs lean politically, then testing whether that lean influences voters.

**How they did it:** Ran a voting simulation across 18 LLMs (finding consistent preference for Biden over Trump); then ran an experiment with 935 U.S. registered voters who interacted with LLMs.

**Key findings:**
- Instruction-tuned models showed more pronounced political lean than base models
- Voter interactions with LLMs shifted choices toward the Democratic nominee
- The influence persisted even when controlling for other variables

**Tags:** `Political Bias & Ideology` `Persuasion & Political Influence`

---

### A30. The Political Preferences of LLMs
| | |
|---|---|
| **Authors** | Rozado, D. |
| **Year** | 2024 |
| **Journal** | *PLOS ONE* |
| **Link** | https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0306621 |

**What it's about:** Administers 11 political orientation tests to 24 LLMs, providing a comprehensive mapping of LLM political preferences. Also demonstrates how fine-tuning can steer models toward specific leanings.

**Key findings:**
- Most LLMs tend left across multiple test instruments
- Fine-tuning on relatively modest amounts of ideologically-coded data can substantially shift model outputs
- Ideological alignment is achievable and relatively inexpensive

**Tags:** `Political Bias & Ideology` `Benchmarks & Evaluation`

---

### A31. PoliTune: Analyzing the Impact of Data Selection and Fine-Tuning on Economic and Political Biases in LLMs
| | |
|---|---|
| **Authors** | Agiza, A., Mostagir, M., & Reda, S. |
| **Year** | 2024 |
| **Journal** | *AAAI/ACM Conference on AI, Ethics, and Society* |
| **Link** | https://ojs.aaai.org/index.php/AIES/article/view/31612 |

**What it's about:** Introduces PoliTune, a parameter-efficient fine-tuning method for ideological alignment of LLMs. Investigates how data selection and fine-tuning interact to shape political and economic bias.

**Key findings:**
- Only a small fraction of parameters need to be modified to steer a model toward a specific ideology
- This makes ideological manipulation scalable and accessible — not limited to large labs
- Raises serious questions about LLM use in politically sensitive applications

**Tags:** `Political Bias & Ideology` `Benchmarks & Evaluation`

---

### A32. Measuring Political Stance and Consistency in Large Language Models
| | |
|---|---|
| **Authors** | Alali, S. F., Maasfeh, M. N., Kutlu, M., & Kardas, S. |
| **Year** | 2026 |
| **Journal** | *European Conference on Information Retrieval* |
| **Link** | https://link.springer.com/chapter/10.1007/978-3-032-21324-2_34 |

**What it's about:** Evaluates political stance consistency across 9 LLMs and 24 sensitive topics using five different prompting techniques.

**Key findings:**
- Models frequently take **opposing positions** on the same issue depending on how they are prompted
- Grok-3-mini was most consistent; Mistral-7B was least consistent
- Models generally supported "the side whose language is used in the prompt"
- On the Qatar blockade and Palestinian oppression, no prompting technique could shift model positions — suggesting deeply entrenched political stances on certain topics

**Tags:** `Political Bias & Ideology` `Benchmarks & Evaluation`

---

### A33. Ideological Distortions in the Digital Public Sphere: An Audit of Authoritarianism in Commercial LLMs
| | |
|---|---|
| **Authors** | Kyritsopoulos, C. G., Moore, A. B., Cram, L., Van Clief, J., & Llewellyn, C. |
| **Year** | 2026 |
| **Journal** | *Preprint (SSRN)* |
| **Link** | https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6108795 |

**What it's about:** Audits Grok, Claude, and ChatGPT using validated psychometric scales for left-wing and right-wing authoritarianism (LWA/RWA), comparing model responses to real ideological extremists.

**Key findings:**
- Models exhibit a "caricature effect" — they misrepresent authoritarian attitudes compared to actual human extremists
- Models underestimate how much right-wing extremists agree with left-wing authoritarian positions
- Models grossly overestimate RWA (right-wing authoritarianism) scores for right-wing extremists
- These distortions may widen perceived political divisions, making LLMs counterproductive as information intermediaries

**Tags:** `Political Bias & Ideology` `Benchmarks & Evaluation`

---

### A35. Measuring Perceived Slant in Large Language Models Through User Evaluations
| | |
|---|---|
| **Authors** | Westwood, S. J., Grimmer, J., & Hall, A. B. |
| **Year** | 2025 |
| **Journal** | *Stanford Graduate School of Business Working Paper* |
| **Link** | https://www.gsb.stanford.edu/faculty-research/working-papers/measuring-perceived-slant-large-language-models-through-user |

**What it's about:** Develops a user-centered approach to measuring political bias in LLMs, grounded in how *actual users* perceive model outputs rather than theoretical frameworks.

**How they did it:** Used ecologically valid prompts on 30 political topics across 24 models, collecting 180,126 assessments from 10,007 U.S. respondents.

**Key findings:**
- Nearly all models are **perceived as left-leaning** by users
- One widely-used model leans left on 24 of 30 topics
- When prompted for neutrality, models produce more *ambivalent* responses, which users interpret as neutral — but ambivalence is not the same as balance

**Tags:** `Political Bias & Ideology` `Benchmarks & Evaluation`

---

## B. Content Moderation

---

### B9. Longitudinal Monitoring of LLM Content Moderation of Social Issues ⭐ Penn
| | |
|---|---|
| **Authors** | Dai, Y., Lurie, E., Metaxa, D., & Friedler, S. A. |
| **Year** | 2025 |
| **Journal** | *Preprint* |
| **Link** | https://arxiv.org/abs/2510.01255 |

**What it's about:** Introduces a *longitudinal* auditing system that publicly tracks how LLMs handle sensitive social issues over time, making it possible to detect covert policy changes by companies.

**How they did it:** The researchers built a monitoring infrastructure that repeatedly queries OpenAI's models, OpenAI's moderation endpoint, and DeepSeek on a dataset of over 400 social issues. Audits were run at regular intervals over a sustained period.

**Key findings:**
- Company policy changes — even when **not publicly disclosed** — are detectable through longitudinal monitoring
- Refusal rates and content classification decisions shift over time in response to undisclosed policy updates
- Provides a model for independent, ongoing AI accountability infrastructure

**Implications:** LLM behavior is not fixed — it can be changed quietly by companies. Longitudinal auditing is essential for holding platforms accountable.

**Tags:** `Content Moderation` `Benchmarks & Evaluation` `Penn Research`

---

### B10. Large-Scale, Longitudinal Study of Large Language Models During the 2024 US Election Season
| | |
|---|---|
| **Authors** | Cen, S. H., Ilyas, A., Driss, H., Park, C., Hopkins, A., & Podimata, C. |
| **Year** | 2025 |
| **Journal** | *Preprint* |
| **Link** | https://arxiv.org/pdf/2509.18446 |

**What it's about:** Examines how 12 LLMs responded to over 12,000 election-related queries over five months during the run-up to the 2024 U.S. presidential election.

**Key contribution:** Releases the resulting dataset of LLM responses for future research. Provides an empirical baseline for understanding how election-related AI behavior varied across models and over time during a real high-stakes election.

**Tags:** `Content Moderation` `Benchmarks & Evaluation`

---

### B11. Identity-related Speech Suppression in Generative AI Content Moderation ⭐ Penn
| | |
|---|---|
| **Authors** | Metaxa, D., & Friedler, S. |
| **Year** | 2025 |
| **Journal** | *ACM EAAMO 2025* |
| **Link** | https://dl.acm.org/doi/10.1145/3757887.3763010 |

**What it's about:** An audit of five content moderation APIs — traditional and generative AI — measuring whether they disproportionately suppress speech *about* nine identity groups (Christian, non-Christian, white, non-white, straight, LGBT, disabled, women, men).

**How they did it:** Built two datasets (one user-generated, one LLM-generated) of identity-related text, developed a high-accuracy auto-tagging system (93–99.8% per category), and submitted texts to five moderation APIs measuring false-positive suppression rates.

**Key findings:**
- All APIs incorrectly suppress identity-related speech at elevated rates for at least one group
- Most APIs flag at least one group at **2–3× the overall false-positive rate**
- Disability-related content is more likely flagged for self-harm; non-Christian content for hate/violence
- Jigsaw performed best (worst-case 1.58×) but still imperfect

**Tags:** `Content Moderation` `Penn Research`

---

### B36. Model-Dependent Moderation: Inconsistencies in Hate Speech Detection Across LLM-Based Systems ⭐ Penn
| | |
|---|---|
| **Authors** | Fasching, N., & Lelkes, Y. |
| **Year** | 2025 |
| **Journal** | *Findings of ACL 2025* |
| **Link** | https://aclanthology.org/2025.findings-acl.1144/ |

**What it's about:** A systematic comparison of seven leading LLM-based content moderation systems on hate speech detection, revealing dramatic inconsistencies across platforms.

**How they did it:** Built a synthetic dataset of over **1.3 million sentences**, then submitted each to seven systems: dedicated moderation endpoints (OpenAI, Mistral), frontier models (Claude 3.5 Sonnet, GPT-4o, DeepSeek V3), and specialized APIs (Google Perspective API).

**Key findings:**
- The same content receives **markedly different classifications** depending on which system reviews it
- Inconsistencies are particularly pronounced for **specific demographic groups**
- The choice of moderation system alone can determine outcomes — there is no reliable cross-platform standard
- Raises serious concerns about consistency and fairness in automated hate speech moderation

**Tags:** `Content Moderation` `Penn Research`

---

### B37. Policy-as-Prompt: Rethinking Content Moderation in the Age of Large Language Models
| | |
|---|---|
| **Authors** | Palla, K., García, J. L. R., Hauff, C., Fabbri, F., Damianou, A., Lindström, H., et al. & Lalmas, M. |
| **Year** | 2025 |
| **Journal** | *ACM FAccT 2025* |
| **Link** | https://dl.acm.org/doi/full/10.1145/3715275.3732054 |

**What it's about:** Proposes a "policy-as-prompt" framework for integrating LLMs into content moderation and systematically identifies its failure modes.

**Key findings:** Five core challenges identified: translating platform policies into effective prompts is harder than it appears; technological constraints tend to shape policy rather than the reverse; power dynamics shift between policy and ML teams; accountability is diffuse; broader governance questions remain unresolved.

**Tags:** `Content Moderation`

---

### B38. SLM-Mod: Small Language Models Surpass LLMs at Content Moderation
| | |
|---|---|
| **Authors** | Zhan, X., Goyal, A., Chen, Y., Chandrasekharan, E., & Saha, K. |
| **Year** | 2025 |
| **Journal** | *NAACL 2025* |
| **Link** | https://aclanthology.org/2025.naacl-long.441/ |

**What it's about:** Large frontier models are expensive to run at scale. This paper shows that **fine-tuned small language models** (<15B parameters) outperform much larger models in zero-shot content moderation.

**How they did it:** Fine-tuned several SLMs on 150K comments from 15 Reddit communities, then benchmarked against zero-shot and few-shot large models.

**Key findings:** Fine-tuned SLMs outperform zero-shot LLMs at content moderation — pointing toward more cost-effective production moderation architectures.

**Tags:** `Content Moderation`

---

### B39. Content Moderation by LLM: From Accuracy to Legitimacy
| | |
|---|---|
| **Authors** | Huang, T. |
| **Year** | 2025 |
| **Journal** | *Artificial Intelligence Review* |
| **Link** | https://arxiv.org/abs/2409.03219 |

**What it's about:** Argues that evaluating LLM content moderation purely on accuracy metrics is insufficient and proposes a legitimacy-based framework.

**Key argument:** Easy cases (clear-cut violations) should be evaluated on accuracy and transparency. Hard cases (ambiguous content) require reasoned justification and user participation. The paper integrates legal and social science theory to propose a new moderation workflow.

**Tags:** `Content Moderation`

---

### B40. Watch Your Language: Investigating Content Moderation with Large Language Models
| | |
|---|---|
| **Authors** | Kumar, D., AbuHashem, Y. A., & Durumeric, Z. |
| **Year** | 2024 |
| **Journal** | *ICWSM 2024* |
| **Link** | https://arxiv.org/abs/2309.14517 |

**What it's about:** Evaluates LLMs on two distinct moderation tasks: rule-based community moderation (Reddit) and general toxic content detection.

**Key findings:**
- GPT-3.5 achieved median accuracy of 64% and median precision of 83% across 95 subreddits for rule-based moderation
- LLMs broadly outperformed existing classifiers on toxicity detection
- Larger models offered only marginal improvements, hinting at a performance ceiling

**Tags:** `Content Moderation`

---

### B41. LLM-Mod: Can Large Language Models Assist Content Moderation?
| | |
|---|---|
| **Authors** | Kolla, M., Salunkhe, S., Chandrasekharan, E., & Saha, K. |
| **Year** | 2024 |
| **Journal** | *CHI Extended Abstracts 2024* |
| **Link** | https://dl.acm.org/doi/full/10.1145/3613905.3650828 |

**What it's about:** Feasibility study examining how an LLM-based moderator reasons about Reddit rule violations.

**Key findings:**
- True-negative rate: 92.3% (good at clearing benign content)
- True-positive rate: 43.1% (poor at flagging actual violations)
- Performs well on keyword-matching violations; fails on complex contextual rule violations

**Tags:** `Content Moderation`

---

### B42. Large Language Models for Automatic Detection of Sensitive Topics
| | |
|---|---|
| **Authors** | Wen, R., Crowe, S., Gupta, K., Li, X., Billinghurst, M., Hoermann, S., et al. & Piumsomboon, T. |
| **Year** | 2024 |
| **Journal** | *OZCHI 2024* |
| **Link** | https://arxiv.org/abs/2409.00940 |

**What it's about:** Evaluates five LLMs on detecting sensitive messages in the mental well-being domain, across two online datasets.

**Key findings:** LLMs show strong potential for integration into mental health content moderation pipelines, with solid accuracy, precision, and recall on sensitive-topic detection.

**Tags:** `Content Moderation`

---

### B43. Algorithmic Arbitrariness in Content Moderation
| | |
|---|---|
| **Authors** | Gomez, J. F., Machado, C. V., Paes, L. M., & Calmon, F. P. |
| **Year** | 2024 |
| **Journal** | *ACM FAccT 2024* |
| **Link** | https://arxiv.org/abs/2402.16979 |

**What it's about:** Examines "predictive multiplicity" in ML content moderation — where equally performing models produce conflicting classifications for the same content.

**Key findings:**
- Multiple equally accurate models can disagree on the same post
- This arbitrariness creates **unfair speech restrictions with disparate impact** across social groups
- Calls for transparency in algorithmic moderation and warns of an "algorithmic leviathan"

**Tags:** `Content Moderation`

---

### B44. Socio-Culturally Aware Evaluation Framework for LLM-Based Content Moderation
| | |
|---|---|
| **Authors** | Kumar, S., Kholkar, G., Mendke, S., Sadana, A., Agrawal, P., & Dandapat, S. |
| **Year** | 2024 |
| **Journal** | *Preprint* |
| **Link** | https://arxiv.org/abs/2412.13578 |

**What it's about:** Introduces an evaluation framework for assessing LLM moderation performance specifically for underrepresented demographic groups, and a scalable method for building diverse test datasets.

**Tags:** `Content Moderation`

---

### B45. Towards Safer Social Media Platforms: Scalable and Performant Few-Shot Harmful Content Moderation Using LLMs
| | |
|---|---|
| **Authors** | Bonagiri, A., Li, L., Oak, R., Babar, Z., Wojcieszak, M., & Chhabra, A. |
| **Year** | 2025 |
| **Journal** | *Preprint* |
| **Link** | https://arxiv.org/abs/2501.13976 |

**What it's about:** Proposes using few-shot in-context learning with LLMs as a scalable alternative to traditional moderation requiring large labeled datasets.

**Key findings:** LLMs with few-shot prompting outperform Perspective API and OpenAI Moderation in detecting harmful content — without needing large training sets.

**Tags:** `Content Moderation`

---

### B46. Ideology-Based LLMs for Content Moderation
| | |
|---|---|
| **Authors** | Civelli, S., Bernardelle, P., Pratama, N. A., & Demartini, G. |
| **Year** | 2025 |
| **Journal** | *Preprint* |
| **Link** | https://arxiv.org/abs/2510.25805 |

**What it's about:** Explores how ideological personas affect LLM content moderation consistency and fairness.

**Key findings:** Personas had modest effects on accuracy, but ideological framing shaped whether content was labeled harmful — demonstrating that the implicit worldview of a model influences its moderation decisions.

**Tags:** `Content Moderation` `Political Bias & Ideology`

---

### B47. Hate Personified: Investigating the Role of LLMs in Content Moderation
| | |
|---|---|
| **Authors** | Masud, S., Singh, S., Hangya, V., Fraser, A., & Chakraborty, T. |
| **Year** | 2024 |
| **Journal** | *EMNLP 2024* |
| **Link** | https://aclanthology.org/2024.emnlp-main.886/ |

**What it's about:** Investigates whether persona-based prompting can make LLMs represent diverse human perspectives in hate speech detection, tested across 5 languages and 6 datasets.

**Key findings:**
- Persona-based prompting increases annotation variability (reflecting real human disagreement)
- Geographical signals improve regional alignment
- Numerical anchors (community flagging rates) can be integrated to improve model performance

**Tags:** `Content Moderation`

---

### B48. Safeguarding Decentralized Social Media: LLM Agents for Automating Community Rule Compliance
| | |
|---|---|
| **Authors** | La Cava, L., & Tagarelli, A. |
| **Year** | 2025 |
| **Journal** | *Online Social Networks and Media* |
| **Link** | https://www.sciencedirect.com/science/article/pii/S2468696425000205 |

**What it's about:** Evaluates six LLM-based AI agents for content moderation on Mastodon, a decentralized platform, across 50,000+ posts from hundreds of servers.

**Key findings:** Agents effectively detect non-compliant content, handle linguistic nuances, and adapt to diverse community norms — suggesting viability for decentralized, community-specific moderation.

**Tags:** `Content Moderation`

---

### B49. On the Limitations of LLM-Synthesized Social Media Misinformation Moderation
| | |
|---|---|
| **Authors** | Singh, S., Wu, J., Churina, S., & Jaidka, K. |
| **Year** | 2025 |
| **Journal** | *Preprint (OpenReview)* |
| **Link** | https://openreview.net/forum?id=ilz2ghLgzt |

**What it's about:** Tests whether LLMs can write Community Notes-style moderation annotations as good as humans. Introduces ModBench.

**Key findings:** Despite web references and few-shot examples, LLM notes persistently fail on accuracy, coherence, and citation reliability. Human-written moderation notes remain essential.

**Tags:** `Content Moderation` `Misinformation & Fact-Checking`

---

### B50. Are Open-Weight LLMs Ready for Social Media Moderation? A Comparative Study on Bluesky
| | |
|---|---|
| **Authors** | Chou, H. Y., Naveed, W., Zhou, S., & Yang, X. |
| **Year** | 2026 |
| **Journal** | *Preprint* |
| **Link** | https://arxiv.org/abs/2602.05189 |

**What it's about:** Benchmarks four proprietary and three open-weight LLMs on harmful content detection using real-world Bluesky posts.

**Key findings:** Open-weight models perform comparably to proprietary ones. Performance varies sharply by content type — rudeness detection vs. intolerance/threat detection have different precision-recall profiles.

**Tags:** `Content Moderation`

---

### B51. CoPE: A Small Language Model for Steerable and Scalable Content Labeling
| | |
|---|---|
| **Authors** | Chakrabarti, S., Willner, D., Klyman, K., Saade, T., Capstick, E., & Nong, S. |
| **Year** | 2025 |
| **Journal** | *Preprint* |
| **Link** | https://arxiv.org/pdf/2512.18027 |

**What it's about:** Introduces CoPE, a small language model that can be steered to apply different content labeling policies via prompts at scale.

**Key findings:** Across seven harm dimensions, CoPE outperforms large models on accuracy, showing that policy-steerable small models are a viable production-scale moderation architecture.

**Tags:** `Content Moderation`

---

### B52. Measurement and Metrics for Content Moderation: The Multi-Dimensional Dynamics of Engagement and Content Removal on Facebook
| | |
|---|---|
| **Authors** | Edelson, L., Kovba, B., Yershova, H., Botelho, A., McCoy, D., & Lauinger, T. |
| **Year** | 2025 |
| **Journal** | *Journal of Online Trust and Safety* |
| **Link** | https://tsjournal.org/index.php/jots/article/view/220 |

**What it's about:** Proposes "prevented dissemination" — an outcome-based metric for measuring the impact of content moderation — and applies it to Facebook posts in English, Ukrainian, and Russian.

**Key findings:** Moderation prevented only **24–30% of predicted future engagement**, highlighting significant practical limits of current moderation systems. Large asymmetries exist in how posts accumulate engagement over time.

**Tags:** `Content Moderation`

---

### B53. Measuring the Mental Health of Content Reviewers: A Systematic Review
| | |
|---|---|
| **Authors** | Gonzalez, A., & Matias, J. N. |
| **Year** | 2025 |
| **Journal** | *Preprint* |
| **Link** | https://arxiv.org/abs/2502.00244 |

**What it's about:** Systematic review of how psychological harm among human content reviewers is currently measured, and what gaps exist.

**Key findings:** Significant gaps in measurement validity, especially in regions where content review labor is concentrated. Calls for culturally-relevant, work-specific mental health metrics.

**Tags:** `Content Moderation`

---

### B54. Perceptions of AI as a Misinformation Moderator: The Roles of Argument Type and Group Chat Size
| | |
|---|---|
| **Authors** | Silver, B., Williams-Ceci, S., & Naaman, M. |
| **Year** | 2025 |
| **Journal** | *Preprint* |
| **Link** | https://sciety.org/articles/activity/10.31234/osf.io/r9aew_v1 |

**What it's about:** Two experiments examining user *perceptions* of AI moderators vs. human moderators in online group settings.

**Key findings:** AI moderators were initially seen as less effective when using harm-based arguments, but this gap disappeared a year later — indicating growing public acceptance. Group size did not affect perceived AI moderator effectiveness.

**Tags:** `Content Moderation` `Misinformation & Fact-Checking`

---

### B55. Adapting to Automated Governance: Unpacking User Perceptions of Bot Moderation in Telegram and Discord
| | |
|---|---|
| **Authors** | Zhao, A., Wu, L., Hsieh, C. Y., & Naaman, M. |
| **Year** | 2024 |
| **Journal** | *ACM* |
| **Link** | https://osf.io/preprints/socarxiv/gqwdp |

**What it's about:** Qualitative study of how users perceive automated bots in Telegram and Discord, based on 21 in-depth interviews.

**Key findings:** Users broadly accept bot moderation for its consistency and perceived neutrality — but bots fail on cultural nuances, making human oversight essential.

**Tags:** `Content Moderation`

---

## C. Persuasion & Political Influence

---

### C6. The Levers of Political Persuasion with Conversational AI
| | |
|---|---|
| **Authors** | Black, S., Lin, H., Fist, C., Margetts, H., Rand, D. G., & Summerfield, C. |
| **Year** | 2025 |
| **Journal** | *Science* |
| **Link** | https://www.science.org/doi/10.1126/science.aea3884 |

**What it's about:** Evaluates 19 LLMs on persuasiveness about political topics, systematically identifying what *makes* LLMs more persuasive.

**Key findings:**
- Post-training and prompting strategies increased LLM persuasiveness more than either personalization or scaling the model
- Higher LLM persuasiveness was **associated with lower factual accuracy** — a critical trade-off
- Published in *Science*, this is one of the most high-profile empirical papers on LLM persuasion

**Tags:** `Persuasion & Political Influence` `Benchmarks & Evaluation`

---

### C8. Dialogues on Democracy: Belief-Tailored AI Conversations Reduce Inaccurate Election Denial Beliefs
| | |
|---|---|
| **Authors** | Hopkins, S. A., Costello, T., Pennycook, G., & Rand, D. |
| **Year** | 2026 |
| **Journal** | *Preprint* |
| **Link** | https://assets-eu.researchsquare.com/files/rs-8663921/v1_covered_e27a55ae-eb7f-4ca2-8157-a1932183c8e8.pdf |

**What it's about:** Two experiments testing whether tailored LLM conversations can reduce belief in election denialism.

**Key findings:**
- Both interventions reduced confidence in conspiratorial election claims
- Participants with the *strongest* prior election denial beliefs experienced the **largest decreases**
- Demonstrates LLMs can be deployed constructively to combat specific forms of political misinformation

**Tags:** `Persuasion & Political Influence` `Misinformation & Fact-Checking`

---

### C20. Leveraging AI for Democratic Discourse: Chat Interventions Can Improve Online Political Conversations at Scale
| | |
|---|---|
| **Authors** | Argyle, L. P., Bail, C. A., Busby, E. C., Gubler, J. R., Howe, T., Rytting, C., et al. & Wingate, D. |
| **Year** | 2023 |
| **Journal** | *PNAS* |
| **Link** | https://www.pnas.org/doi/abs/10.1073/pnas.2311627120 |

**What it's about:** A randomized controlled trial testing an AI assistant that makes real-time suggestions for improving divisive online political conversations.

**How they did it:** One participant in a two-person political conversation had access to the AI assistant; the other did not. Post-conversation surveys measured quality and openness to opposing views.

**Key findings:**
- When one person used the AI assistant, their partner rated the conversation quality higher
- Both participants showed greater willingness to grant opponents space to express views
- Demonstrates that AI can function as a productive *moderating* force in political dialogue

**Tags:** `Democracy & Public Deliberation` `Persuasion & Political Influence`

---

### C22. Biased LLMs Can Influence Political Decision-Making
| | |
|---|---|
| **Authors** | Fisher, J., Feng, S., Aron, R., Richardson, T., Choi, Y., Fisher, D. W., et al. & Reinecke, K. |
| **Year** | 2025 |
| **Journal** | *ACL 2025* |
| **Link** | https://aclanthology.org/2025.acl-long.328/ |

**What it's about:** Two experiments testing whether partisan bias in LLMs shifts users' political opinions and decision-making.

**Key findings:**
- Participants mirrored the biases displayed by LLMs in their political positions
- This effect persisted even **when the model's bias was opposite to the participant's own partisan identity**
- Demonstrates cross-partisan persuasion — a particularly concerning finding

**Tags:** `Persuasion & Political Influence` `Political Bias & Ideology`

---

### C26. Evaluating the Persuasive Influence of Political Microtargeting with Large Language Models
| | |
|---|---|
| **Authors** | Hackenburg, K., & Margetts, H. |
| **Year** | 2024 |
| **Journal** | *PNAS* |
| **Link** | https://www.pnas.org/doi/10.1073/pnas.2403116121 |

**What it's about:** Tests whether GPT-4-generated political messages are persuasive, and whether personalization (microtargeting) amplifies that persuasion.

**Key findings:**
- GPT-4 messages were persuasive on renewable energy, NATO support, and China sanctions
- Microtargeted versions (personalized to demographic/political data) were **not** more persuasive than generic versions
- Personalization did not add persuasive power beyond what general LLM generation already achieves

**Tags:** `Persuasion & Political Influence`

---

### C27. LLM-Generated Messages Can Persuade Humans on Policy Issues
| | |
|---|---|
| **Authors** | Bai, H., Voelkel, J. G., Eichstaedt, J. C., & Willer, R. |
| **Year** | 2024 |
| **Journal** | *Nature Communications* |
| **Link** | https://www.nature.com/articles/s41467-025-61345-5 |

**What it's about:** Tests whether LLM-generated persuasive messages are as effective as messages written by everyday people on a set of highly polarized issues.

**Key findings:**
- LLM messages were **similarly effective** to human-written messages
- LLMs' persuasive power comes from use of "facts, evidence, logical reasoning, and a dispassionate voice" — distinct from human rhetorical approaches
- Raises concerns about automated persuasion at scale

**Tags:** `Persuasion & Political Influence`

---

### C34. Chatbot Voting Advice Applications Inform but Seldom Sway Young Unaligned Voters
| | |
|---|---|
| **Authors** | Velez, Y. R., Green, D. P., & Sevi, S. |
| **Year** | 2025 |
| **Journal** | *PNAS* |
| **Link** | https://www.pnas.org/doi/abs/10.1073/pnas.2515516122 |

**What it's about:** Introduces and evaluates a "VAA Bot" — a chatbot delivering personalized election information from official party platforms to young, politically unaffiliated voters.

**How they did it:** Three experimental studies with young, unaffiliated adults.

**Key findings:**
- The bot successfully improved knowledge of party positions on specific issues
- Produced **weak effects on voting preferences** and partisan evaluations
- LLM-based civic tools are better equipped to *inform* than to *persuade* — a meaningful distinction for democratic design

**Tags:** `Persuasion & Political Influence` `Democracy & Public Deliberation`

---

### C71. Benchmarking Political Persuasion Risks Across Frontier Large Language Models
| | |
|---|---|
| **Authors** | Chen, Z., Kalla, J., & Le, Q. |
| **Year** | 2026 |
| **Journal** | *Preprint* |
| **Link** | https://arxiv.org/pdf/2603.09884 |

**What it's about:** Using two survey experiments, evaluates whether seven frontier AI models exhibit political persuasion capabilities and introduces a cross-model risk assessment framework.

**Key findings:**
- All models outperformed standard campaign advertisements in persuasiveness
- **Claude was the most persuasive**; Grok was the least
- Effect of information-based prompting on persuasion is **model-dependent**: increases persuasion for Claude and Grok but reduces it for GPT
- Provides a benchmarking framework for ongoing cross-model persuasion risk assessment

**Tags:** `Persuasion & Political Influence` `Benchmarks & Evaluation`

---

## D. Misinformation & Fact-Checking

---

### D4. Large Language Models Require Curated Context for Reliable Political Fact-Checking
| | |
|---|---|
| **Authors** | DeVerna, M. R., Yang, K. C., Yan, H. Y., & Menczer, F. |
| **Year** | 2025 |
| **Journal** | *Preprint* |
| **Link** | https://arxiv.org/abs/2511.18749 |

**What it's about:** Tests LLM performance on 6,000 claims vetted by PolitiFact, comparing standard models, web-search-augmented models, and reasoning models.

**Key findings:**
- Standard LLMs perform poorly on fact-checking tasks
- Web search and advanced reasoning improve performance modestly
- The **most effective improvement** comes from giving models access to curated, high-quality contextual evidence
- "Retrieval-augmented generation with quality sources" is the takeaway architecture

**Tags:** `Misinformation & Fact-Checking`

---

### D28. Towards Reliable Misinformation Mitigation: Generalization, Uncertainty, and GPT-4
| | |
|---|---|
| **Authors** | Pelrine, K., Kalantari, R., Qutab, M., Ebner, M., & Chevalier, F. |
| **Year** | 2023 |
| **Journal** | *EMNLP 2023* |
| **Link** | https://aclanthology.org/2023.emnlp-main.395/ |

**What it's about:** Examines GPT-4's cross-domain and cross-language misinformation detection capabilities.

**Key findings:** GPT-4 outperforms prior approaches across languages and domains. Key improvement areas identified: web retrieval, explainability, and uncertainty quantification.

**Tags:** `Misinformation & Fact-Checking`

---

### D56. Language Models Cannot Reliably Distinguish Belief from Knowledge and Fact
| | |
|---|---|
| **Authors** | Suzgun, M., Gur, T., Bianchi, F., Ho, D. E., Icard, T., Jurafsky, D., & Zou, J. |
| **Year** | 2025 |
| **Journal** | *Nature Machine Intelligence* |
| **Link** | https://www.nature.com/articles/s42256-025-01113-8 |

**What it's about:** Evaluates 24 LLMs on a new 13,000-question benchmark testing epistemic discrimination — the ability to distinguish facts, beliefs, and opinions.

**Key findings:**
- All models fail to handle **first-person false beliefs** (e.g., "I believe nicotine is not addictive")
- Even GPT-4o and DeepSeek R1 show dramatic accuracy drops on first-person belief tasks
- Third-person false beliefs are handled far better than first-person ones
- LLM competence may reflect superficial pattern matching rather than genuine epistemic understanding

**Tags:** `Misinformation & Fact-Checking`

---

### D57. Large Language Models Show Dunning-Kruger-Like Effects in Multilingual Fact-Checking
| | |
|---|---|
| **Authors** | Qazi, I. A., Khan, Z., Ghani, A., Raza, A. A., Qazi, Z. A., Sajjad, W., & Azeemi, A. H. |
| **Year** | 2026 |
| **Journal** | *Scientific Reports* |
| **Link** | https://www.nature.com/articles/s41598-026-39046-w |

**What it's about:** Evaluates 9 LLMs on 5,000 professional fact-checked claims across 47 languages, documenting a Dunning-Kruger-like pattern.

**Key findings:**
- Smaller models show **high confidence despite lower accuracy**
- Larger models are more accurate but less confident
- Performance gaps are worst for non-English languages and claims from the Global South
- Smaller organizations with limited resources tend to rely on smaller, more overconfident models — a systemic equity risk

**Tags:** `Misinformation & Fact-Checking`

---

### D58. ThinknCheck: Grounded Claim Verification with Compact, Reasoning-Driven, and Interpretable Models ⭐ Penn
| | |
|---|---|
| **Authors** | Rao, D., Han, F., & Callison-Burch, C. |
| **Year** | 2026 |
| **Journal** | *arXiv* |
| **Link** | https://arxiv.org/pdf/2604.01652 |

**What it's about:** Introduces ThinknCheck, a small LLM trained to *reason before verdict* on claim verification — showing that training models to reason explicitly outperforms prompting them to do so.

**Key findings:** Despite being far smaller than comparable models, ThinknCheck matches or outperforms them across multiple benchmarks. Explicit chain-of-thought *training* (not just prompting) produces more accurate and interpretable small fact-checking models.

**Tags:** `Misinformation & Fact-Checking` `Penn Research`

---

### D59. Factuality Challenges in the Era of LLMs and Opportunities for Fact-Checking
| | |
|---|---|
| **Authors** | Augenstein, I., Baldwin, T., Cha, M., Chakraborty, T., Ciampicaglia, G. L., Corney, D., & Zagni, G. |
| **Year** | 2024 |
| **Journal** | *Nature Machine Intelligence* |
| **Link** | https://www.nature.com/articles/s42256-024-00881-z |

**What it's about:** A broad survey of LLM factuality failures and how those failures interact with automated fact-checking systems.

**Key argument:** LLMs are simultaneously a threat (spreading misinformation at scale) and a potential tool (automating transcription, summarization, cross-referencing for fact-checkers).

**Tags:** `Misinformation & Fact-Checking`

---

### D60. The Perils and Promises of Fact-Checking with Large Language Models
| | |
|---|---|
| **Authors** | Quelle, D., & Bovet, A. |
| **Year** | 2024 |
| **Journal** | *Frontiers in AI* |
| **Link** | https://www.frontiersin.org/journals/artificial-intelligence/articles/10.3389/frai.2024.1341697/full |

**What it's about:** Evaluates LLM agents on the full fact-checking pipeline: query formulation, contextual retrieval, and verdict justification.

**Key findings:** Providing contextual information substantially improves LLM fact-checking. GPT-4 outperforms GPT-3, but accuracy varies by query language and claim type.

**Tags:** `Misinformation & Fact-Checking`

---

### D61. Multilingual Fact-Checking Using LLMs
| | |
|---|---|
| **Authors** | Singhal, A., Law, T., Kassner, C., Gupta, A., Duan, E., Damle, A., & Li, R. L. |
| **Year** | 2024 |
| **Journal** | *NLP4PI Workshop* |
| **Link** | https://aclanthology.org/2024.nlp4pi-1.2/ |

**What it's about:** Benchmarks LLM multilingual factual knowledge and fact-checking ability across five languages and five models.

**Key findings:** Zero-shot prompting with specific techniques outperforms complex reasoning chains. Model accuracy is **negatively correlated** with internet content availability in a given language — a key equity concern.

**Tags:** `Misinformation & Fact-Checking`

---

### D62. Can LLMs Improve Multimodal Fact-Checking by Asking Relevant Questions?
| | |
|---|---|
| **Authors** | Beigi, A., Jiang, B., Li, D., Tan, Z., Shaeri, P., Kumarage, T., & Liu, H. |
| **Year** | 2025 |
| **Journal** | *IEEE BigData 2025* |
| **Link** | https://ieeexplore.ieee.org/abstract/document/11400846/ |

**What it's about:** Introduces Lrq-Fact, a framework using LLMs to generate targeted Fact-Checking Questions (FCQs) that verify claims through structured questioning.

**Key findings:** Consistently outperforms baseline fact-checking methods; generates diverse and relevant question types.

**Tags:** `Misinformation & Fact-Checking`

---

### D63. FACT-GPT: Fact-Checking Augmentation via Claim Matching with LLMs
| | |
|---|---|
| **Authors** | Choi, E. C., & Ferrara, E. |
| **Year** | 2024 |
| **Journal** | *WWW 2024 Companion* |
| **Link** | https://dl.acm.org/doi/abs/10.1145/3589335.3651504 |

**What it's about:** A specialized LLM trained on synthetic data to identify whether social media content aligns with, contradicts, or is unrelated to previously debunked claims.

**Key findings:** Matches accuracy of larger models; closely mirrors human judgment for claim identification.

**Tags:** `Misinformation & Fact-Checking`

---

### D64. Towards Automated Fact-Checking of Real-World Claims: Exploring Task Formulation and Assessment with LLMs
| | |
|---|---|
| **Authors** | Sahitaj, P., Maab, I., Yamagishi, J., Kolanowski, J., Möller, S., & Schmitt, V. |
| **Year** | 2025 |
| **Journal** | *arXiv* |
| **Link** | https://arxiv.org/abs/2502.08909 |

**What it's about:** Establishes baselines for automated fact-checking using Llama-3 models on nearly 18,000 PolitiFact claims with web-retrieved evidence.

**Key findings:** Larger models outperform smaller ones; evidence integration improves all models; distinguishing nuanced rating labels (e.g., "mostly true" vs. "half true") remains a key challenge.

**Tags:** `Misinformation & Fact-Checking`

---

### D65. How LLMs Fail to Support Fact-Checking
| | |
|---|---|
| **Authors** | Proma, A. M., Pate, N., Druckman, J., Ghoshal, G., He, H., & Hoque, E. |
| **Year** | 2025 |
| **Journal** | *arXiv* |
| **Link** | https://arxiv.org/abs/2503.01902 |

**What it's about:** Tests ChatGPT, Gemini, and Claude on identifying credible sources and generating persuasive corrections to political misinformation.

**Key findings:** Models struggle to ground responses in real news sources. When they do cite sources, they preferentially cite left-leaning outlets.

**Tags:** `Misinformation & Fact-Checking`

---

### D66. OpenFactCheck: Building, Benchmarking Customized Fact-Checking Systems and Evaluating LLM Factuality
| | |
|---|---|
| **Authors** | Wang, Y., Wang, M., Iqbal, H., Georgiev, G. N., Geng, J., Gurevych, I., & Nakov, P. |
| **Year** | 2025 |
| **Journal** | *COLING 2025* |
| **Link** | https://aclanthology.org/2025.coling-main.755/ |

**What it's about:** Introduces OpenFactCheck, a unified, modular framework for automated fact-checking with three components: system customization, LLM factuality evaluation, and system reliability assessment.

**Tags:** `Misinformation & Fact-Checking`

---

### D67. Fact-Checking with Generative AI: A Systematic Cross-Topic Examination
| | |
|---|---|
| **Authors** | Kuznetsova, E., Vitulano, I., Makhortykh, M., Stolze, M., Nagy, T., & Vziatysheva, V. |
| **Year** | 2025 |
| **Journal** | *arXiv* |
| **Link** | https://arxiv.org/abs/2503.08404 |

**What it's about:** AI audit of 5 LLMs on 16,000+ journalist-verified claims using topic modeling and regression to identify performance factors.

**Key findings:** GPT-4 and Gemini outperform others; models perform better on false statements about COVID-19 and political controversies (likely due to guardrails); significant cross-model and cross-topic inconsistencies.

**Tags:** `Misinformation & Fact-Checking`

---

### D68. Fact-Checking AI-Generated News Reports: Can LLMs Catch Their Own Lies?
| | |
|---|---|
| **Authors** | Yao, J., Sun, H., & Xue, N. |
| **Year** | 2025 |
| **Journal** | *arXiv* |
| **Link** | https://arxiv.org/abs/2503.18293 |

**What it's about:** Tests whether LLMs can accurately fact-check content generated by *other* LLMs — i.e., can AI catch AI?

**Key findings:** Better at national/international than local news; better on static than dynamic information; better at identifying true than false claims; web search reduces unverifiable claims but introduces low-quality sources.

**Tags:** `Misinformation & Fact-Checking`

---

### D69. Facts Are Harder Than Opinions: A Multilingual, Comparative Analysis of LLM-Based Fact-Checking Reliability
| | |
|---|---|
| **Authors** | Saju, L., Bleier, A., Lasser, J., & Wagner, C. |
| **Year** | 2025 |
| **Journal** | *arXiv* |
| **Link** | https://arxiv.org/abs/2506.03655 |

**What it's about:** Assesses 5 LLMs on 61,514 claims across multiple languages, finding that factual claims are harder to classify than opinions.

**Key findings:** GPT-4 achieves highest accuracy but refused to classify 43% of all claims. Claims that *appear* factual are misclassified more than opinions — a major challenge for scale deployment.

**Tags:** `Misinformation & Fact-Checking`

---

### D70. @Grok Is This True? LLM-Powered Fact-Checking on Social Media
| | |
|---|---|
| **Authors** | Renault, T., Mosleh, M., & Rand, D. |
| **Year** | 2025 |
| **Journal** | *OSF Preprints* |
| **Link** | https://osf.io/preprints/psyarxiv/85quw_v2 |

**What it's about:** The first large-scale empirical study of LLM-based fact-checking in the wild, using 1.7 million real fact-checking requests to Grok and Perplexity on X (Twitter).

**Key findings:**
- Fact-checking constitutes only 7.6% of all chatbot interactions
- **Republicans prefer Grok**; **Democrats prefer Perplexity** — partisan asymmetry in tool selection
- LLM fact-checks shifted beliefs comparably to professional fact-checking
- Responses to Grok polarized when model identity was disclosed — source credibility is political

**Tags:** `Misinformation & Fact-Checking`

---

## E. User Behavior & Information Effects

---

### E3. Experimental Evidence of the Effects of LLMs versus Web Search on Depth of Learning ⭐ Penn
| | |
|---|---|
| **Authors** | Melumad, S., & Yun, J. H. |
| **Year** | 2025 |
| **Journal** | *PNAS Nexus* |
| **Link** | https://academic.oup.com/pnasnexus/article/4/10/pgaf316/8303888 |

**What it's about:** A 7-experiment, N=10,462 study directly comparing learning outcomes when using ChatGPT vs. Google Search.

**How they did it:** Participants were randomly assigned to ChatGPT or Google, learned about a topic, then wrote advice for others. Advice was analyzed for depth, originality, and helpfulness by third-party recipients.

**Key findings:**
- LLM learners reported less depth of learning
- Their advice was shorter, less factually grounded, and more generic
- Advice recipients rated it less helpful and were less likely to adopt it
- Effects persisted even when information *content* was held equal — **presentation format itself** drives passive learning

**Tags:** `User Behavior & Information Effects` `Penn Research`

---

### E14. Artificial Intelligence and Civil Discourse: How LLMs Moderate Climate Change Conversations
| | |
|---|---|
| **Authors** | Fan, W., & Xu, W. |
| **Year** | 2025 |
| **Journal** | *Preprint* |
| **Link** | https://arxiv.org/abs/2506.12077 |

**What it's about:** Examines how LLMs naturally moderate online climate change conversations through their communication style.

**Key findings:** LLMs are more emotionally neutral and maintain lower emotional intensity than human users — intrinsic properties that could improve the quality of discourse on controversial topics without explicit moderation instructions.

**Tags:** `Democracy & Public Deliberation` `User Behavior & Information Effects`

---

### E23. Conversational AI Increases Political Knowledge as Effectively as Self-Directed Internet Search
| | |
|---|---|
| **Authors** | Luettgau, L., Kirk, H. R., Hackenburg, K., Bergs, J., Davidson, H., Ogden, H., et al. & Summerfield, C. |
| **Year** | 2025 |
| **Journal** | *Preprint* |
| **Link** | https://arxiv.org/abs/2509.05219 |

**What it's about:** National survey (N=2,499 UK voters) + RCTs during the 2024 UK election, comparing AI conversations to traditional internet search for political knowledge acquisition.

**Key findings:** AI conversations improved political knowledge and reduced misinformation at rates **comparable to traditional internet search** — a more optimistic counterpoint to papers showing LLMs reduce learning depth.

**Tags:** `User Behavior & Information Effects` `Misinformation & Fact-Checking`

---

## F. Democracy & Public Deliberation

---

### F12. Using LLMs to Enhance Democracy
| | |
|---|---|
| **Authors** | Lazar, S., & Manuali, L. |
| **Year** | 2024 |
| **Journal** | *Minds and Machines* |
| **Link** | https://link.springer.com/article/10.1007/s11023-026-09767-y |

**What it's about:** A philosophical and empirical analysis of whether LLMs can strengthen democratic deliberation and decision-making processes.

**Key findings:**
- LLMs are not suitable replacements for democratic decision-making
- They can strengthen the "informal public sphere" by improving information access
- They can help citizens hold leaders accountable through better-informed engagement

**Tags:** `Democracy & Public Deliberation`

---

### F18. LLMs, Truth, and Democracy: An Overview of Risks
| | |
|---|---|
| **Authors** | Coeckelbergh, M. |
| **Year** | 2025 |
| **Journal** | *Science and Engineering Ethics* |
| **Link** | https://link.springer.com/article/10.1007/s11948-025-00529-0 |

**What it's about:** A philosophical overview of epistemic and democratic risks posed by widespread LLM use, grounded in political philosophy and philosophy of technology.

**Tags:** `Democracy & Public Deliberation` `Misinformation & Fact-Checking`

---

---

## Thematic Cross-Reference Table

| Paper | Pol. Bias | Content Mod | Persuasion | Misinfo | User Behav | Democracy |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| A1 LLMs reflect ideology | ✓ | | | | | |
| A7 China censorship | ✓ | ✓ | | | | |
| A13 Truth & bias trade-off | ✓ | | | ✓ | | |
| A15 LLMs polarize Reddit | ✓ | | | | ✓ | |
| A29 Hidden Persuaders | ✓ | | ✓ | | | |
| B9 Longitudinal monitoring | | ✓ | | | | |
| B11 Speech suppression | | ✓ | | | | |
| B36 Model-dep. moderation | | ✓ | | | | |
| C6 Levers of persuasion | | | ✓ | | | |
| C8 Election denial | | | ✓ | ✓ | | |
| C20 Chat interventions | | | ✓ | | | ✓ |
| C22 Biased LLMs influence | ✓ | | ✓ | | | |
| C26 Microtargeting | | | ✓ | | | |
| C27 LLM messages persuade | | | ✓ | | | |
| C71 Persuasion benchmarks | | | ✓ | | | |
| D4 Fact-checking context | | | | ✓ | | |
| D56 Belief vs. fact | | | | ✓ | | |
| D57 Dunning-Kruger | | | | ✓ | | |
| D58 ThinknCheck | | | | ✓ | | |
| D70 @Grok fact-check | | | | ✓ | ✓ | |
| E3 LLM vs. search | | | | | ✓ | |
| E23 AI = search for knowledge | | | | ✓ | ✓ | |
| F12 LLMs enhance democracy | | | | | | ✓ |

---

## Tag Glossary (Dashboard Definitions)
- **Political Bias & Ideology** — Papers measuring or auditing LLM political lean, ideological consistency, or developer-embedded values
- **Content Moderation** — Papers testing LLMs as moderators, or auditing moderation APIs for bias/inconsistency
- **Persuasion & Political Influence** — Papers testing LLM persuasiveness and its effects on voter/political opinions
- **Misinformation & Fact-Checking** — Papers testing LLM factuality, claim verification, and misinformation correction
- **User Behavior & Information Effects** — Papers studying how LLM use shapes human learning, information processing, or knowledge
- **Democracy & Public Deliberation** — Papers examining LLMs' role in democratic discourse, deliberation, civic participation
- **Benchmarks & Evaluation** — Papers contributing datasets, methodologies, or evaluation frameworks
- **Penn Research** — Work produced by Penn-affiliated faculty or researchers

---

*Source: [Penn MEDIATED LLM Civic Discourse Dashboard](https://penn-mediated.github.io/LLM-Civic-Discourse/) — GitHub: [Penn-MEDIATED/LLM-Civic-Discourse](https://github.com/Penn-MEDIATED/LLM-Civic-Discourse)*

---

## High-Level Synthesis of the Literature

### Overview

The 71 papers in this collection collectively map a field at a critical inflection point: large language models have moved from being research curiosities to active participants in political information ecosystems, and the empirical record on what they actually do — and fail to do — is now substantive enough to draw meaningful conclusions. The literature converges on a set of recurring tensions that cut across all six thematic clusters.

---

### 1. LLMs Are Not Neutral Intermediaries

The most consistent finding across the political bias literature is that **LLMs carry identifiable ideological fingerprints**. Across more than a dozen independent studies using different methods — survey instruments, behavioral audits, opinion polling, user perception studies — virtually all major LLMs lean left of center on both social and economic dimensions (Rozado 2024; Westwood et al. 2025; Motoki et al. 2024; Santurkar et al. 2023). This lean is not random noise: it traces back to developer identity and geography (Buyl et al. 2026), is amplified by scale (Rettenberger et al. 2025), and can be deliberately engineered with surprisingly little fine-tuning data (Agiza et al. 2024; Rozado 2024).

Critically, this bias is not merely a property of the model in isolation — it propagates to users. Fisher et al. (2025, ACL) find that biased LLM outputs shift users' political decision-making even when users' own partisan identity is opposite to the model's lean. Potter et al. (2024) find that LLM interactions moved voters toward the Democratic nominee. And Nguyen et al. (2025) show that selectively curated input documents shift model outputs on immigration and crime — meaning whoever controls what an LLM "reads" holds indirect influence over what it "says." The picture that emerges is of a technology that launders political influence through a veneer of objectivity.

---

### 2. Content Moderation Is Both a Promising Application and a Major Equity Problem

The moderation literature is among the richest in the collection, and it presents a fundamental paradox: LLMs are powerful enough to be deployed for content moderation at scale, but consistent enough in their biases to make that deployment a civil rights concern.

On the capability side, fine-tuned small language models outperform much larger zero-shot models on community moderation tasks (Zhan et al. 2025); LLM agents effectively moderate decentralized networks (La Cava & Tagarelli 2025); and few-shot LLM approaches outperform commercial moderation APIs on harmful content detection (Bonagiri et al. 2025). The technical case for LLM-based moderation is real.

On the equity side, the findings are troubling. Fasching & Lelkes (2025, Penn) show that the same content receives radically different classifications depending on which of the seven leading moderation systems reviews it — the *choice of vendor alone* determines outcomes. Metaxa & Friedler (2025, Penn) demonstrate that all major moderation APIs suppress speech *about* identity groups at elevated rates, with disability and non-Christian content especially vulnerable. And Gomez et al. (2024) show that multiple equally accurate models can produce conflicting verdicts on the same post, introducing an irreducible arbitrariness with disparate impact across social groups.

The longitudinal work adds a further layer: Dai et al. (2025, Penn) show that companies quietly change their models' moderation behavior without public disclosure, and that only sustained external monitoring can detect those shifts. Accountability, in other words, cannot be assumed — it must be built.

---

### 3. LLMs Are Genuine Persuasion Machines — and This Is Alarming

The persuasion literature has produced some of the most striking findings in the collection. LLM-generated messages are as persuasive as messages from everyday people on highly polarized policy issues (Bai et al. 2024, *Nature Communications*). Across 19 models, post-training and prompting strategies increased persuasive power more than either model scale or personalization — and higher persuasiveness correlated with lower factual accuracy (Black et al. 2025, *Science*). A frontier model benchmark found that all seven tested models outperformed standard campaign advertisements, with Claude ranking as the most persuasive (Chen et al. 2026).

What makes these findings particularly consequential is that personalization — the microtargeting approach that has long been the focus of political advertising concern — appears not to add persuasive power beyond what generic LLM generation already achieves (Hackenburg & Margetts 2024). The threat is not sophisticated targeting of individuals; it is the baseline persuasive capacity of the technology, available to anyone with API access.

Importantly, persuasion is not inherently negative. Argyle et al. (2023, *PNAS*) show that AI-assisted conversation suggestions can improve the quality of cross-partisan dialogue. Hopkins et al. (2026) find that tailored LLM conversations can reduce belief in election denial claims, with the largest effects on the most committed believers. The same mechanisms that make LLMs dangerous as influence tools also make them potentially valuable for constructive civic communication — the difference lies in deployment intent and design.

---

### 4. Fact-Checking with LLMs Is Promising but Not Reliable Enough for High-Stakes Use

The fact-checking literature is the most technically detailed cluster in the collection, and its overall message is cautiously pessimistic. Standard LLMs perform poorly on real-world fact-checking tasks without curated context (DeVerna et al. 2025). Models cannot reliably distinguish first-person false beliefs from facts (Suzgun et al. 2025, *Nature Machine Intelligence*). Smaller models display high confidence despite low accuracy — a Dunning-Kruger pattern — while larger models are more accurate but more likely to refuse to answer (Qazi et al. 2026). GPT-4 refused to classify 43% of claims in one multilingual benchmark (Saju et al. 2025).

There are genuinely positive findings. Retrieval-augmented generation with curated sources substantially improves performance (DeVerna et al. 2025). Small reasoning-trained models like ThinknCheck can match or outperform much larger models when trained to reason before delivering a verdict (Rao et al. 2026, Penn). And in the wild, LLM-based fact-checking on X (Twitter) shifted user beliefs at rates comparable to professional fact-checking (Renault et al. 2025).

The consistency problem, however, runs deep. Across models, languages, and claim types, performance is highly variable. Models do better on false statements about topics with guardrails (COVID-19, political controversies) than on genuinely novel misinformation. Multilingual performance degrades sharply for lower-resource languages. These patterns suggest that current LLMs function as strong fact-checkers in narrow, well-covered domains but are unreliable in the long tail of claims where fact-checking capacity is most needed.

---

### 5. The Effects on Users Are Mixed — and the Stakes Are High

The user behavior literature is smaller but methodologically among the strongest in the collection. Melumad & Yun (2025, *PNAS Nexus*, Penn) provide seven-experiment evidence that using LLMs for learning produces shallower understanding than web search — and that this difference is driven by presentation format, not information availability. The concern is not that LLMs give wrong information but that they discourage the effortful engagement that produces durable knowledge.

At the same time, Luettgau et al. (2025) find that conversational AI raises political knowledge and reduces misinformation at rates comparable to traditional search among UK voters, and Wang et al. (2026) find that while LLMs increase ideological polarization on Reddit, they moderate *affective* tone — making discourse calmer even as it becomes more entrenched. Fan & Xu (2025) find similar emotional moderation in climate change discussions.

The pattern suggests a productive framing: LLMs may be better thought of as **discourse moderators** than information providers. They calm the emotional register of public conversation, but that calming effect coexists with — and may even enable — deeper ideological entrenchment. Whether that trade-off is desirable depends on which dimension of political discourse one prioritizes.

---

### 6. The Infrastructure of Accountability Is Underdeveloped

A thread running through all six thematic clusters is the observation that independent accountability mechanisms for LLM behavior in civic contexts are weak or absent. Models change behavior without disclosure (Dai et al. 2025). Moderation outcomes are arbitrary across vendors (Fasching & Lelkes 2025). Political biases are measurable but contested. Persuasive capacities are benchmarked only in research settings. And the tools for measuring LLM factuality, cultural bias, and identity-related suppression are themselves still being developed.

The methodological contributions in this collection — longitudinal auditing systems (Dai et al.), speech suppression benchmarks (Metaxa & Friedler), cultural adaptation frameworks (Havaldar et al.), political persuasion risk benchmarks (Chen et al.) — represent the infrastructure of that accountability layer being built, piece by piece. Whether it keeps pace with deployment is the central open question the literature poses but does not yet answer.

---

### Key Tensions for Future Research

| Tension | Papers in Conversation |
|---|---|
| LLMs inform vs. LLMs indoctrinate | Luettgau et al. (2025) vs. Fisher et al. (2025), Potter et al. (2024) |
| LLMs moderate discourse vs. LLMs polarize it | Fan & Xu (2025), Argyle et al. (2023) vs. Wang et al. (2026) |
| Persuasion as civic tool vs. persuasion as manipulation | Hopkins et al. (2026) vs. Chen et al. (2026), Hackenburg & Margetts (2024) |
| Accuracy as the right metric vs. legitimacy | Huang (2025) vs. Zhan et al. (2025), Bonagiri et al. (2025) |
| Truthfulness vs. political neutrality | Fulay et al. (2024) — a trade-off with no obvious resolution |
| Scalable moderation vs. equitable moderation | SLM-Mod, CoPE, etc. vs. Metaxa & Friedler (2025), Fasching & Lelkes (2025) |

---

*Source: [Penn MEDIATED LLM Civic Discourse Dashboard](https://penn-mediated.github.io/LLM-Civic-Discourse/) — GitHub: [Penn-MEDIATED/LLM-Civic-Discourse](https://github.com/Penn-MEDIATED/LLM-Civic-Discourse)*
