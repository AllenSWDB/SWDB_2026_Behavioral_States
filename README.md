# SWDB 2026 - Behavior States and Neural Encoding Workshop

Produced for: https://github.com/AllenInstitute/swdb_2026_student/wiki

Understanding how the brain controls behavior requires linking neural activity to the behavioral states that animals occupy at any given moment. This workshop examines how behavioral states shape sensory processing and neural encoding using mice performing a context-dependent decision-making task. **Neuropixels probes record brain-wide spiking activity** across cortex, hippocampus, striatum, and thalamus while mice switch between visual and auditory task contexts.

The [Dynamic Routing (DR) dataset](https://allenswdb.github.io/physiology/ephys/dynamic-routing/dynamic-routing-background.html) provides six-probe recordings from twelve mice. Sessions are stored as [Neurodata Without Borders (NWB)](https://www.nwb.org/) files (`.nwb.zarr` format) and accessed via [pynwb](https://pynwb.readthedocs.io/en/stable/).

---

## Workshops

**Workshop 1** - `code/Workshop1.ipynb` — *Tutorial on behavioral states*

* Load and explore NWB session files (trials table, behavioral signals)
* Examine how spontaneous behaviors co-vary with behavioral state
* Introduce Gaussian Hidden Markov Models (HMMs) and apply them to behavioral data 

**Workshop 2** - `code/Workshop2.ipynb` — *Tutorial on neuronal decoding*

* Introduce neural decoding with MOs neurons
* Fit a linear SVM to single-neuron then full-population spike counts
* Quantify decoder performance 

**Problem Sets** - `code/problem_sets.ipynb` — *Evening / homework exercises*

---

## Data

Sessions are stored under `data/dynamicrouting_datacube/`, one folder per session:
Twelve sessions are included.

```
data/dynamicrouting_datacube/
  ecephys_<subject>_<date>_<time>_nwb_<processed>/
    <subject>_<date>.nwb.zarr/   ← NWB session file (Zarr format)
    data_description.json
    subject.json
    ...
```
---

## Environment

Key dependencies (see `environment/Dockerfile`):

| Package | Version |
|---------|---------|
| `pynwb[zarr]` | 4.0.0 |
| `dynamax[notebooks]` | 1.0.2 |
| `scikit-learn` | (bundled) |
| `matplotlib` | 3.11.1 |
| `pandas` | 3.0.5 |

---

## Links

- **CodeOcean Capsule:** https://codeocean.allenneuraldynamics.org/capsule/
- **SWDB Student Wiki:** https://github.com/AllenInstitute/swdb_2026_student/wiki
- **DR Databook:** https://allenswdb.github.io/physiology/ephys/dynamic-routing/dynamic-routing-background.html

