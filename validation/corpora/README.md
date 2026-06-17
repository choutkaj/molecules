# External Validation Corpora

This directory records optional large datasets used for local and long-running validation.

The actual data belongs under `validation/data/`, which is ignored by git. Corpus manifests here
should describe provenance, expected local layout, intended validation tiers, and known caveats.

Reference outputs are not generated in this step. RDKit and Biopython remain reference tools only and
must not become Rust runtime dependencies.
