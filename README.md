1.1.1.1 : Very unlikely, SHA-256 hasn't been proven to be crackable yet


1.2.1.6 : 
2.3.1.1 : yes, it is because there is no seed

2.3.1.2 : yes we get the same output, this is buildtime reproducible but not runtime reproducible

2.4.1.1 : yes, because there is no macro, there is no preprocessing and this will give the same binary.
2.4.1.2 : no, because we use the current time to generate a random number.
2.4.1.3 : yes, because we have a seed

2.6.1.2 : the estimation gets closer and the execution time rises, yes it is consistent.
2.6.1.3 : it's not buildtime reproducible because there is macros, the file montecarlobuildtime.c is an equivalent which is buildtime reproducible.
2.6.1.4 : it's not runtime reproducible because we use the current time to build the seed, the file montecarloruntime.c is an equivalent which is runtime reproducible.
2.6.1.5 : the file montecarloruntime.c is both buildtime reproductible and buildtime reproductible, this is because I removed every macro and the time printing.

