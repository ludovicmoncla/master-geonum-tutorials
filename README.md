![lyon2 geonum](https://perso.liris.cnrs.fr/lmoncla/GEONUM/fig/logos.png)

# Master GEONUM - 2A3 - Gestion et traitement des données spatio-temporelles
***

Ce dépôt git contient les fichiers pour le cours "2A3 - Gestion et traitement des données spatio-temporelles" du Master [GEONUM](https://mastergeonum.org/programme/).


L'objectif de ce tutoriel est d'appréhender la problématique d'analyse de données spatio-temporelles grâce à l'utilisation de librairies Python.
Pour cela nous allons travailler sur un cas d'étude visant la visualisation et le traitement des données de disponibilités des stations Vélo'v de la Métropole de Lyon. 

**Information** Pour ceux qui ont des difficultés à installer un environnement python sur leur ordinateur, vous pouvez simplement télécharger les fichiers des notebooks (`.ipynb`) à partir de ce dépôt et les exécuter à distance avec [Google Colab](http://colab.research.google.com) (*Compte Google requis*).

*******
Notebooks :
 1. [Exploration et manipulation de données en Python](https://github.com/ludovicmoncla/master-geonum-tutorials/blob/main/notebooks/01.velov-data-exploration.ipynb) [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](http://colab.research.google.com/github/ludovicmoncla/master-geonum-tutorials/blob/main/notebooks/01.velov-data-exploration.ipynb)
 2. [Analyse et visualisation de données spatio-temporelles](https://github.com/ludovicmoncla/master-geonum-tutorials/blob/main/notebooks/02.velov-maps.ipynb) [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](http://colab.research.google.com/github/ludovicmoncla/master-geonum-tutorials/blob/main/notebooks/02.velov-maps.ipynb)
 3. [Un peu d'intelligence artificielle](https://github.com/ludovicmoncla/master-geonum-tutorials/blob/main/notebooks/03.velov-dsc.ipynb) [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](http://colab.research.google.com/github/ludovicmoncla/master-geonum-tutorials/blob/main/notebooks/03.velov-dsc.ipynb)


*******
Cheat Sheets :
* [Pandas Cheat sheet](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf)
* [Python for Data Science Cheat sheet](https://www.utc.fr/~jlaforet/Suppl/python-cheatsheets.pdf) (Pandas, Matplotlib, Scikit-Learn, etc.)


*******

La suite de ce document explique comment installer et configurer un environnement python avec conda et installer toutes les bibliothèques requises.

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