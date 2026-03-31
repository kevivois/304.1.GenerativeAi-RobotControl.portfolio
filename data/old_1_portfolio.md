# Portfolio - Kevin Voisin

# Ingénierie informatique

## Analyser un problème informatique complexe

- J'ai conduit une analyse formelle de la problématique GenAI d'automatisation d'un système de génération de textures, documentée dans le [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4), en décomposant les besoins fonctionnels (facilité d'usage, automatisation, scalabilité), en identifiant les contraintes techniques (infrastructure disponible, performance GPU, latence), et en modélisant explicitement leurs dépendances et points de tension pour guider les choix architecturaux.

- J'ai conduit une évaluation comparative structurée de plusieurs solutions GenAI (TEXTure, Paint-it, Text2Tex, SDFusion, MV-Adapter) dans [llm-design-research.pdf](./data/llm-design-research.pdf), en établissant une matrice de critères explicites (qualité de sortie, coût computationnel, complexité d'intégration, maturité), et en documentant les compromis techniques associés à chaque approche pour identifier les opportunités d'implémentation.
- J'ai mené une évaluation isolée de l'impact de FreeU avec un protocole d'expérimentation rigoureux dans le [Rapport comparatif FreeU / sans FreeU](https://typst.app/project/rSFXN1Spr2ZphkfMR5s9yk), en maintenant constant tous les autres paramètres (modèle, prompts, conditions GPU) pour extraire l'effet net de cette technique et produire une base probante pour les recommandations d'usage.

## Concevoir une solution théorique modélisée

- J'ai conçu une architecture de pipeline complète (client local, tunnel SSH/API Flask, orchestration SLURM sur Disco, retour d'artefacts .glb) dans le [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4), en modélisant de manière logique et justifiée chaque composant (services, points d'intégration), les interfaces de communication, et les flux de données pour assurer la cohérence end-to-end du système.
- J'ai fait évoluer l'architecture initiale de Calypso vers Disco entre [PR #36 - AI API Pipeline (Calypso)](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) et [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79), en adaptant le modèle théorique aux contraintes réelles d'infrastructure et de performance, ce qui montre une révision itérative de la conception pour satisfaire les exigences pluridisciplinaires du projet et de son contexte opérationnel.

## Implémenter une approche théorique modélisée

- J'ai implémenté les briques techniques critiques du pipeline (client SSH avec gestion de session, serveur API Flask avec endpoints structurés, scripts SLURM pour orchestration GPU sur A100) dans [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79), en appliquant des standards d'ingénierie (versioning Git, reviews sur les requêtes, logging structuré) et en intégrant des outils d'orchestration adaptés (API REST, gestion des ressources GPU, monitoring).
- J'ai livré une première version fonctionnelle puis orchestré un refactoring systématique à partir des limitations observées en conditions réelles (latence, stabilité, scalabilité) dans [PR #36 - AI API Pipeline (Calypso)](https://github.com/Toys-R-Us-Rex/Duckify/pull/36), ce qui démontre une application concrète du cycle de développement itératif (prototypage rapide, identification des goulots, refactoring ciblé, validation) jusqu'à la livraison d'une version améliorée.

## Évaluer un système informatique

- J'ai évalué plusieurs solutions IA candidate avec des tests rigoureusement ciblés et une batterie de critères formalisés (qualité visuelle des rendus, stabilité d'exécution, coût computationnel, effort d'intégration) dans le [Rapport AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx), en produisant des analyses comparatives critiques et en hiérarchisant les trade-offs pour éclairer les décisions d'architecture.
- J'ai complété cette évaluation globale par une analyse ciblée de FreeU, avec protocole reproductible et métriques quantitatives, dans le [Rapport comparatif FreeU / sans FreeU](https://typst.app/project/rSFXN1Spr2ZphkfMR5s9yk), afin d'isoler ses bénéfices nets et de délimiter clairement les contextes d'usage recommandés.
- J'ai ajusté les décisions finales en intégrant itérativement les retours du CTO et de l'équipe technique dans [Weekly-meeting - 06.03.2026.pdf](./data/Weekly-meeting%20-%2006.03.2026.pdf), ce qui montre une démarche d'évaluation cyclique, mesurée et alignée avec les besoins opérationnels du projet.

# Data Engineering

## Valoriser des ensembles de données hétérogènes et multimodales


## Orchestrer un processus et une infrastructure de traitement de données

- J'ai orchestré un flux complet de traitement de bout en bout (préparation locale des données, soumission distante des jobs, exécution distribuée sur cluster SLURM, récupération structurée d'artefacts) dans [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79), en garantissant traçabilité, reproductibilité et gestion robuste des erreurs à chaque étape.
- J'ai sélectionné itérativement et ajusté les méthodes d'exécution en fonction du contexte infra disponible, migrant l'architecture de Calypso vers Disco dans [PR #36 - AI API Pipeline](https://github.com/Toys-R-Us-Rex/Duckify/pull/36), afin de garantir une solution générative fiable, scalable et exécutable de manière continue dans l'environnement de production.

## Appliquer les compétences de l’ingénierie en informatique au domaine des données
<!--   J'ai appliqué au pipeline IA des standards rigoureux d'ingénierie logicielle (versionnement Git, code review structurée, refactoring itératif, documentation en ligne) visibles dans [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79), en construisant une boucle fermée perception → traitement → décision (acquisition de prompts et modèles candidats, inférence GPU distribuée, analyse comparative des rendus) pour le projet robotique GenAI, ce qui garantit qualité, traçabilité et maintenabilité.
- J'ai transformé des essais exploratoires et itérations préliminaires en décisions techniques formalisées et documentées dans le [Rapport AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx), ce qui montre la capacité à convertir des données brutes multimodales en indicateurs exploitables et hiérarchisés pour éclairer des décisions stratégiques du projet.
-->


# Compétences professionnelles

## Communiquer clairement et efficacement
<!--
- J'ai assuré un rôle structurant de scribe sur les réunions de coordination multidisciplinaires dans [Coordination GenAI.pdf](./data/Coordination%20GenAI.pdf), en synthétisant et en partageant de manière claire et orientée action des discussions variées (enjeux techniques, contraintes d'infrastructure, planification de sprints), ce qui a facilité l'alignement et la traçabilité des décisions.
- J'ai documenté systématiquement les daily meetings dans [Daily Meetings_05.03.2026.pdf](./data/Daily%20Meetings_05.03.2026.pdf), en sélectionnant un format écrit structuré (problèmes identifiés, actions, propriétaires, délais) pour garantir la continuité du suivi et la propagation des apprentissages.
- J'ai communiqué les avancées techniques et les choix architecturaux au CTO dans [Weekly-meeting - 06.03.2026.pdf](./data/Weekly-meeting%20-%2006.03.2026.pdf), en adaptant le niveau de langage, la profondeur technique et la synthèse au profil et aux besoins d'une audience décisionnelle.

-->


## Adopter une posture professionnelle facilitante face aux situations rencontrées

- J'ai tenu compte des contraintes réelles de l'environnement de travail (ressources GPU limitées, accès réseau restreint, infrastructure volatile) en identifiant rapidement les blocages critiques (dépendances non satisfaites, accès aux nœuds de calcul, configuration SLURM) et en proposant des actions correctives pragmatiques et documentées dans [Daily Meetings_05.03.2026.pdf](./data/Daily%20Meetings_05.03.2026.pdf), ce qui a débloqué des situations de risque.
- En tant que chef de semaine, j'ai participé de manière proactive et structurée aux réalisations techniques (review de code, debugging d'infrastructure, optimisations GPU) et j'ai maintenu la dynamique collective par la gestion active de priorités (réaffectation de tâches, arbitrage sur les choix techniques, suivi des jalons) comme documenté dans [Daily Meetings_18.03.2026.pdf](./data/Daily%20Meetings_18.03.2026.pdf), ce qui a assuré la continuité du projet sous pression.

## Argumenter ses opinions et ses choix lors de processus décisionnels et stratégiques

- J'ai défendu rigoureusement le choix de la solution IA finale en fournissant des justifications théoriques approfondies (état de l'art, approches comparées) et des résultats quantitatifs/qualitatifs systématiquement comparés (qualité, coût, stabilité) dans le [Rapport AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx), ce qui a créé un consensus autour de la décision.
- J'ai argumenté l'usage ciblé et conditionnel de FreeU avec le [Rapport comparatif FreeU / sans FreeU](https://typst.app/project/rSFXN1Spr2ZphkfMR5s9yk), en reliant explicitement chaque recommandation aux écarts mesurés (gestion mémoire, qualité, latence) et en délimitant les contextes d'application recommandés vs déconseillés.
- J'ai soutenu et justifié le pivot architectural de Calypso vers Disco à partir d'éléments formels d'infrastructure (ressources GPU disponibles, orchestration SLURM) et de performance (latence, throughput) présentés dans le [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4) et [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79), puis débattu ce choix de manière argumentée et constructive avec l'équipe technique.
- J'ai défendu le choix stratégique de MV-Adapter Text2Texture plutôt qu'Image2Texture en comparant rigoureusement les trade-offs (qualité, latence, dépendances) avec le [Rapport de comparaison T2T vs I2T](https://typst.app/project/rErsptzNiYXKS3zsnXxLcr), et j'ai présenté cette analyse et ses implications à l'équipe dans [Présentation CTO Week](https://toys-r-us-rex.github.io/Duckify/presentations/20260313_duckify_meeting_week_4.pdf).

## Critiquer le déroulement d’une production de manière auto-réflexive

- J'ai pris du recul analytique sur ma production technique et décisionnelle dans [Weekly-meeting - 06.03.2026.pdf](./data/Weekly-meeting%20-%2006.03.2026.pdf), en explicitant mes processus de réflexion, les hypothèses sous-jacentes à mes décisions, ainsi que les limites observées et les améliorations possibles, ce qui montre une posture critique et constructive.
- Cette auto-critique a débouché sur une action concrète: le refactoring progressif de [PR #36 - AI API Pipeline (Calypso)](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) vers [PR #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79), fondé sur des preuves empiriques (limitations observées en production, leçons apprises) et des alternatives explicitement motivées.
