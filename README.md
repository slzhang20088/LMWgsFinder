# LMWgsFinder

**`LMWgsFinder`** is a Perl script package (v5.26.2, built for x86_64-linux-thread-multi) designed to identify LMW-GS genes in the genomes of various wheat cultivars and related species, and to obtain related sequences and information. LMWgsFinder contains 34 Perl scripts and one Linux shell script, and requires the use of ncbi-blast-2.14.0+ and Linux system commands such as “cat”, “dos2unix”, “sed”,  etc to run properly.

**LMWgsFinder** is very easy to use. To get started, follow these steps:

1.  Place the genome sequence file, the corresponding CDS annotation file and the protein annotation file for the genome in the same directory as this package.
2.  Run the main script to start the analysis.

**Usage:**

Format：

perl  LMWgsFinder.v5.pl  genomeTopLevel.fa  genomeName(cannot contain '.')   genomeAnnotationCDS.fasta  genomeAnnotationPro.fasta

Example：
```
perl LMWgsFinder.v5.pl testDNAtoplevel.fa Tatest testCDS.fasta testPro.fasta
```
**LMWgsFinder** will automatically create a folder named `results` in the directory where this package is stored. If you see approximately 20 result files in this folder, it indicates that the package is running correctly and has processed the data as expected. These result files can be used for sequence analysis and experimental validation of LMW-GS genes.

Genomic sequence files, CDS sequence files, and protein sequence files must all be in Fasta format. The extension of the genome sequence file needs to be ".fa", while, the file extension of CDS and Pro needs to be '.fasta'. The naming of the four parameter files (the first being `genomeTopLevel.fa`, the second `genomeName`, the third `genomeAnnotationCDS.fasta`, and the fourth `genomeAnnotationPro.fasta`) does not have any special requirements, except that the name of the second parameter file cannot contain a period (`.`); otherwise, the program will not run correctly. Additionally, the order of these four parameter files must be preserved.
