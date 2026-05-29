rediscovering of an idea already done, chunk out the embedding vectors into their head_size components and do self attention, then concatenate back together. works better when alternating with full attention blocks.
gemini says it works well for small datasets but does not scale well. it then tells me about monarch matrices as the fix. it allows parameter saving using small block diagonal matrices multiplied with a permutation 
matrix to get a full matrix. how is the permutation matrix not at the full size of a regular matrix though? i know you could shrink it because of its possible data type, but i assume you could do something like 
make list of positions where the ones would be instead. not sure how hardware treats that for matrix multiplication though. 
