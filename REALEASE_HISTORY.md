##Release History

####v1.2.2 2017/3/9
* Fixed a bug which was caused by chromosome with no methylation value. [bed_mean_methy]
* Redesign data structure of methy matrix to improve the running speed(almost ten times). [bed_mean_methy]

####v1.2.1 2017/1/12
* Add a new tool "bed_mean_methy": caluculate mean methylation for predefined genomic regions.

####v1.2.0 2016/12/4
* Rewrite the tool "towig";
	1. count whole CGs in genome.(need to specify genome assembly file)
	2. count whole detected CGs, whole available CGs(>=depth threshold)
	3. methylation statics: mean methylation level.
	4. merge reads counts for a CG site in two strands.
* Support "bismark" file format.

####v1.1.4 2016/12/1
* Add format option '-t,--file_type', which could be specified "bismark", "bsmap", "roadmap", "custom" [towig]

####v1.1.3 2016/11/6
* Support .gz input format. [towig]
* Modify mannual for all modules.
* Fixed a bug when depth is zero. [towig]

####v1.1.2 2016/9/2
* Fixed a bug which was caused by UM_count was 0. [pattern]
* Support .wig.gz input format. [pattern]

####v1.1.1 2016/7/7
* Renamed the tool 'refumr' to 'refpattern'. 
* Fixed a bug which was caused by incomplete chromosome. [refpattern]
* Supported wig files seperated by 'comma'. [refpattern, dmr]
* Add example wig files. [refpattern]
* Check chromosome naming scheme. [refpattern]

####v1.1.0 2016/6/27
* Added a new tool 'dmr' to identify differently methylated regions for a specific region.
	1. calculation mean methylation for regions.
	2. remove regions with litter difference within group.
	3. identify regions with great difference between groups.

* Several code-cleanliness updates such as templated functions.

####v1.0.3 2016/5/1
* Fixed a bug that caused incorrect chromosome in Rscript. [refumr]
* Added a wig output file for bin signal.[refumr]

####v1.0.2 2016/4/28
* Fixed a bug that caused incorrect read for the wig file which has no track line or mutiple elements in declaration line. [pattern]

####v1.0.1 2016/4/26
* UMR < 0.1: UMR hotspot 0-0.1; mean methylation of region < 0.1 in hotspot extension; methylation on the edge position of UMR < 0.2. [pattern]
* Changed extended region to total region in calculation of mean methylation in methylated regions. [pattern]

####v1.0.0 2016/3/10
* Added a new tool 'towig' to coverted mutiple methylation level input file to wig file, modified from Normalization.
* Added a new tool 'pattern' to identify methylated pattern regions in bisulfite sequencing, modified from CpG_MPs2.1.2.
* Added a new tool 'refumr' to identify highly accurate umr among mutiple bisulfite sequencing methylomes.
