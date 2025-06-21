pQ1: Les noms des compétitions de l’année 2025.

$\pi nomCompétition(\sigma dateDébut = 2025 (competition) $

Q2 : Les noms et pays des stations de plus de 2500 mètres.

$\pi nomStations,pays(\sigma altitude> 2500(stations)$

Q3 : Les noms et prénoms des skieurs suisses.

$\pi nomSkieur,prénomSkieur(\sigma pays = 'Suisses'(skieur) $

Q4 : Les noms, altitudes et pays des stations où a lieu la compétition 'Coupe d’Europe 2023-2024'.

$\pi nomStation, altitude, pays(\sigma nomCompétition = 'Coupe d’Europe 2023-2024')\bowtie {idStation}(lieux)\bowtie {idCompt}Competitions$

Q5 : Les noms, prénoms et rangs des skieurs autrichiens qui ont participé à la compétition
'Saalbach-2025'.

$\pi nomSkieur, prenomSkieur, rang(
    \sigma nomCompetition = 'Saalbach-2025' (COMPÉTITION) 
    \bowtie CLASSEMENT 
    \bowtie SKIEUR 
    \sigma nationalité = 'Autrichien'
)$


Q6 : Les noms, altitudes et pays des stations où n’a eu lieu aucune compétition.

$\pi nomStation, altitude, pays(STATION)
− 
\pi nomStation, altitude, pays(STATION \bowtie STATION.idStation = LIEU.idStation LIEU)$

Q7 : Les noms, prénoms et nationalités des skieurs ayant participé à toutes les compétitions. 

$\pi nomSkieur, prénomSkieur, nationalité(SKIEUR \bowtie CLASSEMENT)
÷ 
\pi idCompt(COMPÉTITION)$

**Nom :** Lemaitre 

**Groupe :** Groupe 4

**Année :** 1er

**IUT Le Havre - Cours GIT** 

### Compte-rendu TP1 Introduction GIT

Dans ce TP on apprend à travailler avec git. Et a mettre a jours notre git.


# Compte-rendu TP1 : Introduction à GIT

**Nom :** Lemaitre Valentin
**Groupe :** [4]  
**Année :** [2024-2025]  

**IUT Le Havre - Cours GIT**

---

## Objectifs du TP

Ce premier TP avait pour but de se familiariser avec l’outil de gestion de version **Git** en local, sans utiliser de dépôt distant comme GitHub. Les objectifs principaux étaient :

- Configurer Git avec une identité (nom et email) et un éditeur de texte.
- Créer un dépôt Git local avec `git init`.
- Ajouter et suivre les modifications d’un fichier texte (`README.md`).
- Comprendre les 3 zones de Git : *Working Directory*, *Staging Area*, *Repository*.
- Versionner un fichier source Java.
- Ignorer les fichiers compilés à l’aide d’un fichier `.gitignore`.

---

## Étapes réalisées

### 1. Configuration de Git

Configuration de l’identité et de l’éditeur avec :

```bash
git config --global user.name "Prénom Nom"
git config --global user.email "email@example.com"
git config --global core.editor nano```













