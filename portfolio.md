# Portfolio - Kevin Voisin

# Analyser un problème informatique complexe
- J’ai décomposé le problème GenAI en sous-problèmes explicites : qualité visuelle, faisabilité infra (GPU/SSH/SLURM), stabilité des dépendances.
- J’ai comparé des solutions existantes (TEXTure, Paint-it, Text2Tex, SDFusion) et explicité les opportunités/limites de chacune avant décision.
- J’ai formalisé les contraintes d’exécution réelles (authentification SSH, ressources A100, conflits CUDA/PyTorch) pour orienter les choix techniques.
- Artefacts liés (où regarder) :
  - [llm-design-research.pdf](./data/llm-design-research.pdf) : sections « Solutions fonctionnelles », « Solutions en cours d’investigation », « Solutions écartées ».
  - [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4) : section « Problématique » (3 contraintes clés explicitement listées).
  - [Pull Request #79](https://github.com/Toys-R-Us-Rex/Duckify/pull/79) : historique de commits montrant la résolution progressive des contraintes d’infrastructure.

# Concevoir une solution théorique modélisée
- J’ai conçu deux modèles d’architecture successifs (Calypso puis Disco) et justifié le pivot par les contraintes observées.
- Le modèle cible est explicité de bout en bout : client local → SSH → API Flask distante → job SLURM → génération GPU A100 → retour artefact `.glb`.
- J’ai modélisé les points de contrôle critiques (authentification, orchestration des jobs, récupération des résultats).
- Artefacts liés (où regarder) :
  - [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4) : schéma et justification de l’architecture Disco.
  - [PR #36 - AI API Pipeline (Calypso)](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) : première version de l’architecture client/API.
  - [Pull Request #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79) : matérialisation du modèle final (client, serveur, SLURM).

# Implémenter une approche théorique modélisée
- J’ai implémenté la première version (PR #36) puis la version complète Disco (PR #79) en suivant un cycle de développement itératif avec revue.
- Implémentation technique livrée :
  - Client Python SSH (envoi des paramètres d’inférence et déclenchement distant).
  - Serveur Flask (réception/validation de requêtes et orchestration d’exécution).
  - Script SLURM (allocation GPU, logs, exécution du modèle, récupération des sorties).
  - Environnement isolé `uv` pour la reproductibilité.
- Résultat : pipeline exécutable bout-en-bout depuis le notebook vers un artefact `.glb` généré.
- Artefacts liés (où regarder) :
  - [Pull Request #79 - GenAI Pipeline Integration Disco](https://github.com/Toys-R-Us-Rex/Duckify/pull/79) : commits `client.py`, `server.py`, `run.slurm`, README d’exécution.
  - [PR #36 - AI API Pipeline (Calypso)](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) : base d’implémentation initiale (API + client).


# Evaluer un système informatique
- J’ai évalué plusieurs approches avec des critères explicites : faisabilité technique, qualité de sortie, robustesse d’exécution et coût opérationnel.
- J’ai utilisé les retours d’équipe/CTO pour critiquer les résultats (lisibilité des outputs, non-déterminisme, explicitation des limites).
- Artefacts liés (où regarder) :
  - [Weekly-meeting - 06.03.2026.pdf](./data/Weekly-meeting%20-%2006.03.2026.pdf) : critiques mesurées, axes d'amélioration et justification du choix Disco.

# Valoriser des ensembles de données hétérogènes et multimodales
- J’ai travaillé sur des données de natures différentes : texte (prompts), visuel (textures/rendus), paramètres d’inférence et métadonnées d’exécution.
- Artefacts liés (où regarder) :
  - [llm-design-research.pdf](./data/llm-design-research.pdf) : analyse qualitative et comparaison des solutions IA testées.

# Orchestrer un processus et une infrastructure de traitement de données
- J’ai orchestré une chaîne complète de traitement/génération : soumission locale, exécution distante, supervision de job, récupération du résultat.
- J’ai industrialisé l’exécution via SLURM (allocation ressources, logs, timeouts) avec un environnement isolé pour réduire les échecs liés aux dépendances.
- Artefacts liés (où regarder) :
  - [Pull Request #79 - GenAI Pipeline Integration](https://github.com/Toys-R-Us-Rex/Duckify/pull/79) : fichiers d’orchestration `run.slurm`, `server.py`, `client.py`.
  - [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4) : description du pipeline cible et de ses contraintes d’infrastructure.
  - [PR #36 - AI API Pipeline](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) : première orchestration, utile pour montrer l’évolution.

# Appliquer les compétences de l’ingénierie en informatique au domaine des données
- J’ai appliqué des pratiques d’ingénierie logicielle au traitement de données IA : versionnement, revues, documentation, itérations courtes.
- J’ai transformé des essais exploratoires en processus reproductible (paramétrage, exécution contrôlée, traces de résultats).
- Artefacts liés (où regarder) :
  - [Pull Request #79 - GenAI Pipeline Integration](https://github.com/Toys-R-Us-Rex/Duckify/pull/79) : historique de refactorings, corrections review, modularisation.
  - [Pull Request #36 - AI API Pipeline](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) : base technique initiale et amélioration progressive.
  - [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4) : décisions d’ingénierie documentées.

# Communiquer clairement et efficacement
- J’ai assuré le rôle de scribe sur des réunions de coordination et de suivi pour diffuser une information exploitable par l’équipe.
- J'ai été scribe de daily meetings (05.03.2026 et 18.03.2026) et de réunion de coordination (Coordination GenAI).
- J’ai communiqué l’avancement, les blocages et les décisions techniques auprès d’audiences différentes (équipe, CTO, coordination).
- Artefacts liés (où regarder) :
  - [Coordination GenAI.pdf](./data/Coordination%20GenAI.pdf) : directives, répartition des tâches, décisions partagées.
  - [Daily Meetings_05.03.2026.pdf](./data/Daily%20Meetings_05.03.2026.pdf) : statut opérationnel, blocages, plan d’action du jour.
  - [Daily Meetings_18.03.2026.pdf](./data/Daily%20Meetings_18.03.2026.pdf) : rôle de scribe, coordination d'équipe.
  - [Weekly-meeting - 06.03.2026.pdf](./data/Weekly-meeting%20-%2006.03.2026.pdf) : retours d’audience et attentes de communication.

# Adopter une posture professionnelle facilitante face aux situations rencontrées
- J’ai remonté rapidement les blocages (accès Disco, dépendances, retours de review) et proposé des actions correctives concrètes.
- J’ai maintenu une contribution proactive orientée résolution et coordination avec le reste de l’équipe.
- En tant que chef de semaine, j’ai présidé l’ensemble des daily meetings, réaffecté des membres sans tâche claire et identifié les blocages potentiels pour maintenir l’avancement collectif.
- Artefacts liés (où regarder) :
  - [Daily Meetings_05.03.2026.pdf](./data/Daily%20Meetings_05.03.2026.pdf) : blocages identifiés et actions proposées.
  - [Daily Meetings_18.03.2026.pdf](./data/Daily%20Meetings_18.03.2026.pdf) : rôle de chef de semaine, réaffectations, coordination.
  

# Argumenter ses opinions et ses choix lors de processus décisionnels et stratégiques
- J’ai soutenu les décisions techniques avec des éléments vérifiables (contraintes infra, résultats de tests, faisabilité opérationnelle). 
- Artefacts liés (où regarder) :
  - [Rapport GenAI Pipeline - Réflexion & Architecture](https://typst.app/project/r88Ho8oDHaBiIYa7MDoBL4) : sections « Problématique » et « Choix de conception ».
  - [Weekly-meeting - 06.03.2026.pdf](./data/Weekly-meeting%20-%2006.03.2026.pdf) : décisions, critiques, justification des orientations.
  - [Pull Request #79 - Architecture finalisée](https://github.com/Toys-R-Us-Rex/Duckify/pull/79) : traduction concrète des choix dans le code.

# Critiquer le déroulement d’une production de manière auto-réflexive
- J’ai pris du recul sur la production : points forts (progression SLURM, structuration du pipeline) et limites (dépendances, effort de refactoring).
- J’ai proposé des améliorations concrètes et actionnables pour la suite (clarification des critères de choix, consolidation des scripts, qualité des résultats).
- Artefacts liés (où regarder) :
  - [Weekly-meeting - 06.03.2026.pdf](./data/Weekly-meeting%20-%2006.03.2026.pdf) : critiques formulées et attentes explicites.
  - [Pull Request #36 - AI API Pipeline](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) : base de comparaison pour justifier les pivots architecturaux.
