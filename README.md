Gene: YCR009C Weinberg dataset
#declaring variables (represents columns in the dataset)
l<-235
i<-236
j<-237
k<-238

# 266 signifies the number of codons in the sequence
for(x in 1:266)
{
# sum of reads- row 14-28mer row 15-29mer row 16-28mer
codonfreq <- sum(sriv[14,i],sriv[14,j],sriv[14,k],sriv[15,i],sriv[15,j],sriv[15,k],sriv[16,l],sriv[16,i],sriv[16,j])
# incrementing the variables-triplet codon
i <- i+3
j <- j+3
k <- k+3
l <- l+3
# prints the codon position and its frequency
print(c(x,codonfreq))
}
