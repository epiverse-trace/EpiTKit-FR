---
title: Setup
---

Le cours d'introduction à la modélisation des maladies infectieuses pour la santé publique a été développé par la Pontificia Universidad Javeriana pour le continent africain dans le cadre de la stratégie de formation EpiTKit du projet Epiverse. Ce cours est conçu pour améliorer les connaissances et les compétences en modélisation des maladies et en analyse de données dans le contexte de la santé publique.

### Extension du kit de formation Epi : Une collaboration Sud-Sud pour des supports de formation multilingues et localisés en science des données pour la santé publique en Afrique

## **CONTEXTE**

Améliorer les outils de réponse, d'analyse et de contrôle des épidémies en Amérique latine et dans les Caraïbes (**TRACE-LAC**) est un projet financé par le **Centre de recherches pour le développement international (CRDI)** ayant pour objectif de créer une **boîte à outils de données de haute qualité, open-source et interopérable** pour l'analyse des épidémies — et de favoriser une communauté d'utilisateurs engagés — afin d'aider les décideurs à répondre aux épidémies en Amérique latine.

La **Pontificia Universidad Javeriana (Javeriana)** a été soutenue par le **CRDI** pour développer diverses activités et produits de recherche dans le cadre du projet **TRACE-LAC**. Dans le cadre de cet effort, la Javeriana a créé le **Kit de formation Epi (EpiTKit)**, une stratégie de formation en ligne **en libre accès**.

L'**EpiTKit** se compose d'une série de modules et d'unités pour la formation virtuelle en **science des données pour la santé publique** et en **modélisation des maladies infectieuses**, alignée sur l'**initiative Epiverse** dirigée par **data.org**. À ce jour, **10 unités** ont été développées en **espagnol**, adaptées aux publics d'**Amérique latine et des Caraïbes**.

Cette nouvelle phase, développée en **partenariat entre la Pontificia Universidad Javeriana et data.org**, étend la portée de l'**EpiTKit** à l'**Afrique** grâce à une **collaboration Sud-Sud**, en mettant l'accent sur le **multilinguisme** et le **localisme** dans la **traduction** et l'**adaptation culturelle** des supports de formation. L'initiative vise à renforcer les capacités locales en science des données pour la santé publique tout en favorisant l'échange de connaissances entre les régions confrontées à des lacunes et des défis épidémiologiques similaires.

## **OBJECTIF GÉNÉRAL**

**Traduire** et **adapter culturellement** les supports de l'**Epi Training Kit (EpiTKit)** pour le public cible en Côte d'Ivoire, en Gambie, au Ghana, au Kenya, au Nigeria, au Rwanda, au Sénégal, en Sierra Leone, en Tanzanie et au Togo, en assurant la **clarté linguistique**, l'**exactitude technique** et la **pertinence culturelle**. Cette initiative adopte une approche **multilingue** et de **localisme** pour créer des **expériences d'apprentissage sensibles au contexte** qui reflètent les **réalités locales de la santé publique** et renforcent les capacités régionales en science des données pour la réponse aux épidémies.

Cet objectif comprend :

-   **Traduction** et **adaptation** des supports de formation d'un ensemble initial de **cinq unités** développées par **Epiverse TRACE-LAC** en **anglais** et en **français**, tout en intégrant des **contextes locaux** et des exemples spécifiques à la région.

-   **Examen** de la terminologie technique pour assurer la cohérence, l'exactitude et la **pertinence pour les paysages épidémiologiques locaux**.

-   **Adaptation** et **production de ressources multimédias multilingues** qui sont culturellement appropriées et reflètent les diverses réalités des régions africaines.

Les cinq unités à traduire et adapter sont :

1.  **Introduction à la théorie des épidémies**

2.  **Épidémiologie générale**

3.  **Introduction aux statistiques et aux probabilités**

4.  **Paramètres**

5.  **Construction d'un modèle déterministe**

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

-   [Données](https://raw.githubusercontent.com/epiverse-trace/translation-epitkit/refs/heads/main/data/donnees_echantillon.RDS)
