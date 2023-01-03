![Master GEONUM](https://mastergeonum.files.wordpress.com/2021/10/rvb_original.png)

# Master GEONUM - 2A3 - Gestion et traitement des données spatio-temporelles
***

Ce dépôt git contient les fichiers pour le cours "2A3 - Gestion et traitement des données spatio-temporelles" du Master [GEONUM](https://mastergeonum.org/programme/).



Ce document explique comment installer et configurer un environnement python avec conda et installer toutes les bibliothèques requises.

**Information** Pour ceux qui ont des difficultés à installer un environnement python sur leur ordinateur, vous pouvez simplement télécharger les fichiers des notebooks (`.ipynb`) à partir de ce dépôt et les exécuter à distance avec [Google Colab](http://colab.research.google.com) (*Compte Google requis*).

***

## 1. Installer conda

[Conda](https://conda.io/projects/conda/en/latest/index.html) est un système de gestion de paquets et d'environnement à code source ouvert. Il installe, exécute et met à jour rapidement les paquets et leurs dépendances. 
Nous l'utiliserons pour gérer l'environnement python et toutes les bibliothèques python nécessaires pour les tutoriels.
Il existe plusieurs façons d'installer conda sur votre ordinateur:
1. [Anaconda distribution](https://www.anaconda.com/products/distribution): fournit des applications GUI et de nombreux paquets de science des données déjà installés.
2. [Miniconda](https://docs.conda.io/en/latest/miniconda.html): un installateur minimal pour conda, sans application GUI
3. [Miniforge](https://github.com/conda-forge/miniforge): un autre installateur minimal pour conda, sans application GUI (recommandé pour les puces Mac M1 ou M2 (Apple Silicon))

## 2. Configurer un environnement Conda

### 2.1 Télécharger les fichiers de configuration

* Cloner ce dépôt github

```bash
git clone https://github.com/ludovicmoncla/master-geonum-tutorials.git
```

* 

### 2.2 Configurer l'environnement avec toutes les dépendances

* Créez un nouvel environnement appelé `geonum-velov-py39`

```bash
conda create -n geonum-velov-py39 python=3.9
```

* Activez l'environnement

```bash
conda activate geonum-velov-py39
```

* Installer le paquet fiona avec `conda` (cela permet d'éviter un problème lors de l'installation de geopandas avec `pip`)

```bash
conda install fiona=1.8.21
```

* Install dependencies with `pip`

```bash
pip install -r requirements.txt
```


## 3 Lancer le serveur jupyter

```bash
jupyter notebook
```