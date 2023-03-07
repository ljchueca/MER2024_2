# MER2023_2
Material for Master Course MER2023


Load an interactive mode in Arina cluster
```
interactive -n 2 -p vfast -r mer03
````

Load necesary modules
```
module laod BCFtools/1.15.1-GCC-11.3.0
````
a) Conduct a PCA from of unlinked SNPs from 50 anchovy specimens

Compute a covariance matrix with PCAngsd (https://github.com/Rosemeis/pcangsd)

```
./pcangsd_hwe.sh Anchovy_data Anchovy_PCA 2
````
