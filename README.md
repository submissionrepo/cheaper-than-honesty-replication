# Cheaper Than Honesty

Replication package for **Cheaper Than Honesty: Minority Coalitions Can Turn
Decentralized AI Evaluation into a Coin Flip**.

**[Download the complete replication package](https://raw.githubusercontent.com/submissionrepo/cheaper-than-honesty-replication/main/cheaper-than-honesty-replication.zip)**

The archive contains source code, saved experimental data, exact certificate
scripts and witnesses, the three paper figures, and reproduction instructions.

Download and extract the archive, then run from the extracted directory:

```sh
python smoke_test.py
python -m pip install -r requirements.txt
python research_ideas/bittensor_paper_b/figures/make_figures.py
```

The standard-library smoke test replays 36 official epoch fixtures and checks
integer emissions for 64 canonical and eight permuted coalition profiles.
Figure generation uses the saved finite LP values and the 3,000 saved policy
evaluations. Python 3.11 was used for the computations.

The archive's root `README.md` maps each paper result to its scripts and data.
It also explains how to rerun the finite LPs, replay the saved certificates,
and build the Rust 1.89.0 reference from the specified upstream sources.

The code targets Subtensor commit
`c004cebf360f4088187ee49d851dfb1a1eaaf710`. Upstream license texts and
attribution are included. The default-memory coalition experiment measures
one-epoch gains from the stated initial bonds; it does not include future
bond payments. Finite computations do not prove the universal theorems.
