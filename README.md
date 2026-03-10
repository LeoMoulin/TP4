1.1.1.1 : Very unlikely, SHA-256 hasn't been proven to be crackable yet



2.3.1.1 : yes, it is because there is no seed

2.3.1.2 : yes we get the same output, this is buildtime reproducible but not runtime reproducible

2.4.1.1 : yes, because there is no macro, there is no preprocessing and this will give the same binary.
2.4.1.2 : no, because we use the current time to generate a random number
2.4.1.3 : yes, because we have a seed
