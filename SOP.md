# bin-checkm
bin via metabat + checkM: Bigelow Specific

*only old metabat is on the shared modules, here I have download the most recent metabat to my homedir, and am runing from within the same folder, which is called "metabat". 
Tool link ( including download) foud here: https://bitbucket.org/berkeleylab/metabat

```cd metabat```
```./runMetaBat.sh --unbinned -v -m 1500 /home/jgoordial/Goordial_AtlantisMassif/All_sc_metagenomes/fixscaffolds.fa /home/jgoordial/Goordial_AtlantisMassif/Bowtie/70C3R1scaffolds.bam /home/jgoordial/Goordial_AtlantisMassif/Bowtie/69A4R1scaffolds.bam /home/jgoordial/Goordial_AtlantisMassif/Bowtie/69A9R2scaffolds.bam /home/jgoordial/Goordial_AtlantisMassif/Bowtie/68B1R1scaffolds.bam >metabatALLSclog.txt```

files will be output into a folder within the metabat working folder

```module use /mnt/scgc_nfs/opt/modulefiles/common/```
```module load checkm```

```checkm lineage_wf -f fixscaffolds.fa.metabat-bins1500/CheckM.txt -t 8 -x fa fixscaffolds.fa.metabat-bins1500/ fixscaffolds.fa.metabat-bins1500/SCG
checkm tree_qa fixscaffolds.fa.metabat-bins1500/SCG >fixscaffolds.fa.metabat-bins1500/tree_qa_out.txt```

Here will have an output of bins, with completeness, contamination estimates, and IDs based on marker genes. Note - Eukaryotic marker genes are not included in checkMs ID. 



