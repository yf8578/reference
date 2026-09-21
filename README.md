# Genomic reference archive

This private repository stores a split `tar.zst` archive of the `reference` directory used for NIPT analysis.

The directory `reference/1KGP_EAS_reference_panel` is intentionally excluded. All other top-level entries, including hidden files, are included.

## Download and verify

Download every release asset into one directory, then run:

```bash
shasum -a 256 -c SHA256SUMS.txt
```

## Restore

```bash
cat reference.tar.zst.part-* | zstd -d | tar -xf -
```

This recreates the `reference` directory in the current directory.

`CONTENTS.tsv` lists the archived top-level entries and their original byte sizes.
