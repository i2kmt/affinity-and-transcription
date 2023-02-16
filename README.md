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
After reading and studying many articles, I found that in a _first step_, p53 activates transciprtion of genes without interacting with other co-factors. Actually, co-factors get involved in transcription regulation afterwards in order to suppress or amplify it. [^3]

# Synthetic biology study[^1].
So my basic question, after learning the things stated above, I thought: "So how is actually transcription level regulated? How does one transcription factor have many targets which are all expressed in different levels?"

[^1]: Inga, A., Storici, F., Darden, T. A., & Resnick, M. A. (2002). Differential transactivation by the p53 transcription factor is highly dependent on p53 level and promoter target sequence. Molecular and cellular biology, 22(24), 8612-8625.
[^2]: McLure, K. G., & Lee, P. W. (1998). How p53 binds DNA as a tetramer. The EMBO journal, 17(12), 3342-3350.
[^3]: Verfaillie, A., Svetlichnyy, D., Imrichova, H., Davie, K., Fiers, M., Atak, Z. K., ... & Aerts, S. (2016). Multiplex enhancer-reporter assays uncover unsophisticated TP53 enhancer logic. Genome research, 26(7), 882-895.

