# Validation Corpora

Each registered corpus is self-contained:

```text
<corpus-id>/
  corpus.toml
  sources.lock.json
  data/
  features/
  golden/
  status.toml
```

`data/` is generated locally and ignored. Source locks, feature manifests, deterministic goldens, and generated status evidence are repository artifacts. A corpus may be release-required even when its source data is local-only; `local_only` describes data availability, not validation importance.

The public baseline corpora are `pubchem-1k` for small-molecule features and `pdb-100` for macromolecular features. They are the normal targeted release checks for features with applicable external parity contracts.

Broader validation uses `pubchem-100k`, `enamine-diversity`, and `pdb-1000`. `pl-rex` is a domain-specific small-molecule corpus. These larger corpora are intended for deliberate broad validation runs, not routine CI.

`pdb-100` is an exact prefix of `pdb-1000`. Historical `smoke`, `pubchem-100`, and `pdb-10` fixture directories may remain for internal regression or smoke-test use, but they are not registered validation corpora and do not appear in the generated dashboard.