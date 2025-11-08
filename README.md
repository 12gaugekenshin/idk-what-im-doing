Note from the Author

This repository represents my concept and research idea, not a completed or original software implementation.
Much of the included code and structure was adapted, refactored, or inspired by open examples and community prototypes - the intent is to demonstrate the concept of using Kaspa as a backbone for AI provenance and energy accountability, not to claim authorship of every line.

Anyone is welcome to build on or improve the technical foundation.
My focus is on the ideology and design direction - how math, proof, and transparency can form the next layer of trust for AI systems.



Proof-of-Compute-Integrity (PoCI)

Proof-of-Compute-Integrity (PoCI) is a proposed verification framework that proves computation happened as claimed - with authentic inputs, code, data, and energy - and that the resulting artifacts remain unaltered.
Unlike Proof-of-Work, which measures raw energy expenditure, PoCI measures verifiable computational honesty: it links each compute event (such as model training or inference) to cryptographic hashes, signed attestations, and on-chain anchors.
In essence, PoCI transforms computation itself into a provable act of integrity, ensuring that every model, dataset, or result can be traced back to its true origin in both time and energy.

Kaspa–AI Provenance isn’t just a technical concept - it’s a statement of belief.
Proof-of-Compute-Integrity (PoCI) represents a world where truth in computation doesn’t come from reputation, branding, or authority - but from physics, energy, and math.
Every hash, signature, and timestamp forms a digital law of nature: what happened, happened.
By merging Kaspa’s time-energy consensus with transparent AI provenance, we move toward systems that are not only decentralized - but honest by design.


Kaspa–AI Provenance System

Anchoring Artificial Intelligence in Physics, Proof, and Transparency

Overview

This repository is an early-stage concept exploring how AI model provenance (origin, lineage, and training integrity) could be anchored to the Kaspa blockchain - using its high-throughput, proof-of-work DAG architecture to timestamp, verify, and secure model events.

It’s not a finished product - it’s an open foundation meant to inspire and enable builders, researchers, and Kaspa developers to expand on the idea.

Core Concept

Modern AI models are powerful but opaque.
We can’t easily prove:
Where the training data came from
What energy or compute was used
Whether weights or results were altered after training

The Kaspa–AI Provenance System aims to fix that by linking each model’s key lifecycle events directly to the Kaspa ledger.
That means every dataset, training checkpoint, and release can be verified through math - not trust.

How It Works

Each AI lifecycle event (training start, checkpoint, final release, evaluation) produces a signed JSON record containing:

File and dataset hashes

Code and hyperparameter hashes

Timestamp (Kaspa-aligned)

Optional off-chain storage references (IPFS / Filecoin)

These records can then be anchored on-chain to Kaspa via transaction payloads or RPC submissions, forming an immutable history of model evolution.

Features (Planned / Conceptual)

Event Schema for model lineage (Rust & Python examples included)

Hashing Utilities for datasets, weights, and training logs

Kaspa Timestamping — proof-of-existence through block inclusion

Ed25519 Signing for model ownership and integrity

Off-chain Artifact Storage (IPFS, Filecoin)

Async Event Broadcasting to Kaspa RPC nodes

Energy-Proof Integration (via KII / ZETA for carbon accounting)

Example Codes (I do not code! These examples were generated as a concept to further embody the idea! They probably will not work as I have no clue on developing / writing code!)

See /idk's for Rust and Python prototypes.
These (would if working) generate JSON events representing model checkpoints and compute proofs, ready for later integration with Kaspa RPC.

cargo run


Produces:

{
  "event_type": "TRAIN_START",
  
  "model_id": "kaspa_bert_v1",
  
  "data_hash": "9a3f...d2e",
  
  "timestamp": "2025-11-08T12:34:56Z"
}

Use Cases

AI Labs: verifiable model history and compliance trails

Compute Networks: proof-of-training or proof-of-inference

Energy Systems: carbon-accounted compute anchored to PoW

Open Research: public, immutable model records

Decentralized AI: machine-to-machine payment and trust

Vision

“Make intelligence accountable to physics, not PR.”
The long-term goal is to create a proof layer for AI - a transparent, physics-aligned infrastructure where truth about computation can’t be rewritten.

Contributing
This is an open research concept - feel free to fork, build, or extend it.
Contributions are welcome in:
Kaspa RPC integration
Key signing and validation layers
Storage abstraction (IPFS / Filecoin clients)
UI / Explorer for model lineage

License

Open-source under the MIT License - build, modify, and use freely with attribution.
