---
title: Setup
---

Le cours Introduction à la modélisation des maladies infectieuses pour la santé publique a été développé par la Pontificia Universidad Javeriana pour les publics africains, dans le cadre de la stratégie de formation EpiTKit sous l’initiative Epiverse. Ce cours vise à renforcer les connaissances et les compétences en modélisation des maladies infectieuses et en analyse de données dans un contexte de santé publique.

## **CONTEXTE**  

Le projet **TRACE-LAC** (**Enhancing Tools for Response, Analytics and Control of Epidemics in Latin America and the Caribbean**) est financé par le **Centre de recherches pour le développement international (CRDI)**. Son objectif est de développer un **ensemble d’outils de données open-source et interopérables** pour l’analyse des épidémies, tout en favorisant une communauté d’utilisateurs engagée afin de soutenir les décideurs dans leur réponse aux épidémies en **Amérique latine**.  

La **Pontificia Universidad Javeriana** bénéficie du soutien du **CRDI** pour mener diverses activités et produire des résultats de recherche dans le cadre du projet **TRACE-LAC**. Dans cet effort, Javeriana a créé le **Epi Training Kit (EpiTKit)**, une **stratégie de formation en ligne en libre accès**.  

## **OBJECTIF GÉNÉRAL**  

**Traduire** et **adapter culturellement** les supports du **Epi Training Kit (EpiTKit)** pour les publics cibles en **Côte d’Ivoire, Gambie, Ghana, Kenya, Nigeria, Rwanda, Sénégal, Sierra Leone, Tanzanie et Togo**, en garantissant une **clarté linguistique**, une **précision technique** et une **pertinence culturelle**.  

### **Les cinq unités à traduire et adapter**  

1. **Introduction à la théorie des épidémies**  
2. **Épidémiologie générale**  
3. **Introduction aux statistiques et à la probabilité**  
4. **Paramètres**  
5. **Construction d’un modèle déterministe**  

## **INSTITUTIONS**

Pontificia Universidad Javeriana, le Medical Research Council Unit en Gambie et data.org.

Pour plus d'informations sur le projet, visitez notre page :
[Page du projet sur GitHub](https://epiverse-trace.github.io/translation-epitkit/)

## Règles du cours
Découvrez notre [Code de conduite TRACE-LAC](https://drive.google.com/drive/u/0/folders/1_rvQDFcniVR3nKVWGDIhzR6Bk-5lgN8J).

## Configuration logicielle

Suivez ces deux étapes :

### 1. Installer ou mettre à jour R et RStudio

R et RStudio sont deux logiciels distincts :

* **R** est un langage de programmation et un logiciel utilisé pour exécuter du code écrit en R.
* **RStudio** est un environnement de développement intégré (IDE) qui facilite le travail avec R. Nous recommandons d'utiliser RStudio pour interagir avec R.

Pour installer R et RStudio, suivez ces instructions <https://posit.co/download/rstudio-desktop/>.

::::::::::::::::::::::::::::: callout

### Déjà installé ?

Attendez ! C'est le bon moment pour vous assurer que votre installation de R est à jour.
Ce tutoriel nécessite **R version 4.0.0 ou ultérieure**.

:::::::::::::::::::::::::::::

Pour vérifier si votre version de R est à jour :

-   Dans RStudio, votre version de R sera affichée dans [la fenêtre de la console](https://docs.posit.co/ide/user/ide/guide/code/console.html). Ou vous pouvez exécuter `sessionInfo()`.

-   **- Pour mettre à jour R**, téléchargez et installez la dernière version depuis le [site web du projet R](https://cran.rstudio.com/) pour votre système d'exploitation.

    -   Après avoir installé une nouvelle version, vous devrez réinstaller tous les paquets.

    -   Pour Windows, le paquet `{installr}` peut mettre à jour R et migrer votre bibliothèque de paquets.

-   **Pour mettre à jour RStudio**, ouvrez RStudio et `cliquez sur Aide > Rechercher les mises à jour`. Si une nouvelle version est disponible, suivez les instructions à l'écran.

::::::::::::::::::::::::::::: callout

### Vérifier les mises à jour régulièrement

Bien que cela puisse sembler intimidant, il est **beaucoup plus courant** de rencontrer des problèmes en raison de versions obsolètes de R ou de paquets R. Se tenir au courant des dernières versions de R, RStudio et de tous les paquets fréquemment utilisés est une bonne pratique.

:::::::::::::::::::::::::::::

## Jeu de données

N'oubliez pas de les stocker dans le dossier **data** de l'emplacement de votre projet.

-   [Données](https://raw.githubusercontent.com/epiverse-trace/EpiTKit-FR/refs/heads/main/episodes/data/echantillon_covid.RDS)
