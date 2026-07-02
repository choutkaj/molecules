# Validation Corpora

Each directory is self-contained:

```text
<corpus-id>/
  corpus.toml
  sources.lock.json
  data/
  features/
  golden/
  status.toml
```

`data/` is ignored except for `tiny`. Source locks and deterministic gzip goldens are committed.

Routine validation during coding should use the fast and medium corpora: `tiny`, `pubchem-100`, `pubchem-1000`, `pdb-10`, `pdb-100`, and `pl-rex`. The large corpora, `pubchem-100k` and `enamine-diversity`, are intended for occasional broad validation runs by a human or by an agent only when the larger run is explicitly needed.

`pubchem-100` is an exact prefix of `pubchem-1000`; `pubchem-100k` is an explicit large-run corpus, not a routine coding tier. `enamine-diversity` pins all 50,240 records, with SMILES packs for all records and SDF V2000 packs for the 47,359 V2000 source records. `pdb-10` is an exact prefix of `pdb-100`.
