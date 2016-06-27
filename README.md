
##iBSTools
--
iBStools(integrated Bisulfite Sequencing Tools) is an integrated tools for comprehensive analysis of bisulfite sequencing reads including whole genome bisulfite sequencing(WGBS) and reduced representation bisulfite sequencing (RRBS). It is not only comprised of a serial of basic tools of bisulfite sequencing reads mapping and quality control, methylation ratio assessment and statistics at single-base resolution, but new advanced tools for DNA methylation patterns (under-methylated, inter-methylated and full-methylated regions) identification, annotation and heterogeneity assessment, as well as identification and clustering group analysis of differentially methylated regions of paired and multiple samples cohorts. iBStools provides a comprehensive suite  to perform a wide  variety of bisulfite sequencing analysis.

![workflow](https://github.com/methylation/iBSTools/blob/master/imgs/workflow.png "foo")

####Modules
--
iBSTools has four modules:
* **towig** - methylation level file to Wiggle format
* **pattern** - identification of methylation patterns  of genomic reigons
* **refumr** - identification of reference methyalted regions among mutiple methylomes.
* **dmr** - identification of differentially methylated regions among two groups

####Manual
--
* Simple Examples:

__Usage:__ Convert "H1_bismark.cov" into "wig" format. Methy counts is in col 5,unmethy counts is in col 6.

	towig --methy_unmethy 5,6 -i H1_bismark.cov -o H1_wig -n H1

__Usage:__ Identify methylation patterns from "H1_wig/".

	pattern -i H1_wig/ -o H1_pattern/ -n H1

__Usage:__ Identify reference methylation patterns regions from mutiple methylomes in "wig_list.txt".

	refumr -p UM -path ./software/iBSTools_v1.1.0/ -w wig_list.txt -o ref_UM

__Usage:__ Identify differentially methylated regions for a specific genomic regions between two groups of methylomes.

	dmr -r ref_UM/ref_UM.bed -rh 1 -w1 file_list_1.txt  -w2 file_list_2.txt -o diff


* More details please read the wiki[iBSTools wiki](https://github.com/methylation/iBSTools/wiki)

####Using Tips
--
1. If you use PBS(Portable Batch System) in your cluster server , **avoid to appoint relative path** for “-o,--outdir” and other parameters which need to assign path because workspace is changed when pbs file is submitted. 

2. wiggle format
More detail information in [UCSC Genome Browser: Wiggle Track Format (WIG)](http://genome.ucsc.edu/goldenPath/help/wiggle.html).

3. construction information
iBSTools is contructed in R3.1.3 and perl v5.16.3. 
and iBSTools is tested in R2.x and perl v5.10.x... 
iBSTools just employs basic funtions in R and perl. So almost all of versions of R and perl is available.

4. dependence relationship
towig is independent. Input could come from BSMAP,Bismark or ENCODE.
pattern is independent. 
refumr requires pattern.
