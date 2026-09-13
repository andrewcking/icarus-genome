# Icarus Genome Archive

This public archive preserves the reconstructed genome used by the interactive
memorial at [icarus.adrix.com](https://icarus.adrix.com).

Icarus was a male cat. His `genome-v1` release contains 39 reconstructed
sequences: two computational copies of each of the 18 feline autosomes, X, Y,
and the mitochondrial sequence. Every emitted position is an A, C, G, or T;
the reconstruction follows the memorial project's stated “best Icarus guess”
policy instead of masking uncertain positions with N.

These sequences are a reference-guided computational reconstruction from the
sequencing data supplied by Basepaws. They preserve two inferred autosomal
haplotypes where possible, but they are not a laboratory-finished, fully
phased assembly and `hap1`/`hap2` do not identify biological parents.

## Release contents

The [genome-v1 release](https://github.com/andrewcking/icarus-genome/releases/tag/genome-v1)
contains:

- `icarus.best-guess.39-sequences.fa.gz` — BGZF-compressed FASTA, 1,330,251,615 bytes
- `icarus.best-guess.39-sequences.fa.gz.fai` — FASTA coordinate index
- `icarus.best-guess.39-sequences.fa.gz.gzi` — BGZF block index
- `sequence-manifest.tsv` — record names, lengths, and reconstruction roles
- `SHA256SUMS.genome` — integrity hashes for the released genome artifacts

The primary archive SHA-256 is:

```text
a00c7b79a3da88590aad895568b94e0fff7a34da70ab085d16851ee86f6e9a67
```

The paired `.fai` and `.gzi` indexes let compatible tools and the memorial
retrieve a small coordinate window without downloading or decompressing the
entire genome.
