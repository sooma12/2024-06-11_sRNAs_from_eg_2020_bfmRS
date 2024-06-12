# 2024-06-11_sRNAs_from_eg_2020_bfmRS

1. Reads from EG:

```text
>> June 11th, 2024
Hi Mark, I put the raw fastq files on the cluster, here:
/work/geisingerlab/Eddie/151116-0034H_Edward_Geisinger/fastq_Lane2
could you give it a shot with your pipeline?
```

Reads were in .fastq.gz format.  Moved .fastq.gz files to ./data/rawreads and gunzipped.
Moved the "undetermined" .fastq.gz file to a subfolder

2. bowtie-build

Used FASTA file: /work/geisingerlab/Mark/rnaSeq/palethorpe_sRNAs_fixed_2024-05-30/ref/CP065432.1.fasta

3. Sample sheet

Two column sample sheet with sample name and fastq path

4. Bowtie2 aligner

- Used `--local` aligner mode
- 8 threads with `-p 8`
- `--no-unal` to shrink .sam files by dropping unaligned reads
- `-U $fq` passes one fastq file in paired end mode
- Outputs .sam files

5. Samtools



