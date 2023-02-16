# Description

Every biology fan knows that the mechanisms behind a gene's transcription setting and regulation are quite complex. A factor that seemed interesting to me was the affinity between the DNA Binding Domain (DBD) of a transcription factor and the DNA promoter sequence of a gene. So, I decided to find a way to investigate it myself.
After a lot of thought, I looked into TP53 as a transcription factor and how different genes were expressed according to the DBD-promoter affinities.

# TP53's characteristics
### Prerequired knowledge on p53
Now, as transcription is extremely detailed and regulated by many factors, I think it is appropriate to note some basic and important characteristics of the p53 protein. [TP53](https://www.uniprot.org/uniprotkb/P04637/entry) is the main protein who regulates apoptosis (aka cell suicide). Although it regulates other proteins as an enzyme, p53 can also form tetramers (a-dimer-of-dimers) and become a transcription factor.

<p align="center">
 <img width=30% height=30% src="https://user-images.githubusercontent.com/117028076/211454328-2dc32395-75a8-48aa-8e19-9e96c9208090.png">
</p>

Let's separate a p53 mollecule in 3 parts:
1. N-terminus domain: At this place, p53 has 2 important transactivation domains: TAD1 and TAD2. These domains make it possible to other co-factor proteins to bind to p53. Binding of different co-factors has a different effect on gene expression.
2. DNA-Binding-Domain (DBD) (located in the "centre"): This is the most important domain of p53 as a transcription factor. The DBD is responsible for the protein-DNA binding between p53 and a gene's promoter. Like every transcription factor, p53 can "read" and bind to a specific DNA sequence (we will look more into this later on).
3. C-terminus domain: The C-terminus domain is responsible for the p53's tetramerization

### p53's DBD
p53's DBD is `5′-PuPuPuC(A/T)(T/A)GPyPyPy-3′`, where Pu and Py represent purines and pyrimidines, respectively. This is knows as a "Half Site". As mentioned before, p53 acts like a transcription factor in a form of a dimer-of-dimers. This means that 2 p53 proteins bind together into forming a dimer and then two dimers bind together and form a tetramer. Each dimer can bind to a "Half Site". And so, the p53 tetramer's full transcription site is the same as two "Half Site".[^2]

<p align="center">
 <img src="https://user-images.githubusercontent.com/117028076/211453267-75377ce8-d104-453f-bc64-51aa0d1d0166.png">
</p>

### p53 and transcription
After reading and studying many articles, I found that in a _first step_, p53 activates transciprtion of genes without interacting with other co-factors. Actually, co-factors get involved in transcription regulation afterwards in order to suppress or amplify it. [^3] Another really important thing to note is that p53's targeted genes are based only in accessible chromatin in euchromatin, which means that their transcription is not dependent on any chromatin unfolding-proteins nor mechanisms.

# Synthetic biology study[^1].
So my basic question, after learning the things stated above, I thought: "So how is actually transcription level regulated? How does one transcription factor have many targets which are all expressed in different levels?". Well, the answere seemed pretty obvious to me, leading me to investigate the affinity between a transcription factor's DBD and DNA-promoter-sequence of a targeted gene. Sadly, I did not find much bibliography who investigated this mechanism, but I did find a study [^1] which is noted below. Luckily, this paper provided to me enough information to run the tests that I wanted, which mainly included to measure the affinity between p53's DBD and different promoter sequences via JASPAR.

### The paper
In the paper that I based my litle project, they used _S. cerevisiae_ cells. By using methods of synthetic biology, they based a p53-dependent promoter behind the ADE2 gene. The ADE2 gene, can cause the colonies of the yeast to change colors from red to pink and to white according to it's expression rate. The number of p53-dependent promoters varied as they contained different promoter sequences of different genes that are targeted normally by p53 in mamalian cells (ex. p21, MDM2, GADD45). The article provides the different sequences that are recognized by p53, and the expression rate of ADE2 that was induced by the different promoters. 
<p align="center">
<img src="https://user-images.githubusercontent.com/117028076/219463221-bf82b61c-72b6-42e2-9bb7-579bd2ba532c.png"
     width="500" 
     height="333" />
</p>

# The project

### Method
I gathered all the different gene's promoter sequences that were provided by the paper [^1] and by using the choice "Scan" on JASPAR, I measured the affinity between TP53 and each sequence with p=80%. 

### Results

| Gene      | Promoter               | Score     | Relative score | Strand | Experimental rank | Affinity rank |
| --------- | ---------------------- | --------- | -------------- | ------ | ----------------- | ------------- |
| PIG3      | CAGCTTGCCCACCCATGCTC   | 10.128636 | 0.83730        | +      | 18                | 15            |
| IGF-BP3-A | AAACAAGCCACCAACATGCTT  | **-**     | **-**          |        | 17                | 18            |
| RGC       | GGACTTGCCTGGCCTTGCCT   | 11.504828 | 0.84722        | -      | 16                | 14            |
| cFOS      | GGACTTGTCTGAGCGCGTGC   | 8.817308  | 0.82136        | -      | 15                | 17            |
| BAX       | AGACAAGCCTGGGCGTGGGC   | 9.629974  | 0.83124        | +      | 14                | 16            |
| PA26      | GGACAAGTCTCAACAAGTTC   | 13.602616 | 0.86634        | +      | 13                | 12            |
| MDM2      | GGTCAAGTTGGGACACGTCC   | 12.834704 | 0.87019        | -      | 12                | 13            |
| NOXA      | AGGCTTGCCCCGGCAAGTTG   | 16.189728 | 0.88993        | -      | 11                | 9             |
| Cyclin    | AGGCTTGCCCGGGCAGGTCT   | 16.73818  | 0.89493        | -      | 10                | 7             |
| PUMA      | CTGCAAGTCCTGACTTGTCC   | 16.431227 | 0.91390        | +      | 9                 | 8             |
| AIP1      | TCTCTTGCCCGGGCTTGTCG   | 15.135793 | 0.89816        | -      | 8                 | 10            |
| PCNA      | GAACAAGTCCGGGCATATGT   | 17.172523 | 0.89889        | -      | 7                 | 6             |
| 14-3-3 σ   | TAGCATTAGCCCAGACATGTCC | 14.635928 | 0.89208        | +     | 6                 | 11            |
| HFAS      | TGGCTTGTCAGGGCTTGTCC   | 17.184814 | 0.92306        | -      | 5                 | 5             |
| GADD45    | GAACATGTCTAAGCATGCTG   | 20.14384  | 0.92598        | -      | 4                 | 3             |
| m-FAS     | GGGCATGTACAAACATGTCA   | 19.407656 | 0.95008        | +      | 3                 | 4             |
| TP53      | TGACATGCCCAGGCATGTCT   | 26.69956  | 0.98575        | +      | 2                 | 1             |
| P21       | CAACATGTTGGGACATGTTC   | 22.15398  | 0.94431        | -      | 1                 | 2             |

[^1]: Inga, A., Storici, F., Darden, T. A., & Resnick, M. A. (2002). Differential transactivation by the p53 transcription factor is highly dependent on p53 level and promoter target sequence. Molecular and cellular biology, 22(24), 8612-8625.
[^2]: McLure, K. G., & Lee, P. W. (1998). How p53 binds DNA as a tetramer. The EMBO journal, 17(12), 3342-3350.
[^3]: Verfaillie, A., Svetlichnyy, D., Imrichova, H., Davie, K., Fiers, M., Atak, Z. K., ... & Aerts, S. (2016). Multiplex enhancer-reporter assays uncover unsophisticated TP53 enhancer logic. Genome research, 26(7), 882-895.

