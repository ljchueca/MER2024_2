# MER2024_2
Material for Master Course MER2024


Load an interactive mode in Arina cluster
```
interactive -n 4 -p vfast -r mer3
````

Load necesary modules
```
module load BCFtools/1.15.1-GCC-11.3.0
````
a) Conduct a PCA from of unlinked SNPs from 50 anchovy specimens

Compute a covariance matrix with PCAngsd (https://github.com/Rosemeis/pcangsd)

```
./pcangsd_hwe.sh Anchovy_data Anchovy_PCA 4
````

b) Estimate Admixture proportions with NGSAdmix (http://www.popgen.dk/software/index.php/NgsAdmix)

```
screen -S NGSadmix
````
```
./ngsadmix.sh Anchovy_data Anchovy_Admixture 2 10 4 1>./Anchovy_Admixture/ngsadmix.err 2>./Anchovy_Admixture/ngsadmix.log
````
