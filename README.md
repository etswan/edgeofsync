# Edge of Sync

**Collective transitions in dancing groups** · [edgeofsync.org](https://edgeofsync.org)

This project models the transitions in a closed-loop feedback system of human-to-human and human-to-audio coupled oscillations, where group movement generates music in real time alongside heart rate and both limb and agent-center locations. It asks when and how the collective shifts between synchrony states, whether those shifts track markers of altered states of consciousness (heart rate) with persistence (a psychological instrument), and whether collective synchrony carries longer-term consequences for wellbeing. Modeling aims are mechanistic specificity of transitions, estimating how near a transition the system is, and whether groups regulate that distance.

The project uses two complementary models:

- **The computational model** (theoretical) generates these dynamics from first principles. It is led by adaptive-network Kuramoto coupling, with the swarmalator family and Couzin zonal models adding spatial movement, and a closed loop through music the group generates as it dances.
- **The data-driven model** (analytical) will turn video recordings of dancing groups into per-dancer movement signals, feeding a pipeline that detects collective states, transitions, coupling and early-warning signals directly from the recordings. It is in development.

## Repository contents

| Path | Contents |
|---|---|
| `index.html` | Landing page |
| `theoretical/index.html` | The interactive computational model |
| `theoretical/Edge_of_Sync_About_the_Model.pdf` | Full model description: equations, parameters, results and the transition framework |
| `analytical/index.html` | Placeholder for the data-driven model |
| `assets/` | Images for the landing page |
| `js/` | Three.js r147 and OrbitControls, served locally |
| `CNAME` | Custom domain for GitHub Pages |

## The computational model

Each dancer is an oscillator with its own natural tempo and a position on a shared floor. Dancers couple their phases to those nearby, are drawn toward those in phase with them, and, with adaptive coupling on, learn whom to move with from their shared phase history. A song oscillator follows the group's mean phase and builds in strength as the group synchronizes, bringing in a low percussive beat, moving harmony and a melodic hook. The dancers hear the song a moment late and lean toward its beat, pulled most by the low percussion.

In the web model you can:

- choose **who is dancing**: strangers, professional dancers or friends;
- **click the floor** to release fog, which weakens what nearby dancers can see but not what they hear, or to scramble their rhythm, and read the impact analysis under the buttons;
- run a **coupling sweep**, watch the **early-warning** indicators and the **occupancy landscape**, and follow the group's trajectory in the **phase portrait**;
- adjust coupling, tempo spread, noise, movement rules, adaptive learning and the music's pull and memory.

Every element in the model is tagged in its Data and Sources section as a published model, a novel combination or an illustrative choice. The PDF sets out the mathematics in full.

## Python notebook

`Edge_of_Sync_Model.ipynb` is a Python version of the computational model that matches the web model. It runs single groups, compares the three groups, runs fog and scramble experiments with the same rules as the website, runs coupling sweeps, computes early-warning indicators and occupancy landscapes, and tests for two stable states at fixed coupling. It needs only `numpy` and `matplotlib`.

```python
m = DanceFloor('friends', seed=3, F=0.8, mem=15)
out = m.run(120)          # time series of R, S, coupling, song strength and more
```

## Status

The model's equations and parameter values are mechanistic assumptions; the values are illustrative and have not yet been calibrated against human data. Results reported in the documentation come from preliminary simulation runs and are labeled with the number of runs behind them. The documentation distinguishes established theory, implemented and observed results, and proposed mechanisms throughout.

## Running locally

The site is static. From the repository folder:

```bash
python3 -m http.server 8000
```

then open `http://localhost:8000`.

## License and credit

Released under the MIT License. Developed by Emma T. Swan.
