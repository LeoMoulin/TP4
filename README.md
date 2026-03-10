## 1.1.1

1.1.1.1 : Very unlikely, SHA-256 hasn't been proven to be crackable yet
1.1.1.2 : I used AI to generate a python script to bruteforce and I found aac et ada have the same checksum, this is a collision
1.1.1.3 : it is not recommended because they add additionnal data so we could have the same original file but not the same result

## 2.2.1

2.2.1.1 : the size is 16.3 Kib, the permissions are -rwxr-xr-x, architecture x86-64.
2.2.1.3 : No, because we output the build time which may differ
2.2.1.4 : Yes
2.2.1.6 : This is bad practice because someone who download a binary can't know what is inside

## 2.3.1

2.3.1.1 : yes, it is because there is no seed
2.3.1.2 : yes we get the same output, this is buildtime reproducible but not runtime reproducible

## 2.4.1
2.4.1.1 : yes, because there is no macro, there is no preprocessing and this will give the same binary.
2.4.1.2 : no, because we use the current time to generate a random number.
2.4.1.3 : yes, because we have a seed

## 2.6.1

2.6.1.2 : the estimation gets closer and the execution time rises, yes it is consistent <br>
2.6.1.3 : it's not buildtime reproducible because there is macros, the file montecarlobuildtime.c is an equivalent which is buildtime reproducible <br>
2.6.1.4 : it's not runtime reproducible because we use the current time to build the seed, the file montecarloruntime.c is an equivalent which is runtime reproducible <br>
2.6.1.5 : the file montecarloruntime.c is both buildtime reproductible and buildtime reproductible, this is because I removed every macro and the time printing <br>

## 3.3.1
3.3.1.1 : we need two parameters, Docker doesn't change that
3.3.1.2 : 


