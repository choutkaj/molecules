# External Validation Corpora

This directory records optional large datasets used for local and long-running validation.

The actual large-corpus data belongs under `validation/data/`, which is ignored by git. Corpus
descriptors here define the canonical IDs used by feature metadata, validation manifests, status,
and dashboard columns.

Reference outputs are not generated in this step. RDKit and Biopython remain reference tools only and
must not become Rust runtime dependencies. `tiny` uses committed external records; all other corpora
must remain provenance-pinned even when their raw files are local.
