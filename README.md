# MER2023_2
Material for Master Course MER2023


Load an interactive mode in Arina cluster
```
interactive -n 2 -p vfast -r mer03
````

Load necesary modules
```
module load BCFtools/1.15.1-GCC-11.3.0
````
a) Conduct a PCA from of unlinked SNPs from 50 anchovy specimens

Compute a covariance matrix with PCAngsd (https://github.com/Rosemeis/pcangsd)

```
./pcangsd_hwe.sh Anchovy_data Anchovy_PCA 2
````

b) Estimate Admixture proportions with NGSAdmix (http://www.popgen.dk/software/index.php/NgsAdmix)

```
screen -S NGSadmix
````
```
./ngsadmix.sh Anchovy_data Anchovy_Admixture 2 10 2 1>./Anchovy_Admixture/ngsadmix.err 2>./Anchovy_Admixture/ngsadmix.log
````
