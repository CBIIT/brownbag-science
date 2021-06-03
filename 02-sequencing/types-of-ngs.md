# Types of NGS





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

