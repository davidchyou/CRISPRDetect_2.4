# CRISPRDetect_2.4

This is the current version of CRISPRDetect (as running here http://bioanalysis.otago.ac.nz/CRISPRDetect, 2019). In this version, the following features were improved:

**Array-quality score is now in the GFF output**

Since the first CRISPRDetect release, the 'score' column was used to define the length of the CRISPR array, as well as the spacer and the repeat lengths, instead of the array-quality score. Because CRISPRDetect is a highly respected CRISPR-array predictor, many applications (e.g. CRISPRStudio) get CRISPR array lengths from the score column of the GFF file. 

To filter CRISPR arrays by array-quality score it is now in the GFF output. To retain the former "CRISPRDetect-GFF" format, array-quality scores are included in the GFF file in the comment column, as the new, "Array_quality_score" attribute.

**Correct array orientation prediction especially in Type-2 CRISPR-Cas systems**

CRISPRDetect uses a built-in repeat database to predict orientations of CRISPR-arrays predicted, along with other criteria such as the stability of any RNA folds. This was improved by updating the repeat database (July 2019), to include many more repeat sequences of published CRISPR arrays of all types, including many Type-2 CRISPR-Cas systems. 
