# tdna-insertion

Hello! This repository holds the jupyter notebooks files that I used to complete my honors project at Park University concerning the insertion of T-DNA into plant genomes by the pathogenic Agrobacterium tumefaciens. In essence, we used previously generated sequences of sites of T-DNA insertion in Arabipsis thaliana to train machine learning models. We found that trained models could accurately predict whether or not an unlabelled sequence from A. thaliana was a site of insertion or not.

Here is a short description of each of the files in the repo:

# TDNA-Preprocessing.ipynb

This file was used to take sequences in the GenBank Full format and scrape out relevant data including the sequence and whether the sequence was on the left or right side of T-DNA insertion. It then generated cases of "no insertion" by randomly selecting sequences from the A. thaliana genome and formatted all samples in a Pandas DataFrame that was interpretable for Sci-Kit Learn's classifiers.

# TNDA-GCPlotter.ipynb

This file can take lists of sequences and plot the distributions of GC content using matplotlib. It can also run a Mann-Whitney U test between two distributions.

# TDNA-MLOptimizationRIGHT.ipynb and TDNA-MLOptimizationLEFT.ipynb

This file was used to train and optimize several types of machine learning models for lists of sequences to the right and left of insertion sites, respectively. Additionally, these files were used to benchmark models using ROC curves and confusion matrices.

# TDNA-PermutationAnalysis.ipynb

Feature importance was computed in this file by taking each feature, randomly permuting the data in only that feature across all samples, and measuring the resulting loss in model accuracy. The loss is plotted for each feature using matplotlib. Becuase sci-kit learn's permutation analysis functions were not made to handle data that has been encoded using one-hot encoding, a custom function was used.

# Acknowledgements

Thank you to Dr. Azin Agah who advised met through this project! 

All sequences used in this project were taken GenBank and were generated as a result of the following studies:

Brunaud, V., Balzergue, S., Dubreucq, B., Aubourg, S., Samson, F., Chauvin, S., Bechtold, N., Cruaud, C., Derose, R., Pelletier, G., Lepiniec, L., Caboche, M., & Lecharny, A. (2002). T‐DNA integration into the Arabidopsis genome depends on sequences of pre‐insertion sites. EMBO Reports, 3(12), 1152–1157. 

Li, Y., Rosso, M. G., Ülker, B., & Weisshaar, B. (2006). Analysis of T-DNA insertion site distribution patterns in Arabidopsis thaliana reveals special features of genes without insertions. Genomics, 87(5), 645–652. 

Ortega, D., Raynal, M., Laudié, M., Llauro, C., Cooke, R. W. I., Devic, M., Genestier, S., Picard, G., Abad, P., Contard, P., Sarrobert, C., Nussaume, L., Bechtold, N., Horlow, C., Pelletier, G., & Delseny, M. (2002). Flanking sequence tags in Arabidopsis thaliana T-DNA insertion lines: a pilot study. Comptes Rendus Biologies. 

Samson, F., Brunaud, V., Balzergue, S., Dubreucq, B., Lepiniec, L., Pelletier, G., Caboche, M., & Lecharny, A. (2002). FLAGdb/FST: a database of mapped flanking insertion sites (FSTs) of Arabidopsis thaliana T-DNA transformants. Nucleic Acids Research, 30(1), 94–97
