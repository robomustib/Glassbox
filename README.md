# Glassbox

### A transparent neural network visualiser for the classroom
Glassbox is a browser-based educational tool that makes the inner workings of a small neural network visible in real time. Learners interact directly with the network — selecting input shapes, observing signal flow through hidden neurons, and training the weights through feedback — all without writing a single line of code.

The name reflects the core idea: instead of treating the network as a black box, every weight, every connection, and every decision is made visible.

---

## What it teaches

- **Signal flow:** how an input activates hidden neurons and produces an output prediction
- **Weights as memory:** how connection strengths encode what the network has learned
- **Backpropagation:** how confirming or correcting a prediction changes specific weights
- **Confidence:** why the network picks one output over another, expressed as a percentage

---

## How it works

A 5→3→5 network is displayed with input neurons (shapes), three hidden neurons, and output neurons (shapes). Learners click an input shape and the network immediately:

1. Propagates the signal forward through the hidden layer
2. Highlights the winner output neuron
3. Displays connection lines coloured by weight sign (green = positive, red = negative) and scaled by signal strength
4. Shows the weight panel for the active input, with exact values and change indicators

The learner then confirms the prediction (**Correct ✓**) or corrects it (**Wrong ✗**). Backpropagation runs and the weight panel updates, showing which connections became stronger or weaker and by how much. A plain-language explanation describes what just happened.

---

## Features

- Live SVG connection visualisation — line thickness reflects actual signal flow
- Winner path highlighted distinctly from background connections
- Per-input weight panel with bar charts, numeric values and Δ change indicators
- Plain-language explanation after every interaction
- Training log with full session history
- Accuracy tracker (correct / corrections / attempts)
- Single HTML file — no framework, no build step, no dependencies beyond Google Fonts
- WordPress-ready — all CSS classes scoped under `#gbnn-root`, no theme interference

---

## Network architecture

```
Input (5)  →  Hidden (3)  →  Output (5)
  ■               H1             ■
  ●               H2             ●
  ▲               H3             ▲
  ♦                              ♦
  ★                             ★
```

Weights are initialised randomly near zero. The network starts as a blank slate and learns entirely from user feedback.

---

## Educational context

Glassbox Network was developed as a didactic tool for technology and computer science education at secondary and post-secondary level. It is suited for learners who are ready to engage with the mechanics of neural networks — weight matrices, activation functions, and gradient-based learning — without requiring any programming background.

For a more accessible entry point aimed at younger learners, see the companion tool **AniMaL**, which teaches the same core concepts through an animal feeding game.

---

## Demo
Click here to try out:
[Glassbox Demo](https://www.mustafa-bilgin.de/neuronale-netze-2)
---
 
## License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** License.
Note: You are free to share and adapt the material for non-commercial purposes, provided you give appropriate credit. Commercial use is not permitted without prior consent. For details, see the [LICENSE](LICENSE) file.

Copyright (c) 2026 Mustafa Bilgin

## Citation

If you use this software for your research, please cite it using the DOI:

**APA Format (7th Ed.):**
> Bilgin, M. (2026). *Glassbox — A transparent neural network visualiser for the classroom* (Version 2.0.0) [Computer software]. Zenodo. [https://doi.org/10.5281/zenodo.xxxx](https://doi.org/10.5281/zenodo.xxx)

**BibTeX:**
```bibtex
@software{Glassbox,
  author       = {Bilgin, Mustafa},
  title        = {Glassbox — A transparent neural network visualiser for the classroom},
  year         = {2026},
  publisher    = {Zenodo},
  version      = {1.0.0},
  doi          = {10.5281/zenodo.xxxx},
  url          = {https://doi.org/10.5281/zenodo.xxxx}  

