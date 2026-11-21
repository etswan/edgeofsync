# edgeofsync

**A computational model of collective transitions in a dancing group**

Live model: [edgeofsync.org](https://edgeofsync.org)

Edge of Sync models how a dancing group moves into and out of synchrony in a closed loop, where the dancers' own movement generates the music they hear. Each dancer is an oscillator with a natural tempo of their own, moving across a shared floor, and the strength of their coupling learns from their shared history. The model asks when and how the collective shifts between states of synchrony, from either direction, how near to a transition the group is at any moment, and whether groups hold themselves at that edge.

It is the generative counterpart to an experimental study that will track movement, sound and heart rate in dancing groups.

## What the model combines

- **Swarmalators** for movement coupled to phase, with heterogeneous tempos and optional self-propulsion
- **Couzin zones** (repulsion, alignment, attraction) as an alternative movement rule
- **Kuramoto phase coupling**, weighted by proximity
- **Adaptive (Hebbian) coupling**, with an optional plasticity lag for non-reciprocal learning
- **A closed loop through generated music**, whose pull on the dancers grows with how clearly a shared beat can be heard

## Measures

Phase synchrony (Kuramoto R), space-phase order (S), mean learned coupling, metastability, a quasi-potential landscape, early-warning signals (variance and autocorrelation), recovery time after a perturbation, and an up-and-down coupling sweep for hysteresis.

## Status

All parameter values are illustrative and not yet calibrated to dance data. The combination of adaptive coupling, swarmalators and a closed musical loop is a novel model built for this project.

## Running it

The model is a single page, `index.html`, using [three.js](https://threejs.org) r147 (included in `js/`). Open the page in a browser, or visit the live site. No build step is needed.

## Key references

- O'Keeffe, K. P., Hong, H., & Strogatz, S. H. (2017). Oscillators that sync and swarm. *Nature Communications, 8*, 1504.
- Yoon, S., O'Keeffe, K. P., Mendes, J. F. F., & Goltsev, A. V. (2022). Sync and swarm: Solvable model of nonidentical swarmalators. *Physical Review Letters, 129*, 208002.
- Couzin, I. D., Krause, J., James, R., Ruxton, G. D., & Franks, N. R. (2002). Collective memory and spatial sorting in animal groups. *Journal of Theoretical Biology, 218*(1), 1–11.
- Aoki, T., & Aoyagi, T. (2009). Co-evolution of phases and connection strengths in a network of phase oscillators. *Physical Review Letters, 102*, 034101.
- Scheffer, M., et al. (2009). Early-warning signals for critical transitions. *Nature, 461*, 53–59.

The full reference list is in the model's Data and Sources section.

## License

Code: MIT License (see `LICENSE`).
Text and figures: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

## Author

Model developed by Emma T. Swan.
