# Introduction to GPSeq

Genomic loci Positioning by Sequencing (a.k.a. GPSeq, pronounced *gee-pea-seek*) is a next-generation sequencing-based technique that allows measuring the radial localization of genomic loci in a genome-wide manner. In other words, it identifies the position of genomic loci of interest along the nuclear radius.

GPSeq works by applying a controlled restriction enzyme diffusion on a cell population. Specifically, performing the genome restriction reaction at different time durations builds restriction waves that grow from the nuclear periphery towards its interior.

The genomic restriction waves are quantified via FISH by ligating restricted sites with a FISH-compatible adapter (a.k.a., YFISH adapter). Alternatively, a sequencing-compatible adapter can be ligated instead of the YFISH one. This adapter allows the production of one sequencing library per restriction duration (i.e., per condition).

Pre-processing of each sequenced library (i.e., FASTQ file) generates a BED file with one line per restriction site, containing the genomic coordinates of the site and the number of de-duplicated reads mapped to it.

Finally, we merge the BED files generated from all libraries to calculate a binned genome-wide centrality track (i.e., GPSeq score).

### Resources

* [GPSeq Paper](https://www.nature.com/articles/s41587-020-0519-y) (from publisher).
* [GPSeq Paper](resources/gpseq-paper.pdf) (pdf).
* [GPSeq Supplementary Information](resources/gpseq-si.pdf) (pdf).

In particular, we recommend reading the two Supplementary Notes to the paper (see Supplementary Information) to learn about GPSeq score calculation, and effects of enzyme-choice and coverage on the GPSeq score itself.
