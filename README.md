# Compositional Reinforcement Learning in Continuous Goal-Spaces

**Author:** Zukisa Mbuli  
**Degree:** Master of Science in Computer Science (with Distinction) 
**Institution:** School of Computer Science & Applied Mathematics, University of the Witwatersrand, Johannesburg  
**Supervisors:** Prof. Benjamin Rosman, Prof. Steve James, Dr. Geraud Nangue Tasse  
**Date:** September 2026  

📄 **[Read the Full Dissertation (PDF)](https://zakesman.github.io/compositional-rl-dissertation/compositional-rl-dissertation-zukisa-mbuli.pdf)**

---

## Abstract

The area of lifelong reinforcement learning has seen many advances in recent years especially through transfer learning. Among the transfer learning methods driving
these advances, logical composition of tasks and value functions is of particular interest, as it allows agents to construct solutions to novel tasks by combining policies
trained on simpler ones. Recent works have further extended this framework to zero-shot composition, enabling agents to generalise to unseen task combinations without
additional training. These methods nonetheless assume a discrete set of goals: while continuous state spaces are not precluded, they require an explicit, human-engineered
mapping from continuous states to a finite set of relevant goals. Our research addresses this problem by applying representation learning methods to it. Specifically,
we apply a form of variational autoencoder that uses vector quantization to discretize the latent space, rather than the Gaussian distribution used by regular variational autoencoders. This variational autoencoder is known as the Vector-Quantized Variational Autoencoder. Through the results we obtain, we establish that a model can be developed to achieve Boolean task composition through latent representations, despite lacking an oracle with explicit knowledge of environmental goals. This model functions
in a continuous goal space and handles high-dimensional perceptual inputs from the environment.

---

## Key Contributions

* **Unsupervised Visual Goal Representation Learning:** Develops a Vector-Quantized Variational Autoencoder (VQ-VAE) vision pipeline with entropy regularisation and Smith-Waterman sequence alignment to autonomously discover a finite, discrete latent representation of goals from raw, high-dimensional egocentric observations in a continuous 3D MiniWorld environment—without human labels or prior knowledge of the number of goals.
* **Compositional Reinforcement Learning with PPO:** Extends Boolean Task Algebra from value-based methods to an Actor–Critic framework using Proximal Policy Optimization (PPO), enabling zero-shot logical composition (`AND`, `OR`) of base skills over learned discrete goal codes.
* **Empirical Validation Against an Oracle Baseline:** Demonstrates that an agent operating purely from unsupervised visual representations achieves compositional task performance comparable to a baseline agent equipped with ground-truth oracle knowledge of environmental goals.

---

## Codebase Status

> **Note:** The experimental codebase, VQ-VAE training scripts, and PPO compositional agent implementation are currently undergoing cleanup and documentation. A link to the public code repository will be added here once released.

---

## Citation

If you find this dissertation useful in your research, please consider citing it:

```bibtex
@mastersthesis{mbuli2026compositional,
  author       = {Zukisa Mbuli},
  title        = {Compositional Reinforcement Learning in Continuous Goal-Spaces},
  school       = {University of the Witwatersrand, Johannesburg},
  year         = {2026},
  month        = {September},
  type         = {Master of Science Dissertation}
}
```

