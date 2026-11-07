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
| 3 | Deep Learning Core | Review | 15 |
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

## Review queue
- 03-deep-learning-core/06-optimizers — Adam default hyperparameters (lr=1e-3, b1=0.9, b2=0.999, eps=1e-8); momentum's effective lr = lr/(1-beta)
- 03-deep-learning-core/08-weight-initialization — init matches activation (sigmoid/tanh -> Xavier, ReLU/GELU -> Kaiming 2/fan_in); symmetry: identical init stays identical forever
