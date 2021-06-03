# Types of NGS



|                                    | Sanger | MiSeq | HiSeq | NovaSeq |
| ---------------------------------- | ------ | ----- | ----- | ------- |
| Reads (millions) from a single run | 0.0004 | 30    | 3,000 | 13,000  |
| Gigabases/day                      | 0.001  | 7     | 500   | 4000    |

also see [cost of sequencing](genome-size.md)



|                                   |                          | **Illumina**  |               |                            |                 |                      |                        |                          |
| --------------------------------- | ------------------------ | ------------- | ------------- | -------------------------- | --------------- | -------------------- | ---------------------- | ------------------------ |
|                                   | **Sanger**               | **MiSeq**     | **NextSeq**   | **HiSeq**                  | **NovaSeq**     | **Ion Torrent**      | **PacificBiosciences** | **OxfordNanopore**       |
| **Throughput range per run (Gb)** | *c*. 0.0005              | 10–15         | 10–120        | 1000–1800                  | 2000–6000       | 1–15                 | 0.5–10                 | 0.1–1                    |
| **Read length**                   | Up to 1 kb               | 300           | 150           | 150                        | 250             | 200–400              | up to 60 kb            | up to 100 kb             |
| **Read type**                     | SR                       | SR, PE        | SR, PE        | SR, PE                     | SR, PE          | SR                   | SR                     | SR                       |
| **Error rate (%)**                | 0.001–1                  | 0.8           | 0.8           | 0.2                        | 0.2–0.8         | 1–2                  | 13                     | 5–40                     |
| **Error type**                    | Substitutions            | Substitutions | Substitutions | Substitutions              | Substitutions   | Indels, homopolymers | Indels                 | Indels, deletions        |
| **Advantages**                    | Read accuracy and length | Read length   | Throughput    | Throughput, low error rate | High throughput | Speed, read length   | Speed, read length     | Read length, portability |

also see [another comparision](https://www.intechopen.com/books/next-generation-sequencing-advances-applications-and-challenges/next-generation-sequencing-an-overview-of-the-history-tools-and-omic-applications#T1)



|            | Advantages                                                   | Limitations                                                  | Examples                                                     |
| ---------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Short-Read | · Higher sequence fidelity<br/>· Cheap  <br/>· Can sequence fragmented DNA | · Not able to resolve structural variants, phasing alleles or distinguish highly homologous genomic regions<br />· Unable to provide coverage of some repetitive regions | * Ion Torrent<br />* 454<br />* Illumina<br />* SOLiD<br />* cPAS<br />* MPSS<br /> |
| Long-Read  | · Able to sequence genetic regions that are difficult to characterize with short-read seq due to repeat sequences<br />· Able to resolve structural rearrangements or homologous regions<br />· Able to read through an entire RNA transcript to determine the specific isoform<br />· Assists *de novo* genome assembly | · Lower per read accuracy<br />· Bioinformatic challenges, caused by coverage biases, high error rates in base allocation, scalability and limited availability of appropriate pipelines | Pac-Bio (2nd)<br />* Single molecule real time sequencing (3rd Gen)<br />Nanopore (3rd Gen) |

(adapted from [technologynetworks.com](https://www.technologynetworks.com/genomics/articles/an-overview-of-next-generation-sequencing-346532), [wikipedia.org](https://en.wikipedia.org/wiki/DNA_sequencing))



Also: 

* Whole-genome vs Whole-exome sequencing

* Whole-exome (DNA sequencing) vs RNA-Seq (RNA sequencing)

  


---



Illumina Sequencing

- 90% of sequencing market
- millions to billions of reads per run
- 300 to 600 bases per read
- high fidelity > 99.9% accuracy
- can do $1000 genome in 48 hours
- Issues/limitations
  - length limits - limited to 300 bases (errors from chemistry adds up)
  - some lagging, some jumping ahead
  - sometimes hard to tell clusters apart
  - able to detect differences in clusters when differences occur, look in middle
  - colors can be similar (blue, green, yellow) close to each other in frequency



**II. Long-Read Sequencing (Nanopore)**

* single strand of dna is threaded through pore, current is measured

- high error rates (10-15%)

- - errors are biased

- can read RNA directly

- really long reads (2 Mb)

- extremely portable (can be done in field), very small device! 

- See Nature Review Drug Discovery vol 1, p. 77-84 (2002)



**III. PacBio (also synthesis based sequencer)**

different chemistry

- no blocker
- fluorescent group is on phosphate group)
- 4 bases, four colors
- camera monitors image in real time
- 1 to 8 million wells
- long reads (100kb)
- High error rates (10-15%)
  - errors are random! (good)
  - if you sample same fragment several times, errors go away with consensus sequence
  - can yield accuracy of 1:1000 to 1:10,000 (which exceeds illumina sequencing accuracy)
- nature review genetics 11, 31-46 (2010)



CONS:

- harder to prepare
- cost more

PROS

- if you want to assemble new genome (no reference sequence), MUCH easier

- - (sometimes you get structural variants in short reads, sequences are inverted)

- much better at structural variation detection (important for certain cancers)

- phase variation: which variant are on which chromosome?

- - can be difficult to determine if mutation is on chromosome A or chromosome B (we get two)

