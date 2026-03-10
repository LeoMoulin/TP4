## 1.1.1

1.1.1.1 : Very unlikely, SHA-256 hasn't been proven to be crackable yet <br>
1.1.1.2 : I used AI to generate a python script to bruteforce and I found aac et ada have the same checksum, this is a collision <br>
1.1.1.3 : it is not recommended because they add additionnal data so we could have the same original file but not the same result <br>

## 2.2.1

2.2.1.1 : the size is 16.3 Kib, the permissions are -rwxr-xr-x, architecture x86-64. <br>
2.2.1.3 : No, because we output the build time which may differ <br>
2.2.1.4 : Yes <br>
2.2.1.5 : It works because we have the same architecture, if their machine had a different one, the output would have been different. <br>
2.2.1.6 : This is bad practice because someone who download a binary can't know what is inside <br>

## 2.3.1

2.3.1.1 : yes, it is because there is no seed <br>
2.3.1.2 : yes we get the same output, this is buildtime reproducible but not runtime reproducible <br>

## 2.4.1
2.4.1.1 : yes, because there is no macro, there is no preprocessing and this will give the same binary. <br>
2.4.1.2 : no, because we use the current time to generate a random number. <br>
2.4.1.3 : yes, because we have a seed <br>

## 2.6.1

2.6.1.2 : the estimation gets closer and the execution time rises, yes it is consistent <br>
2.6.1.3 : it's not buildtime reproducible because there is macros, the file montecarlobuildtime.c is an equivalent which is buildtime reproducible <br>
2.6.1.4 : it's not runtime reproducible because we use the current time to build the seed, the file montecarloruntime.c is an equivalent which is runtime reproducible <br>
2.6.1.5 : the file montecarloruntime.c is both buildtime reproductible and buildtime reproductible, this is because I removed every macro and the time printing <br>

## 3.3.1
3.3.1.1 : we need two parameters, Docker doesn't change that <br>
3.3.1.2 : with listing 7 we have ~277Mo and with listing 8, we have ~8,3Mo. Listing 7 is heavier as listing 8 uses multi stage build. The result is that in listing 7 all the builds tools are kept in the result but in listing 8 this is not the case.<br>
3.3.1.3 : the binary size is 16.4 KiB. The difference comes from the fact that the container also contains Alpine.<br>
3.3.1.4 : the purpose is, in a multi stage build, to copy files from a previous build stage into the final image.<br>

## 4.1.6
4.1.6.1 : yes <br>
4.1.6.2 : yes it is in /nix/store<br>
4.1.6.3 : yes because nix ensures deterministic builds <br>
4.1.6.4 : nix shells create a temporary environment but nix profile add the binary permanently<br>
4.1.6.5 : /nix/store contains all packets and their dependencies, this is immutable because we want to prevent accidental modifications.<br>
4.1.6.6 : nix flake lock ensures full reproducibility by binding dependencies to a fixed version. This makes sure every person running the program has the intended versions of the required packages.<br>
4.1.6.8 : with a flake file <br>
4.1.6.9 : yes, I should share the flake.lock file too. If I don't, the other students won't be able to fully reproduce the intended environment. <br>

### General questions 
1 : When we use Nix and we terminate the sessions, everything is remove from the computer. When we use docker or podman, we need to store the image and it takes space. <br>

