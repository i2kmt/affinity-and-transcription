# Description

Every biology fan knows that the mechanisms behind a gene's transcription setting and regulation are quite complex. A factor that seemed interesting to me was the affinity between the DNA Binding Domain (DBD) of a transcription factor and the DNA promoter sequence of a gene. So, I decided to find a way to investigate it myself.
After a lot of thought, I looked into TP53 as a transcription factor and how different genes were expressed according to the DBD-promoter affinities.
 
## Prerequired knowledge on p53
Now, as transcription is extremely detailed and regulated by many factors, I think it is appropriate to note some basic and important characteristics of the p53 protein. [TP53](https://www.uniprot.org/uniprotkb/P04637/entry) is the main protein who regulates apoptosis (aka cell suicide). Although it regulates other proteins as an enzyme, p53 can also form tetramers (a-dimer-of-dimers) and become a transcription factor.

Let's separate a p53 mollecule in 3 parts:
1. N-terminus domain: At this place, p53 has 2 important transactivation domains: TAD1 and TAD2. These domains make it possible to other co-factor proteins to bind to p53. Binding of different co-factors has a different effect on gene expression.
2. DNA-Binding-Domain (DBD) (located in the "centre"): This is the most important domain of p53 as a transcription factor. The DBD is responsible for the protein-DNA binding between p53 and a gene's promoter. Like every transcription factor, p53 can "read" and bind to a specific DNA sequence (we will look more into this later on).
3. C-terminus domain: The C-terminus domain is responsible for the p53's tetramerization

## p53's DBD
p53's DBD is 5′-PuPuPuC(A/T)(T/A)GPyPyPy-3′, where Pu and Py represent purines and pyrimidines, respectively. This is knows as a "Half Site". As mentioned before, p53 acts like a transcription factor in a form of a dimer-of-dimers. This means that 2 p53 proteins bind together into forming a dimer and then two dimers bind together and form a tetramer. Each dimer can bind to a "Half Site". And so, the p53 tetramer's full transcription site is the same as two "Half Site".

![Pasted image 20221122231547](https://user-images.githubusercontent.com/117028076/211453267-75377ce8-d104-453f-bc64-51aa0d1d0166.png)

