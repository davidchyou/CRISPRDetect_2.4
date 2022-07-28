# CRISPRDetect_2.4

This is an updated version of CRISPRDetect_2.2. In this version, the following shortcomings were addressed:

**Array-quality score was not in the GFF output**

Since the first CRISPRDetect release, the score column was used to keep the length of the CRISPR array, as well as the spacer and the repeat lengths, instead of the array-quality score as intended. Because CRISPRDetect is a highly respected CRISPR-array predictor, many applications (e.g. CRISPRStudio) get CRISPR array lengths from the score column of the GFF file. Therefore, for a very long period of time, the array-quality score was not in the GFF output, and the only way to get it is to parse it out from the text-output.

It is computationally easier to filter CRISPR arrays by array-quality score if the array-quality score is in the GFF output somewhere. By not destroying the highly respected "CRISPRDetect-GFF" format, array-quality scores are included in the GFF file in the comment column, as the new, "Array_quality_score" attribute.

**Incorrect array orientation especially in Type-2 CRISPR-Cas systems**

CRISPRDetect uses a built-in repeat database to predict orientations of CRISPR-arrays predicted, along with other criteria such as the stability of any RNA folds. While the orietation prediction is robust in general, there were reports that orietation prediction are often incorrect for CRISPR arrays of Type-2 CRISPR-Cas systems. This is largely due to the limited variety of Type-2 CRISPR repeats, 

This is improved by updating the repeat database, to include repeat sequences of published CRISPR arrays of all types, including those of the Type-2 CRISPR-Cas systems.
