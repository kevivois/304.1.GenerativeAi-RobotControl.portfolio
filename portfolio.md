# Portfolio Compétences Kevin Voisin : Duckify


## Analyser un problème informatique complexe

- J'ai analysé les besoins fonctionnels et contraintes techniques du pipeline GenAI (usage, scalabilité, latence, performance GPU) -> [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4)
- J'ai analysé et comparé plusieurs solutions GenAI , et conclu à un choix final  -> [GenAi - Analyse & Recherche de solutions](https://typst.app/project/r73B9i9BnakW76rGmJycGx)
- J'ai isolé l'impact de FreeU via un protocole contrôlé -> [Rapport comparatif FreeU / sans FreeU](https://typst.app/project/rSFXN1Spr2ZphkfMR5s9yk)

## Concevoir une solution théorique modélisée

- J'ai conçu une architecture complète (client local, API, orchestration SLURM, retour d'artefacts) -> [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4) + [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79)

## Implémenter une approche théorique modélisée

- J'ai intégré la pipeline GenAI dans l'architecture globale Duckify avec une chaîne complète client -> API serveur -> modèle -> SLURM -> [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79)
- J'ai implémenté le client qui transmet les paramètres de génération, l'API serveur qui orchestre les requêtes, la couche modèle qui prépare l'exécution, et le job cluster qui lance MV-Adapter -> [client.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/79/changes#diff-552a6ef43687b83cb97f69cdf1d41e984f4689e1c310ea408f9bad863d23013b) + [server.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/79/changes#diff-d6f9f28dc0fea2755b10b7e414339ffe6f3ac10019dfaee05365437707764223) + [models.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/79/changes#diff-bcf4242c3782fa390494f45dc3d2eeffdbf34e33c8fd32c7395e7584524d605f) + [run.slurm](https://github.com/Toys-R-Us-Rex/Duckify/pull/79/changes#diff-198334a4f8958fc28604947fd7cd5b21bba8d0b6e4426d0c67056a2e2cee95ff)
- J'ai intégré et refactorisé dans MV-Adapter le benchmark qualité multi-générations (OpenCLIP, NIMA, ranking, rendu des vues 3D, gestion des outputs) -> [PR #6 - MV-Adapter](https://github.com/Toys-R-Us-Rex/MV-Adapter/pull/6) + [scripts/texture_t2tex.py](https://github.com/Toys-R-Us-Rex/MV-Adapter/pull/6/changes#diff-8994820c4d4c244c49e9b52e480a5d27ecf510cd740cd1e9dad6f117c363a0ad) + [nima_rw.py](https://github.com/Toys-R-Us-Rex/MV-Adapter/pull/6/changes#diff-4f76cbef2170089efc671543898d634587c3e6822ec46948ed7f1ccc1527d38f) + [openclip_rw.py](https://github.com/Toys-R-Us-Rex/MV-Adapter/pull/6/changes#diff-291fbd183ad32b68f731518780f8c3d8a3e8845c7656cca6a3c467435864f736) + [rank_rw.py](https://github.com/Toys-R-Us-Rex/MV-Adapter/pull/6/changes#diff-73ba3ab24f38d603d0d5d890c9d2ff3cb6561ad69059931c5ed6b75422726f35) + [render_rw.py](https://github.com/Toys-R-Us-Rex/MV-Adapter/pull/6/changes#diff-1ea4d6c331e35b56345f85ba79cb1df13950524da3110a29719de710edb915c0)
- J'ai implémenté la propagation de bout en bout des paramètres benchmark (activation + nombre de générations) du client jusqu'au cluster -> [PR #115 - Duckify](https://github.com/Toys-R-Us-Rex/Duckify/pull/115) + [client.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-552a6ef43687b83cb97f69cdf1d41e984f4689e1c310ea408f9bad863d23013b) + [data.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-3ddcbbc6513c417d517f1be4b684eb63cfc9376d30257a48875b152a8439841e) + [server.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-d6f9f28dc0fea2755b10b7e414339ffe6f3ac10019dfaee05365437707764223) + [models.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-bcf4242c3782fa390494f45dc3d2eeffdbf34e33c8fd32c7395e7584524d605f) + [run.slurm](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-198334a4f8958fc28604947fd7cd5b21bba8d0b6e4426d0c67056a2e2cee95ff)

## Évaluer un système informatique

- J'ai évalué plusieurs solutions IA avec des critères formalisés et des comparatifs critiques -> [Rapport AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx)
- J'ai évalué de façon ciblée l'effet de FreeU avec métriques quantitatives -> [Rapport comparatif FreeU / sans FreeU](https://typst.app/project/rSFXN1Spr2ZphkfMR5s9yk)
- J'ai évalué plusieurs configurations d'hyperparamètres Text2Texture (guidance scale, steps) sur 80 générations pour mesurer leur impact sur la qualité perçue -> [Optimisation des Hyperparamètres pour la Génération de Textures 3D](https://typst.app/project/rIZH0bul1eBFVShFEzuLWc)
- J'ai intégré une évaluation automatisée multi-générations (OpenCLIP + NIMA + ranking) pour comparer les sorties de manière systématique -> [PR #6 - MV-Adapter](https://github.com/Toys-R-Us-Rex/MV-Adapter/pull/6) + [PR #115 - Duckify](https://github.com/Toys-R-Us-Rex/Duckify/pull/115)

## Valoriser des ensembles de données hétérogènes et multimodales


- J'ai transformé les sorties d'expérimentation en recommandations techniques actionnables -> [Rapport comparatif FreeU / sans FreeU](https://typst.app/project/rSFXN1Spr2ZphkfMR5s9yk)
- J'ai conduit une recherche structurée des meilleurs hyperparamètres Text2Texture (guidance scale, steps) sur 80 générations, en croisant prompts, contraintes visuelles et scoring qualitatif pour extraire une configuration recommandée -> [Optimisation des Hyperparamètres pour la Génération de Textures 3D](https://typst.app/project/rIZH0bul1eBFVShFEzuLWc)

## Orchestrer un processus et une infrastructure de traitement de données

- J'ai orchestré un flux complet local -> soumission distante -> exécution cluster SLURM -> récupération d'artefacts -> [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79) + [client.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/79/changes#diff-552a6ef43687b83cb97f69cdf1d41e984f4689e1c310ea408f9bad863d23013b) + [server.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/79/changes#diff-d6f9f28dc0fea2755b10b7e414339ffe6f3ac10019dfaee05365437707764223) + [models.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/79/changes#diff-bcf4242c3782fa390494f45dc3d2eeffdbf34e33c8fd32c7395e7584524d605f) + [run.slurm](https://github.com/Toys-R-Us-Rex/Duckify/pull/79/changes#diff-198334a4f8958fc28604947fd7cd5b21bba8d0b6e4426d0c67056a2e2cee95ff)
- J'ai orchestré un mode benchmark paramétrable (activation + nombre de générations) de la saisie client à l'exécution cluster -> [PR #115 - Duckify](https://github.com/Toys-R-Us-Rex/Duckify/pull/115) + [client.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-552a6ef43687b83cb97f69cdf1d41e984f4689e1c310ea408f9bad863d23013b) + [data.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-3ddcbbc6513c417d517f1be4b684eb63cfc9376d30257a48875b152a8439841e) + [server.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-d6f9f28dc0fea2755b10b7e414339ffe6f3ac10019dfaee05365437707764223) + [models.py](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-bcf4242c3782fa390494f45dc3d2eeffdbf34e33c8fd32c7395e7584524d605f) + [run.slurm](https://github.com/Toys-R-Us-Rex/Duckify/pull/115/changes#diff-198334a4f8958fc28604947fd7cd5b21bba8d0b6e4426d0c67056a2e2cee95ff)

## Appliquer les compétences de l'ingénierie en informatique au domaine des données

- J'ai appliqué des pratiques d'ingénierie logicielle (Git, review, refactoring, traçabilité) au pipeline GenAI -> [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79)
- J'ai transformé des expérimentations en décisions techniques documentées -> [Rapport AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx)

## Communiquer clairement et efficacement

- J'ai produit des documents techniques structurés pour communiquer analyses, protocoles et recommandations -> [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4)
- Durant chaque présentation hébdomadaire avec le CTO & PO , j'ai pu présenter mes avancées, choix et blocages à mes collègues [Présentation semaine 4 - Slides 3-4 , 14 à 21 ](https://toys-r-us-rex.github.io/Duckify/presentations/20260313_duckify_meeting_week_4.pdf) + [Présentation semaine 5 - Slides 3 , 8 ](https://toys-r-us-rex.github.io/Duckify/presentations/20260320_duckify_meeting_week_5.pdf) + [Présentation semaine 6 , Slides 3, 9 à 12](https://toys-r-us-rex.github.io/Duckify/presentations/20260327_duckify_meeting_week_6.pdf)
- J'ai amélioré la qualité de mes comptes-rendus de scribing entre mes deux premiers daily ([05.03.2026](https://toys-r-us-rex.github.io/Duckify/meetings/daily/2026-03-05.pdf), [13.03.2026](https://toys-r-us-rex.github.io/Duckify/meetings/daily/2026-03-13.pdf)) et mes deux derniers ([18.03.2026](https://toys-r-us-rex.github.io/Duckify/meetings/daily/2026-03-18.pdf), [31.03.2026](https://toys-r-us-rex.github.io/Duckify/meetings/daily/2026-03-31.pdf)), avec une rédaction plus structurée des bloquants, des solutions et de la redistribution des tâches.

## Adopter une posture professionnelle facilitante face aux situations rencontrées

- Désigné chef de semaine, j'ai pris le lead opérationnel en réaffectant les tâches pour garantir une charge de travail équilibrée et m'assurer que chaque membre dispose d'objectifs clairs -> [Weekly meeting 13.03.2026](https://toys-r-us-rex.github.io/Duckify/meetings/weekly/2026-03-13.pdf) + [Daily meeting 18.03.2026](https://toys-r-us-rex.github.io/Duckify/meetings/daily/2026-03-18.pdf) + [Daily meeting 20.03.2026](https://toys-r-us-rex.github.io/Duckify/meetings/daily/2026-03-20.pdf)
JJ’ai pris le lead lors de la présentation au CTO de la semaine 5 et piloté la définition du milestone de la semaine suivante, validé collectivement avec l’équipe -> [Présentation ceo week 5](https://toys-r-us-rex.github.io/Duckify/presentations/20260320_duckify_meeting_week_5.pdf)
- J'ai collaboré avec un collègue GenAI pour intégrer ses scripts d'évaluation dans la pipeline, en m'appuyant sur son transfert de connaissance pour fiabiliser l'intégration -> [PR #6 - MV-Adapter](https://github.com/Toys-R-Us-Rex/MV-Adapter/pull/6) + [PR #115 - Duckify](https://github.com/Toys-R-Us-Rex/Duckify/pull/115)

## Argumenter ses opinions et ses choix lors de processus décisionnels et stratégiques

- J'ai argumenté le choix de la solution IA finale sur base théorique et expérimentale -> [Rapport AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx)
- J'ai argumenté l'usage conditionnel de FreeU selon les écarts mesurés -> [Rapport comparatif FreeU / sans FreeU](https://typst.app/project/rSFXN1Spr2ZphkfMR5s9yk)
- J'ai argumenté le choix des hyperparamètres Text2Texture retenus (guidance/steps) à partir d'une comparaison structurée des performances -> [Optimisation des Hyperparamètres pour la Génération de Textures 3D](https://typst.app/project/rIZH0bul1eBFVShFEzuLWc)
- J'ai soutenu le pivot Calypso vers Disco avec arguments d'infrastructure et de performance -> [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4) + [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79)
- J'ai défendu le choix Text2Texture vs Image2Texture avec analyse des trade-offs -> [Rapport de comparaison T2T vs I2T](https://typst.app/project/rErsptzNiYXKS3zsnXxLcr)

## Critiquer le déroulement d'une production de manière auto-réflexive

- J'ai exercé une auto-critique régulière de l'avancement du projet lors des présentations hebdomadaires au CTO/PO, en identifiant les écarts entre objectifs et résultats -> [Présentation CEO week 2 - Slide 6](https://toys-r-us-rex.github.io/Duckify/presentations/20260227_duckify_meeting_week_2.pdf) + [Présentation CEO week 3 - Slide 10](https://toys-r-us-rex.github.io/Duckify/presentations/20260306_duckify_meeting_week_3.pdf)

- J'ai explicité les causes du non-achèvement complet des milestones de la semaine 4 et formulé des ajustements pour la suite -> [Présentation week 4 - Slide 4](https://toys-r-us-rex.github.io/Duckify/presentations/20260313_duckify_meeting_week_4.pdf) + [Présentation week 5 - Slide 3](https://toys-r-us-rex.github.io/Duckify/presentations/20260320_duckify_meeting_week_5.pdf)
