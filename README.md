# Amanita_thiersii and A. foetens
Code and data for A. thiersii/ A. foetens project. 

# Download genes from NCBI for other saprotrophic Amanitas
Genes: ITS, LSU, SSU, mitochondrial LSU, mitochondrial SSU

# Do alignment with MAFFT using the L-INS-i method
1. Local alignment = L-INS-i algorithm "$ mafft --auto --adjustdirectionaccurately input_file > output_file"

# After aligning with MAFFT, run IQtree on MAFFT alignments.
2. "for f in PATH/MAFFT_results/_*.fasta; do iqtree -s $f -m MFP -msub nuclear -bb 1000 -bnni -pre PATH/iqtree_output/${f##*/}; done"

# After IQtree, run "cat" to concatenate treefiles. 
3. cat "PATH/iqtree_output/* fasta.treefile > PATH/astral5gene/input5gene.trees"
 
# Then run ASTRAL.
4. "java -jar ~/Astral/astral.5.7.8.jar -i PATH/astral5gene/input5gene.trees -o PATH/astral5gene/output5geneastral.tre

# For details, see file "Code_5gene_trees.txt"
