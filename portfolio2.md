# Portfolio 2 - Synthèse par compétences (Duckify)

# Analyser un problème informatique complexe
- J'ai mené une revue littérature approfondie sur l'état de l'art en génération IA de textures 3D. Le rapport [llm-design-research.pdf](./data/llm-design-research.pdf) démontre la rigueur de ma recherche en présentant solutions industrielles et scientifiques.
- Analyse des contraintes d'infrastructure HPC : accès SSH avec authentification clés, orchestration SLURM, conflits de dépendances Python (CUDA/PyTorch versions). Formalisation dans rapport Typst et documentation PR #79.
- J'ai structuré une matrice d'analyse des expérimentations (prompts, paramètres, résultats) pour objectiver les décisions techniques.
- Artefacts liés : [Rapport GenAI Pipeline - Problématiques analysées](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4) (détail complet des 3 problématiques clés), [Document AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx), [Excel de Tracking - Tests Text2Texture](https://docs.google.com/spreadsheets/d/1NpckWJFnlC7U_zsNBi_d-7OBQRsPJaKOQ3xO2CpFwcs/edit?usp=sharing), [Pull Request #79](https://github.com/Toys-R-Us-Rex/Duckify/pull/79).

# Concevoir une solution théorique modélisée
- J'ai conçu et modélisé deux architectures complètes de pipeline IA : d'abord sur Calypso (PR #36), puis repensé la solution pour Disco avec contraintes SSH d'infrastructure renforcées.
- Architecture Disco : PC local (client) → SSH authentifié → API Flask sur serveur → SLURM job → exécution GPU A100 → retour fichier .glb texturé. Modélisation complète des flux de données, points critiques de sécurité (clés SSH, authentification), orchestration des jobs SLURM et gestion des résultats.
- Artefacts liés : [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4) (détail des problématiques et choix de conception), [Pull Request #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79#issue-2765828916) (implémentation complète), [PR #36 - AI API Pipeline (Calypso)](https://github.com/Toys-R-Us-Rex/Duckify/pull/36), [Notes de réunion LLM-DESIGN](./data/Coordination%20GenAI.pdf).

# Implémenter une approche théorique modélisée
- Implémentation PR #36 (Calypso) : API backend, client, orchestration Docker initiale.
- **Implémentation PR #79 (Disco - complet et production-ready)** : 
  - Client Python SSH : authentification de clés, envoi paramètres (objet 3D + prompt) vers serveur distant.
  - Serveur Flask sur Disco : réception POST requêtes, validation paramètres, coordination avec SLURM.
  - Script SLURM : exécution MV-Adapter dans environnement Python dédié (uv), gestion GPU A100, retour fichier .glb texturé.
  - Environnement Python isolé (uv) pour éviter conflits de dépendances (CUDA/PyTorch).
- Déploiement complet bout-en-bout : du notebook local jusqu'à récupération artefact final.
- Artefacts liés : [Pull Request #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79) (21 fichiers, 2223 additions - commits détaillés visibles dans la PR), [Documentation AI Solution (+ MV-Adapter)](https://typst.app/project/r73B9i9BnakW76rGmJycGx), [PR #36 - AI API Pipeline (Calypso)](https://github.com/Toys-R-Us-Rex/Duckify/pull/36).

# Evaluer un système informatique
- J’ai benchmarké plusieurs solutions IA en conditions réelles, avec un protocole documenté pour comparer faisabilité, qualité et coût d’exécution.
- Évaluation comparative Calypso vs Disco : impact de la puissance GPU (A100 vs infrastructure locale), fiabilité et reproductibilité environnement. Cette évaluation factuelle a justifié le pivot vers Disco mieux adapté aux ressources HPC disponibles.
- Artefacts liés : [Rapport GenAI Pipeline](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4) (section Problématique justifiant Disco), [Document AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx), [Rapport de Réunion CTO/Équipe - PDF](./data/Weekly-meeting%20-%2006.03.2026.pdf).

# Valoriser des ensembles de données hétérogènes et multimodales
- J’ai manipulé des entrées textuelles (prompts), visuelles (textures/images de sortie) et des métadonnées expérimentales (seeds, paramètres, notes d’évaluation).
- J’ai consolidé ces données dans un support commun pour faciliter l’analyse croisée et la décision d’équipe.
- Artefacts liés : [Excel de Tracking - Tests Text2Texture](https://docs.google.com/spreadsheets/d/1NpckWJFnlC7U_zsNBi_d-7OBQRsPJaKOQ3xO2CpFwcs/edit?usp=sharing), [Documentation AI Solution (+ MV-Adapter)](https://typst.app/project/r73B9i9BnakW76rGmJycGx).

# Orchestrer un processus et une infrastructure de traitement de données
- Orchestre bout-en-bout complet (PR #36 Calypso, puis PR #79 Disco) : notebook local → client SSH → API Flask → SLURM scheduler → GPU A100 → fichier résultat.
- Industrialisation via SLURM (script `run.slurm`) : allocation GPU, gestion mémoire (80GB), timeouts, logs structurés. Gestion environnement Python isolé (uv) pour reproductibilité.
- Coordination client/serveur fiabilisée : retry logic, gestion erreurs SSH, validation paramètres, suivi job états.
- Artefacts liés : [Pull Request #79 - GenAI Pipeline Integration](https://github.com/Toys-R-Us-Rex/Duckify/pull/79#issue-2765828916) (commits SLURM et serveur visibles), [Rapport Architecture GenAI](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4) (section choix de conception), [Documentation AI Solution (+ MV-Adapter)](https://typst.app/project/r73B9i9BnakW76rGmJycGx), [PR #36 - AI API Pipeline](https://github.com/Toys-R-Us-Rex/Duckify/pull/36).

# Appliquer les compétences de l’ingénierie en informatique au domaine des données
- J'ai appliqué des pratiques d'ingénierie logicielle rigoureuses (backlog JIRA, versioning Git, PR reviews, documentation) à un problème complexe de génération de données visuelles par IA.
- Conversion des essais exploratoires en protocole d'expérimentation traçable, reproductible et exploitable. Gestion environnements isolés avec uv pour fiabilité pipeline.
- Architecture client/serveur modularisée (PR #79) : séparation claire responsabilités, communication structurée, gestion erreurs robuste.
- Artefacts liés : [Pull Request #79 - GenAI Pipeline Integration](https://github.com/Toys-R-Us-Rex/Duckify/pull/79) (31 commits, architecture modulaire visible), [Pull Request #36 - AI API Pipeline](https://github.com/Toys-R-Us-Rex/Duckify/pull/36), [Rapport GenAI Pipeline](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4) (choix conception documentés), [Daily Meeting Notes W1 & W2](https://typst.app/project/roWPq3UVmcXvuuZUvlFFKM).

# Communiquer clairement et efficacement
- J’ai assuré un rôle de scribe à plusieurs réunions clés pour garantir la circulation d’information et l’alignement technique.
- J’ai présenté l’état d’avancement et les arbitrages techniques au PO, au CTO et à l’équipe.
- Artefacts liés : [Notes de réunion LLM-DESIGN](./data/Coordination%20GenAI.pdf), [Notes de Daily Meeting (Scribe du 05.03) - PDF](./data/Daily%20Meetings_05.03.2026.pdf), [Slides de Présentation W3](https://hessoit-my.sharepoint.com/:p:/r/personal/nathan_antoniet_hes-so_ch/Documents/presentation-week-3.pptx?d=wd7dc986a100d49fb85e629c7f265e3d0&csf=1&web=1&e=6lrqrL).

# Adopter une posture professionnelle facilitante face aux situations rencontrées
- J’ai partagé rapidement les blocages techniques, proposé des alternatives et documenté les solutions pour l’équipe.
- J’ai maintenu une posture proactive orientée résolution, notamment sur les problèmes de dépendances et d’infrastructure.
- Artefacts liés : [Notes de Daily Meeting (Scribe du 05.03) - PDF](./data/Daily%20Meetings_05.03.2026.pdf), [Excel de Tracking - Tests Text2Texture](https://docs.google.com/spreadsheets/d/1NpckWJFnlC7U_zsNBi_d-7OBQRsPJaKOQ3xO2CpFwcs/edit?usp=sharing).

# Argumenter ses opinions et ses choix lors de processus décisionnels et stratégiques
- J'ai argumenté les choix technologiques à partir de preuves expérimentales : tests de performance, contraintes matérielles réelles, analyse reproductibilité environnement.
- Justification du pivot Calypso → Disco : infrastructure insuffisante sur Calypso, limitation fiabilité, besoin ressources GPU (A100) pour production. Décision documentée dans rapport Typst et rapports CTO.
- Évaluation architecture : choix client/serveur SSH (vs alternatives contenerisation pure) basé sur contraintes infrastructure HES, sécurité réseau, et reproductibilité des environnements Python isolés.
- Artefacts liés : [Rapport GenAI Pipeline - Justification Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4) (section Problématique et Choix de conception), [Pull Request #79 - Architecture finalisée](https://github.com/Toys-R-Us-Rex/Duckify/pull/79), [Présentation PO/CTO - Slides 9-14 & 26](./data/Duckify%20Meeting%20Week%201.pptx), [Rapport de Réunion CTO/Équipe - PDF](./data/Weekly-meeting%20-%2006.03.2026.pdf).

# Critiquer le déroulement d’une production de manière auto-réflexive
- J’ai identifié les points forts (montée en compétence SLURM, structuration des tests) et les points de friction (dependency hell, coût de refactoring).
- J’ai défini un plan d’amélioration concret : refactoring de pipeline, décision finale de méthode IA, optimisation continue du prompt engineering.
- Artefacts liés : [Rapport de Réunion CTO/Équipe - PDF](./data/Weekly-meeting%20-%2006.03.2026.pdf), [Document AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx), [Pull Request #36 - AI API Pipeline](https://github.com/Toys-R-Us-Rex/Duckify/pull/36).
