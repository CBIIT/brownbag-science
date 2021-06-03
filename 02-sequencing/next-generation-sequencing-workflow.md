# Next-Generation Sequencing Workflow



**TAKE HOME MESSAGE**: There is a lot of work that happens after the Sequencer machine does its work



## (Extremely) Generic Steps

1. <u>Sample Preparation</u> 
   1. Obtain Sample from Patient, extract DNA from Sample
2. <u>Library Preparation</u>
   1. Fragment and Amplify Template DNA 
3. <u>Sequencing</u>
   1. Put in sequencer and run the machine
4. <u>Data Analysis</u>
   1. Short Reads from Sequencer (FASTQ)
   2. Mapped reads (BAM)
5. Output: Genetic sequence 





## Overall Steps - More Detail

* <u>Sample preparation</u> (extract DNA from biological sample)
* <u>Library Preparation</u>, Construction (chop up DNA into fragments)
* <u>Sequencing</u>
  * raw sequencing reads captured:  BCL
  * (on sequencer) BCL converted and then converted FASTQ
    * FASTQ = FASTA + quality info
      * Sequence identifier
      * Nucleotide sequence - aka the *read*
      * Phred quality info per base
* <u>Data Analysis</u>
  * Quality Control, including trimming and/or filtering reads ()
  * Align reads to reference genome: FASTQ --> SAM/BAM
  * Alignment Cleanup: BAM
  * Variant Calling (VCF)
  * Variant Annotation
    * Add information for each variant: symbol, name, transcript, amino acid sequence
    * COSMIC, dbSNP/1000 genomes, panel of normals, etc
  * Variant Filtering - Biological
    * In a clinical setting, usually no matched normal --> Remove unimportant variants 
    * Remove known germline variants in population; Improving databases (e.g. dbSNP -> 1000 genomes -> 1000 genomes -> SweGen)
  * Variant Filtering - Technical
    * VAR cutoff, read depth, variant quality score
    * Panel of normals
  * General Quality Control
    * Base quality, GC bias, distinct reads, percent reads mapped, mapping quality, average depth on target region, uniformity, etc





## Data Analysis

Steps in a typical next-generation resequencing workflow. *De facto* standard file formats are given in parentheses.

![image-20210603075529513](img-src/next-generation-sequencing.assets/image-20210603075529513.png)

(figure taken from [nature.com](https://www.nature.com/articles/hdy2016102.pdf))

---

Prev:  [05-Medical-Genetics.md](05-Medical-Genetics.md) 

Next:  [07-Types-of-NGS.md](07-Types-of-NGS.md) 

