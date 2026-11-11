# My AI Engineering Path
<!-- Managed by the ai-engineering-from-scratch learning skills.
     Repo: https://github.com/rohitg00/ai-engineering-from-scratch -->

## Mission
理解每天在用的 AI（understand the AI I already use daily）.
Build goal: 還不確定（not sure yet）.

## Placement
- Date: 2026-11-04
- Score: 7/10 (Math & Statistics 2/2, Classical ML 2/2, Deep Learning 1/2, NLP & Transformers 0/2, Applied AI 2/2)
- Entry point: Phase 7: Transformers Deep Dive
- Pace: ~2 h/week

## Path
| Phase | Name | Status | Est. hours |
|-------|------|--------|------------|
| 0 | Setup & Tooling | Skip | -- |
| 1 | Math Foundations | Skip | -- |
| 2 | ML Fundamentals | Skip | -- |
| 3 | Deep Learning Core | Done | 15 |
| 4 | Computer Vision | Skip | -- |
| 5 | NLP — Foundations to Advanced | Review | 30 |
| 6 | Speech & Audio | Skip | -- |
| 7 | Transformers Deep Dive | Do | 14 |
| 8 | Generative AI | Do | 14 |
| 9 | Reinforcement Learning | Do | 13 |
| 10 | LLMs from Scratch | Do | 26 |
| 11 | LLM Engineering | Do | 19 |
| 12 | Multimodal AI | Do | 65 |
| 13 | Tools & Protocols | Do | 76 |
| 14 | Agent Engineering | Do | 55 |
| 15 | Autonomous Systems | Do | 20 |
| 16 | Multi-Agent & Swarms | Do | 28 |
| 17 | Infrastructure & Production | Do | 34 |
| 18 | Ethics, Safety & Alignment | Do | 31 |
| 19 | Capstone Projects | Do | 620 |
| | **Total (Review + Do)** | | **1060** |

Note: Phase 5 is marked Review (not Skip) because the NLP & Transformers area scored 0/2.

## Progress log
| Date | Lesson | Quiz | Note |
|------|--------|------|------|
| 2026-11-05 | 03-deep-learning-core/01-the-perceptron | 3/3 | Mixed up AND gate with softmax; unsure why sigmoid replaces step (gradients) — revisit in backprop |
| 2026-11-05 | 03-deep-learning-core/02-multi-layer-networks | 3/3 | Warm-up: confused 'linearly separable' with linear feature-label relation; counted params by #layers not width; suggested ReLU (lesson 04) |
| 2026-11-05 | 03-deep-learning-core/03-backpropagation | 3/3 | Hand-computed full backward pass correctly; sign slip on update direction (w - lr*negative grad -> w increases); needed topological sort explained before Q3 |
| 2026-11-05 | 03-deep-learning-core/04-activation-functions | 3/3 | Fixed sign slip from last lesson (warm-up); solid on linear collapse and dead ReLU neurons; softmax now placed correctly as output-only |
| 2026-11-07 | 03-deep-learning-core/05-loss-functions | 2/3 | Strong on CE vs MSE gradients and softmax gradient p-y; mistook label smoothing for an LR schedule in quiz |
| 2026-11-07 | 03-deep-learning-core/06-optimizers | 2/3 | Asked what RMSProp is for (per-parameter step scaling); got bias correction; unsure why momentum lr=0.05 stalled (effective lr x10); didn't recall Adam defaults |
| 2026-11-07 | 03-deep-learning-core/07-regularization | 2/3 | Asked what a batch is; needed BatchNorm vs LayerNorm re-explained (row vs column) before Q1; thought model.eval() enables gradients; warm-up missed Adam defaults again |
| 2026-11-07 | 03-deep-learning-core/08-weight-initialization | 2/3 | Thought identical-init neurons would diverge after updates (they stay identical forever — showed demo); got Var(w)=1/fan_in and ReLU halving; picked 'small dataset' for when to use Xavier |
| 2026-11-08 | 03-deep-learning-core/09-learning-rate-schedules | 3/3 | Classified lr 0.1/0.6/1.1 on x^2 correctly; good warmup reasoning; needed 1cycle explained before Q2; warm-up cleared init review item |
| 2026-11-09 | 03-deep-learning-core/10-mini-framework | 3/3 | Said code is less familiar; thought Sequential.parameters() returns 1 (it's a flat list, 65 here) and described ReLU/Dropout behavior instead of 'no params'; training-loop order explained via dependency chain before quiz |
| 2026-11-10 | 03-deep-learning-core/11-intro-to-pytorch | 3/3 | Got batch tensor shapes; said W is (32,256) — weights don't depend on batch, W=(256,784); asked why GPU suits matmul (independent cells -> parallel). torch not installable in cloud env, used lesson-3 values |
| 2026-11-10 | 03-deep-learning-core/12-intro-to-jax | 3/3 | Missed both warm-ups (autograd = autodiff engine; no_grad = no graph tracking, not freezing) -> chose a quick PyTorch review first, then got deployment check right; solid on grad/vmap/jit roles. jax not installable in env |
| 2026-11-10 | 03-deep-learning-core/13-debugging-neural-networks | 2/3 | Good on overfit-one-batch as a control test; thought it fails due to local minimum (it only proves capacity, not absence of bugs); picked 'overfitting' for val flat from step 0 (suspect data pipeline). Used numpy demo since torch unavailable |
| 2026-11-11 | 05-nlp-foundations-to-advanced/01-text-processing | 2/3 | Predicted regex splits of 12.3/q8h and step-1a rule-order swap correctly; lemmatize missed watched (no ed rule) and (ran,NOUN) table miss; spaCy fix = built-in POS tagger; quiz picked spaCy for transformer pipeline |
| 2026-11-11 | 05-nlp-foundations-to-advanced/02-bag-of-words-tfidf | 2/3 | Warm-up: said ponies->ponie (ies rule gives poni). Got df/IDF (the=1), long-doc bias without L2; thought stop_words='english' keeps 'no' (it removes no/not/of/without); asked for full vectorizer-param walkthrough; quiz picked PCA for TF-IDF-weighted embedding |

## Review queue
- 03-deep-learning-core/06-optimizers — Adam default hyperparameters (lr=1e-3, b1=0.9, b2=0.999, eps=1e-8); momentum's effective lr = lr/(1-beta)
- 03-deep-learning-core/11-intro-to-pytorch — autograd (automatic differentiation engine) vs torch.no_grad() (skip graph tracking at inference) vs model.eval() (dropout/BatchNorm behavior)
- 03-deep-learning-core/13-debugging-neural-networks — val loss flat from the start = suspect data pipeline (train/val mismatch), not classic overfitting; overfit-one-batch is a screen, passing doesn't prove no bug
- 05-nlp-foundations-to-advanced/01-text-processing — transformer pipelines use the model's own paired tokenizer (token IDs must match the embedding vocab), not spaCy/NLTK; lemmatization needs correct POS
- 05-nlp-foundations-to-advanced/02-bag-of-words-tfidf — TF-IDF weighted embedding = weighted average of token embeddings using TF-IDF scores as weights; sklearn stop_words='english' deletes negations (no/not/without)
