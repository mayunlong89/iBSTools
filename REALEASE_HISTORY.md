##Release History

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
