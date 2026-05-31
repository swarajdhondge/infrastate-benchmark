# InfraState Benchmark

A multi-domain benchmark for evaluating **LLM-based infrastructure state prediction** across Docker, Git, SQL, Python, npm, Terraform, Kubernetes, and cross-domain interactions.

> **Paper:** *Error Compounding in LLM-Based Infrastructure Simulation: A Multi-Domain Benchmark Study*
> Swaraj Dhondge (Independent Researcher)
> Preprint: https://zenodo.org/records/20479284 · DOI: [10.5281/zenodo.20479283](https://doi.org/10.5281/zenodo.20479283)
> *Preprint — a peer-reviewed version is planned.*

## What this is

A benchmark of **1,496 evaluation entries across 80 scenarios**, spanning seven infrastructure
domains plus cross-domain interactions, generated from **containerized real-tool execution with
ground-truth state capture**. It measures whether LLMs can track infrastructure state across
multi-step command sequences — the failure mode the paper calls *error compounding*.

**Domains:** Docker · Git · SQL · Python · npm · Terraform · Kubernetes · cross-domain

## Key findings

- **Single-step (teacher-forced):** a deterministic-first **hybrid** approach gives **+11.5 EM**
  over pure LLM prediction (*p* < 1e-6, Wilcoxon) at **63% lower token cost**.
- **Multi-step (auto-regressive):** models retain only **13–24%** of their teacher-forced
  accuracy, and the hybrid advantage collapses to **statistically insignificant** (*p* > 0.19).
- **Takeaway:** *error compounding, not model capability, is the bottleneck* for LLM-based
  infrastructure simulation. Five open models (7B–72B) evaluated under three conditions
  (pure LLM / hybrid / oracle).

## Access

The benchmark **dataset and evaluation harness are available on request**, not posted publicly.

This is deliberate: keeping the evaluation set out of public web crawls prevents it from leaking
into LLM training corpora, which would contaminate future evaluations. This is standard practice
for benchmarks whose value depends on remaining unseen by the models they test.

**To request access:**
1. Open a [**Benchmark Access Request**](../../issues/new?template=access-request.yml) issue.
2. Fill in your name, affiliation, intended use, and agree to the terms (research use, no
   redistribution, no use as training data).
3. The maintainer will follow up with an access link.

## Citation

If you use this benchmark, please cite the paper (see [`CITATION.cff`](CITATION.cff)):

```bibtex
@misc{dhondge2026infrastate,
  title        = {Error Compounding in LLM-Based Infrastructure Simulation: A Multi-Domain Benchmark Study},
  author       = {Dhondge, Swaraj},
  year         = {2026},
  doi          = {10.5281/zenodo.20479283},
  howpublished = {Preprint, Zenodo},
  url          = {https://doi.org/10.5281/zenodo.20479283}
}
```

## License

Repository contents (this README, citation metadata) are released under **CC BY 4.0**.
The benchmark dataset and harness are distributed separately under their own access terms,
communicated at the time of an approved request.
