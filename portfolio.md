# Portfolio - Kevin Voisin

# Compétences

Ensemble des démonstrations structurées par domaine de compétence selon le référentiel 304.

## Ingénierie informatique

# Analyser un problème informatique complexe

- J’ai analysé la problématique GenAI en détaillant ses composantes avec une granularité adaptée (qualité visuelle, robustesse SSH/Flask/SLURM, contraintes GPU, dépendances), comme le montre le [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4), où les contraintes et leurs interactions sont explicitées.
- J’ai identifié les opportunités techniques en comparant de manière structurée plusieurs solutions (TEXTure, Paint-it, Text2Tex, SDFusion, MV-Adapter) dans [llm-design-research.pdf](./data/llm-design-research.pdf), avec des critères et compromis formalisés.
- J’ai analysé une contrainte précise en évaluant l’impact de FreeU à protocole constant dans le [Rapport comparatif FreeU / sans FreeU](https://typst.app/project/rSFXN1Spr2ZphkfMR5s9yk), ce qui isole la variable testée et renforce la validité de l’analyse.

# Concevoir une solution théorique modélisée

- J’ai conçu une architecture de pipeline complète (client local, SSH/API Flask, SLURM sur Disco, retour .glb) dans le [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4), en modélisant de manière logique et justifiée les composants, interfaces et flux.
- J’ai fait évoluer le modèle initial de Calypso vers Disco entre [PR #36 - AI API Pipeline (Calypso)](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) et [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79), ce qui montre une conception théorique révisée pour satisfaire les contraintes d’un problème pluridisciplinaire et de son contexte.

# Implémenter une approche théorique modélisée

- J’ai implémenté les briques techniques du pipeline (client SSH, serveur Flask, scripts SLURM sur A100) dans [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79), en appliquant de bonnes pratiques de développement et les outils adéquats (Git, API, orchestration GPU).
- J’ai livré une première version fonctionnelle puis lancé un refactoring à partir des limites observées en conditions réelles dans [PR #36 - AI API Pipeline (Calypso)](https://github.com/Toys-R-Us-Rex/Duckify/pull/36), ce qui démontre une mise en application concrète du cycle de développement (prototypage, debug, amélioration) jusqu’à la livraison.

# Évaluer un système informatique

- J’ai évalué plusieurs solutions IA avec des tests ciblés et des critères explicites (qualité, stabilité, coût, effort) dans le [Rapport AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx), en commentant les résultats de manière critique.
- J’ai mené une évaluation ciblée de FreeU avec un protocole reproductible dans le [Rapport comparatif FreeU / sans FreeU](https://typst.app/project/rSFXN1Spr2ZphkfMR5s9yk), ce qui produit une base objective et pertinente pour comparer les performances.
- J’ai ajusté la décision finale en intégrant les retours du CTO et de l’équipe dans [Weekly-meeting - 06.03.2026.pdf](./data/Weekly-meeting%20-%2006.03.2026.pdf), ce qui montre une évaluation itérative, mesurée et utile au pilotage du système.

## Data Engineering

# Valoriser des ensembles de données hétérogènes et multimodales

- J’ai exploité conjointement prompts textuels, sorties visuelles et métadonnées d’inférence dans le [Rapport AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx), ce qui montre la préparation et l’analyse de données hétérogènes issues de modalités différentes.
- J'ai nettoyé et préparé des données multimodales (images, paramètres d'inférence, logs) en les normalisant vers une représentation commune dans le [Rapport comparatif FreeU / sans FreeU](https://typst.app/project/rSFXN1Spr2ZphkfMR5s9yk).
- J'ai structuré les comparaisons de rendus, ce qui permet de commenter la qualité et la valeur des données produites, puis d'en tirer des recommandations opérationnelles.

# Orchestrer un processus et une infrastructure de traitement de données

- J’ai orchestré un flux complet de traitement (préparation locale, soumission distante, exécution cluster, monitoring, récupération d’artefacts) dans [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79), ce qui correspond à un pipeline de bout en bout.
- J'ai sélectionné et ajusté des méthodes d'exécution adaptées au contexte infra en migrant de Calypso vers Disco dans [PR #36 - AI API Pipeline](https://github.com/Toys-R-Us-Rex/Duckify/pull/36), afin de garantir une solution générative exécutable de manière continue.
- J'ai produit un framework informatique pour le pipeline GenAI intégrant soumission, monitoring et récupération, ce qui fournit une solution système reconfigurable et générale dans [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79).

# Appliquer les compétences de l’ingénierie en informatique au domaine des données

- J'ai appliqué au pipeline IA des standards d'ingénierie (versionnement, review, refactoring, documentation) visibles dans [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79), en construisant une boucle perception (acquisition de prompts/modèles) → traitement (inférence GPU) → décision (analyse des rendus) pour le projet robotique GenAI.
- J’ai transformé des essais exploratoires en décisions techniques formalisées dans le [Rapport AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx), ce qui montre la capacité à convertir des données multimodales en indicateurs exploitables pour la décision.

## Compétences professionnelles

# Communiquer clairement et efficacement

- J’ai assuré un rôle de scribe sur les réunions de coordination dans [Coordination GenAI.pdf](./data/Coordination%20GenAI.pdf), en partageant des sujets variés (technique, contraintes, planification) de façon claire et orientée action.
- J’ai documenté les daily meetings dans [Daily Meetings_05.03.2026.pdf](./data/Daily%20Meetings_05.03.2026.pdf), en choisissant un support écrit adapté pour garantir la continuité du suivi.
- J’ai communiqué les avancées techniques au CTO dans [Weekly-meeting - 06.03.2026.pdf](./data/Weekly-meeting%20-%2006.03.2026.pdf), en adaptant le niveau de langage et la synthèse à une audience décisionnelle.

# Adopter une posture professionnelle facilitante face aux situations rencontrées

- J’ai tenu compte des contraintes de l’environnement de travail en remontant rapidement les blocages (dépendances, accès, infrastructure) et en proposant des actions correctives dans [Daily Meetings_05.03.2026.pdf](./data/Daily%20Meetings_05.03.2026.pdf).
- En tant que chef de semaine, j’ai participé de manière proactive aux réalisations techniques et maintenu la dynamique collective (réaffectation, priorisation, suivi) comme documenté dans [Daily Meetings_18.03.2026.pdf](./data/Daily%20Meetings_18.03.2026.pdf).

# Argumenter ses opinions et ses choix lors de processus décisionnels et stratégiques

- J’ai défendu le choix de la solution finale avec des justifications théoriques et des résultats quantitatifs/qualitatifs comparés dans le [Rapport AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx).
- J’ai argumenté l’usage de FreeU dans des contextes ciblés via le [Rapport comparatif FreeU / sans FreeU](https://typst.app/project/rSFXN1Spr2ZphkfMR5s9yk), en reliant explicitement les recommandations aux écarts mesurés.
- J’ai soutenu le pivot Calypso vers Disco à partir d’éléments d’infrastructure et de performance dans le [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4) et [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79), puis débattu ce choix de manière argumentée avec l’équipe.
- J’ai défendu le choix de MV-Adapter Text2Texture face à MV-Adapter Image2Texture avec le [Rapport de comparaison T2T vs I2T](https://typst.app/project/rErsptzNiYXKS3zsnXxLcr), puis je l’ai présenté à l’équipe dans [Présentation CTO Week](https://toys-r-us-rex.github.io/Duckify/presentations/20260313_duckify_meeting_week_4.pdf).

# Critiquer le déroulement d’une production de manière auto-réflexive

- J’ai pris du recul sur ma production dans [Weekly-meeting - 06.03.2026.pdf](./data/Weekly-meeting%20-%2006.03.2026.pdf), en explicitant mes chemins de réflexion, mes décisions, ainsi que leurs limites.
- J’ai jugé a posteriori la justesse des choix réalisés et ajusté la trajectoire en faisant évoluer l’implémentation de [PR #36 - AI API Pipeline](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) vers [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79), ce qui correspond à une auto-critique argumentée avec alternatives motivées.
