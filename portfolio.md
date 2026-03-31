# Compétences


## Analyser un problème informatique complexe

- J'ai analysé les besoins fonctionnels et contraintes techniques du pipeline GenAI (usage, scalabilité, latence, performance GPU) -> [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4)
- J'ai comparé plusieurs solutions GenAI avec une matrice de critères (qualité, coût, intégration, maturité) -> [llm-design-research.pdf](./data/llm-design-research.pdf)
- J'ai isolé l'impact de FreeU via un protocole contrôlé -> [Rapport comparatif FreeU / sans FreeU](https://typst.app/project/rSFXN1Spr2ZphkfMR5s9yk)

## Concevoir une solution théorique modélisée

- J'ai conçu une architecture complète (client local, API, orchestration SLURM, retour d'artefacts) -> [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4)
- J'ai révisé la conception après contraintes réelles d'infrastructure (pivot Calypso vers Disco) -> [PR #36 - AI API Pipeline (Calypso)](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) + [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79)

## Implémenter une approche théorique modélisée

- J'ai implémenté les briques techniques du pipeline (client SSH, API Flask, scripts SLURM) -> [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79)
- J'ai refactorisé l'implémentation suite aux limites observées en production -> [PR #36 - AI API Pipeline (Calypso)](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) + [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79)
- J'ai intégré et refactorisé dans MV-Adapter le benchmark qualité multi-générations (OpenCLIP, NIMA, ranking, rendu des vues 3D, gestion des outputs) -> [PR #6 - MV-Adapter](https://github.com/Toys-R-Us-Rex/MV-Adapter/pull/6) + [scripts/texture_t2tex.py](https://github.com/Toys-R-Us-Rex/MV-Adapter/pull/6/changes#diff-8994820c4d4c244c49e9b52e480a5d27ecf510cd740cd1e9dad6f117c363a0ad) + [nima_rw.py](https://github.com/Toys-R-Us-Rex/MV-Adapter/pull/6/changes#diff-4f76cbef2170089efc671543898d634587c3e6822ec46948ed7f1ccc1527d38f) + [openclip_rw.py](https://github.com/Toys-R-Us-Rex/MV-Adapter/pull/6/changes#diff-291fbd183ad32b68f731518780f8c3d8a3e8845c7656cca6a3c467435864f736) + [rank_rw.py](https://github.com/Toys-R-Us-Rex/MV-Adapter/pull/6/changes#diff-73ba3ab24f38d603d0d5d890c9d2ff3cb6561ad69059931c5ed6b75422726f35) + [render_rw.py](https://github.com/Toys-R-Us-Rex/MV-Adapter/pull/6/changes#diff-1ea4d6c331e35b56345f85ba79cb1df13950524da3110a29719de710edb915c0)
- J'ai implémenté la propagation de bout en bout des paramètres benchmark (activation + nombre de générations) du client jusqu'au cluster -> [PR #115 - Duckify](https://github.com/Toys-R-Us-Rex/Duckify/pull/115) + [client.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-552a6ef43687b83cb97f69cdf1d41e984f4689e1c310ea408f9bad863d23013b) + [data.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-3ddcbbc6513c417d517f1be4b684eb63cfc9376d30257a48875b152a8439841e) + [server.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-d6f9f28dc0fea2755b10b7e414339ffe6f3ac10019dfaee05365437707764223) + [models.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-bcf4242c3782fa390494f45dc3d2eeffdbf34e33c8fd32c7395e7584524d605f) + [run.slurm](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-198334a4f8958fc28604947fd7cd5b21bba8d0b6e4426d0c67056a2e2cee95ff)

## Évaluer un système informatique

- J'ai évalué plusieurs solutions IA avec des critères formalisés et des comparatifs critiques -> [Rapport AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx)
- J'ai évalué de façon ciblée l'effet de FreeU avec métriques quantitatives -> [Rapport comparatif FreeU / sans FreeU](https://typst.app/project/rSFXN1Spr2ZphkfMR5s9yk)
- J'ai intégré une évaluation automatisée multi-générations (OpenCLIP + NIMA + ranking) pour comparer les sorties de manière systématique -> [PR #6 - MV-Adapter](https://github.com/Toys-R-Us-Rex/MV-Adapter/pull/6) + [PR #115 - Duckify](https://github.com/Toys-R-Us-Rex/Duckify/pull/115)
- J'ai ajusté les décisions techniques selon les résultats observés et les retours du CTO/équipe -> [Weekly-meeting - 06.03.2026.pdf](./data/Weekly-meeting%20-%2006.03.2026.pdf)

## Valoriser des ensembles de données hétérogènes et multimodales

- J'ai structuré des résultats multimodaux (prompts, rendus, métriques) pour produire des comparatifs exploitables -> [Rapport AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx)
- J'ai transformé les sorties d'expérimentation en recommandations techniques actionnables -> [Rapport comparatif FreeU / sans FreeU](https://typst.app/project/rSFXN1Spr2ZphkfMR5s9yk)

## Orchestrer un processus et une infrastructure de traitement de données

- J'ai orchestré un flux complet local -> soumission distante -> exécution cluster SLURM -> récupération d'artefacts -> [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79)
- J'ai adapté l'infrastructure d'exécution selon les contraintes de scalabilité/performance -> [PR #36 - AI API Pipeline](https://github.com/Toys-R-Us-Rex/Duckify/pull/36)
- J'ai orchestré un mode benchmark paramétrable (activation + nombre de générations) de la saisie client à l'exécution cluster -> [PR #115 - Duckify](https://github.com/Toys-R-Us-Rex/Duckify/pull/115) + [client.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-552a6ef43687b83cb97f69cdf1d41e984f4689e1c310ea408f9bad863d23013b) + [data.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-3ddcbbc6513c417d517f1be4b684eb63cfc9376d30257a48875b152a8439841e) + [server.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-d6f9f28dc0fea2755b10b7e414339ffe6f3ac10019dfaee05365437707764223) + [models.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-bcf4242c3782fa390494f45dc3d2eeffdbf34e33c8fd32c7395e7584524d605f) + [run.slurm](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-198334a4f8958fc28604947fd7cd5b21bba8d0b6e4426d0c67056a2e2cee95ff)

## Appliquer les compétences de l'ingénierie en informatique au domaine des données

- J'ai appliqué des pratiques d'ingénierie logicielle (Git, review, refactoring, traçabilité) au pipeline GenAI -> [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79)
- J'ai transformé des expérimentations en décisions techniques documentées -> [Rapport AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx)

## Communiquer clairement et efficacement

- J'ai produit des documents techniques structurés pour communiquer analyses, protocoles et recommandations -> [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4)
- J'ai restitué les résultats et choix techniques au CTO/équipe en format présentation -> [Présentation CTO Week](https://toys-r-us-rex.github.io/Duckify/presentations/20260313_duckify_meeting_week_4.pdf)
- J'ai amélioré la qualité de mes comptes-rendus de scribing entre mes deux premiers daily ([05.03.2026](https://toys-r-us-rex.github.io/Duckify/meetings/daily/2026-03-05.pdf), [13.03.2026](https://toys-r-us-rex.github.io/Duckify/meetings/daily/2026-03-13.pdf)) et mes deux derniers ([18.03.2026](https://toys-r-us-rex.github.io/Duckify/meetings/daily/2026-03-18.pdf), [31.03.2026](https://toys-r-us-rex.github.io/Duckify/meetings/daily/2026-03-31.pdf)), avec une rédaction plus structurée des bloquants, des solutions et de la redistribution des tâches.

## Adopter une posture professionnelle facilitante face aux situations rencontrées

- J'ai identifié et traité des blocages critiques (dépendances, accès nœuds, configuration SLURM) avec actions correctives -> [Daily Meetings_05.03.2026.pdf](./data/Daily%20Meetings_05.03.2026.pdf)
- En semaine de chef, j'ai maintenu la dynamique collective (priorisation, arbitrage, suivi des jalons) -> [Daily Meetings_18.03.2026.pdf](./data/Daily%20Meetings_18.03.2026.pdf)
- J'ai collaboré avec un collègue GenAI pour intégrer ses scripts d'évaluation dans la pipeline, en m'appuyant sur son transfert de connaissance pour fiabiliser l'intégration -> [PR #6 - MV-Adapter](https://github.com/Toys-R-Us-Rex/MV-Adapter/pull/6) + [PR #115 - Duckify](https://github.com/Toys-R-Us-Rex/Duckify/pull/115)

## Argumenter ses opinions et ses choix lors de processus décisionnels et stratégiques

- J'ai argumenté le choix de la solution IA finale sur base théorique et expérimentale -> [Rapport AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx)
- J'ai argumenté l'usage conditionnel de FreeU selon les écarts mesurés -> [Rapport comparatif FreeU / sans FreeU](https://typst.app/project/rSFXN1Spr2ZphkfMR5s9yk)
- J'ai soutenu le pivot Calypso vers Disco avec arguments d'infrastructure et de performance -> [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4) + [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79)
- J'ai défendu le choix Text2Texture vs Image2Texture avec analyse des trade-offs -> [Rapport de comparaison T2T vs I2T](https://typst.app/project/rErsptzNiYXKS3zsnXxLcr)

## Critiquer le déroulement d'une production de manière auto-réflexive

- J'ai formulé une auto-critique de ma trajectoire technique et décisionnelle avec axes d'amélioration -> [Weekly-meeting - 06.03.2026.pdf](./data/Weekly-meeting%20-%2006.03.2026.pdf)
- J'ai converti cette auto-critique en action concrète via refactoring du pipeline -> [PR #36 - AI API Pipeline (Calypso)](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) + [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79)

