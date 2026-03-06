# Portfolio de Compétences - Semaine 2 (W2)
**Projet :** Duckify
**Date :** 27 Février 2026 

---

## 1. Rapport Hebdomadaire 

### Actions clés & Résultats
- **Exploration & Validation de solutions IA :** Teste exhaustif de 8 solutions AI différentes pour la génération de textures, documentations des approches et évaluation de la reproductibilité de chaque solution.
- **Développement de la pipeline d'intégration :** Conception et implémentation d'une architecture complète appelant une API via le serveur SSH Calypso avec Docker pour exécuter la solution de génération de texture.
- **Intégration technique :** Mise en place du flux de travail : PC local → API SSH (Calypso) → Docker → exécution de la solution IA → résultats.
- **Communication & Planification :** Réunion d'intégration mercredi avec l'équipe pour valider la structure de la pipeline et les points techniques de coordination.
- **Participation quotidienne :** Présence aux daily meetings (sauf mardi) avec documentation et communication claire des avancées et blocages.
- **Apprentissage infrastructure :** Prise en main des clusters Chacha et Disco à partir de mercredi/jeudi, initiation à l'utilisation de SLURM.

### Artifacts (Preuves)
- **Documentation des solutions testées :** [Document AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx)
- **Daily Meeting Notes :** [Réunions quotidiennes W2](https://typst.app/project/roWPq3UVmcXvuuZUvlFFKM) (participation sauf mardi)
- **Pipeline d'intégration :** [Pull Request #36 - AI API Pipeline](https://github.com/Toys-R-Us-Rex/Duckify/pull/36)
- **Réunion d'intégration mercredi :** Documentation interne via la PR (commentaires et discussions)
- **Workflow & Architecture :** [Diagramme du workflow CI/CD visible dans la PR](https://github.com/Toys-R-Us-Rex/Duckify/pull/36)

---

## 2. Justification des Compétences 

| Compétence ciblée | Action & Justification | Preuve |
| :--- | :--- | :--- |
| **Analyser un problème complexe**  | Exploration systématique de 8 solutions IA distinctes, évaluation de leurs avantages/contraintes et identification des problèmes de reproductibilité liés à l'environnement. | [Document AI Testing & Documentation](https://typst.app/project/rVAS0WHLmFP2e3ResWqTdV) |
| **Concevoir une solution architecturale**  | Conception et développement d'une pipeline complète (PC local → API SSH → Docker → traitement IA) permettant l'exécution fiable de la génération de textures sur Calypso. | [Pull Request #36](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) |
| **Communiquer clairement**  | Présentation structurée des solutions testées aux coéquipiers, participation quotidienne aux meetings avec documentation des blocages et avancées. | [Daily Meeting Notes](https://typst.app/project/roWPq3UVmcXvuuZUvlFFKM) |
| **Posture pro facilitante**  | Réunion mercredi pour valider la structure d'intégration, collaboration active sur la planification et mise en place de la pipeline avec l'équipe. | [Pull Request #36 - discussions](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) + Daily notes |
| **Maîtriser les outils techniques**  | Mise en place d'une architecture SSH + Docker, gestion de l'API, premiers pas sur les clusters Chacha/Disco et initiation à SLURM. | [Pull Request #36](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) + documentation clusters |

---

## 3. Auto-réflexion

### 3.1 Ce qui a fonctionné
- **Développement efficace de la pipeline :** L'architecture PC local → API SSH → Docker a été mise en place plus rapidement que prévu, malgré la complexité de l'infrastructure.
- **Approche systématique :** Tester 8 solutions IA et les documenter a permis une meilleure compréhension des options disponibles et de leurs contraintes.
- **Communication au sein de l'équipe :** Les réunions convergeront vers une vision claire de l'intégration et des prochaines étapes.
- **Proactivité sur l'infrastructure :** Avoir demandé accès à Chacha/Disco dès mercredi permet de démarrer les expériences gourmandes en ressources.

### 3.2 Ce qui n'a pas fonctionné
- **Reproductibilité des solutions testées :** La plupart des 8 solutions IA testées présentaient des difficultés importantes à reproduire en raison de l'environnement (dépendances obsolètes, conflits de packages, configurations spécifiques).
- **Maîtrise rapide de SLURM :** Malgré la prise en main de Chacha et Disco à partir de mercredi/jeudi, la compréhension du système SLURM reste incomplète et représente une courbe d'apprentissage abrupte.
- **Gestion du temps initial :** La crainte de "perdre du temps" sur le testing des solutions n'a ralenti la progression que modérément, mais aurait pu être mieux structurée.

### 3.3 Ce que je changerai
- **Priorité accrue sur la documentation des bloques :** Documenter plus précisément les erreurs de reproductibilité pour les transmettre aux développeurs/chercheurs concernés.
- **Valider l'intégration plus tôt :** Tester l'API SSH + Docker dès la W1 aurait pu identifier certains problèmes plus précocement.
- **Structurer le testing en sprints :** Plutôt que de tester 8 solutions en vrac, les tester 2-3 par jour avec jalons clairs d'évaluation.

---

## 4. Hiring Process Q&A (3 Questions) 

### Q1. Quelle a été ta principale contribution technique cette semaine ?
**Réponse :** J’ai conçu et implémenté une pipeline complète pour exécuter la génération de textures IA via Calypso, en orchestrant le flux PC local → API SSH → Docker → exécution IA → résultats. Cette contribution a permis de valider une base d’intégration fiable pour l’équipe.

### Q2. Quel obstacle majeur as-tu rencontré, et comment l’as-tu géré ?
**Réponse :** Le principal obstacle a été la reproductibilité des solutions IA testées (dépendances obsolètes, conflits de packages, environnements instables). Je l’ai géré avec une approche méthodique : tests comparatifs de 8 solutions, documentation systématique des résultats et communication régulière des blocages en daily.

### Q3. Quelles sont tes priorités pour la suite du projet ?
**Réponse :** Mes priorités sont de consolider la reproductibilité (standardisation de l’environnement), approfondir l’utilisation de SLURM sur Chacha/Disco pour les charges lourdes et de tester des solutions seulement testable sur Chacha/Disco & les comparer de manière protocolaire et structurée


