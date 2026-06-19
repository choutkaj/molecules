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
`pubchem-100` is an exact prefix of `pubchem-1000`; `pdb-10` is an exact prefix of `pdb-100`.
