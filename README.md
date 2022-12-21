# Amanita_thiersii
Code and data for A. thiersii project
# On 12/19/22 Anne requested I re-do analysis of 5-gene tree omitting genes from A. thiersii 10802 because they are too closely related to A. thiersii Skay4041_het. 
# (I think perhaps we should omit A. thiersii Skay4041_het and keep sequences from 10802 because 10802 includes all 5 genes and Skay4041_het only has two, but I would like your advice on that problem).
# For today, I omitted all 5 genes for 10802 in all five raw fasta files, then did alignment with MAFFT using two methods
# 1. Local alignment = L-INS-i algorithm (same as before) "$ mafft --auto --adjustdirectionaccurately input_file > output_file"
# 2. Global alignment = G-INS-i algorithm "$ mafft --globalpair --maxiterate 1000 --adjustdirectionaccurately input_file > output_file" (co-author Robledo indicated he usually used G-INS-i so I wanted to try it to see if it made a difference.)
# Output files of MAFFT have "global" in file name if they were produced with G-INS-i MAFFT algorithm
# After aligning with MAFFT, I ran IQtree on MAFFT alignments
# After IQtree, ran "cat" to concatenate treefiles 
# Then I ran ASTRAL
# Separately, I tried to re-run concatenate code from Mickey "Concatenate.code copy" but could not get it to work in Terminal.
