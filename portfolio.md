# Portfolio de Compétences - Projet Duckify
**Période :** Février 2026 (Semaines 1 & 2)
**Rôle principal :** R&D IA Générative, Ingénierie de Pipeline & Coordination technique

---

## 1. Rapport d'Activité & Évolution du Projet

Ce journal de bord retrace l'évolution de la recherche et de l'implémentation de solutions de génération de textures 3D par IA (LLM-Design) pour le projet Duckify.

### Semaine 1 : Cadrage, Recherche Initiale & Faisabilité
- **Cadrage stratégique & Coordination :** Rôle de scribe lors de la réunion de coordination LLM-DESIGN pour figer les directives. Création et gestion du backlog technique sur JIRA.
- **Recherche technique :** Exploration de modèles génératifs (TEXTure, Text2Tex, Paint-it, SDFusion) pour la création de textures à partir de prompts.
- **Communication leadership :** Présentation des recherches et justification de la solution LLM retenue face au Product Owner (PO) et au CTO.
- **Livrables W1 :** - [Notes de réunion LLM-DESIGN](./data/Coordination%20GenAI.pdf)
  - [Document de recherche LLM](./data/llm-design-research.pdf)
  - [Présentation PO/CTO - Slides 9-14 & 26](./data/Duckify%20Meeting%20Week%201.pptx)

### Semaine 2 : Développement Architectural & Tests Scalables
- **Développement de la pipeline d'intégration :** Conception et implémentation de l'architecture backend complète. Mise en place du flux : *PC local → API SSH (Serveur Calypso) → Docker → Exécution de l'IA → Retour des résultats (ZIP)*.
- **Tests intensifs (Benchmarking) :** Évaluation exhaustive de 8 solutions IA distinctes, avec une documentation rigoureuse sur leur reproductibilité et leurs contraintes d'environnement.
- **Mise à l'échelle (Infrastructure) :** Prise en main des clusters calculatoires haute performance (Chacha et Disco) et initiation au gestionnaire de jobs SLURM pour pallier les limites matérielles du serveur Calypso.
- **Livrables W2 :**
  - [Pull Request #36 - AI API Pipeline & Diagramme CI/CD](https://github.com/Toys-R-Us-Rex/Duckify/pull/36)
  - [Document AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx)
  - [Daily Meeting Notes W1 & W2](https://typst.app/project/roWPq3UVmcXvuuZUvlFFKM)

---

## 2. Matrice des Compétences Validées

| Compétence ciblée | Actions menées (W1 & W2) | Preuves |
| :--- | :--- | :--- |
| **Analyser un problème complexe** | - W1 : Identification des contraintes liées à la génération de textures par LLM.<br>- W2 : Exploration systématique de 8 solutions IA et analyse des problèmes de reproductibilité des environnements. | [Recherche W1](./data/llm-design-research.pdf)<br>[Testing W2](https://typst.app/project/rVAS0WHLmFP2e3ResWqTdV) |
| **Concevoir une solution architecturale** | - W2 : Développement d'une pipeline robuste et sécurisée (SSH, API locale, isolation Docker) pour l'inférence IA sur serveur distant. | [PR #36 - Architecture](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) |
| **Maîtriser les outils techniques** | - W2 : Intégration avancée de Docker, gestion des tunnels SSH, et initiation au calcul distribué via SLURM (Clusters Chacha/Disco). | [PR #36](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) |
| **Communiquer clairement** | - W1 : Rôle de scribe pour aligner l'équipe technique.<br>- W2 : Présentation structurée des tests aux coéquipiers et documentation rigoureuse des blocages en Daily Meetings. | [Notes de réunion](./data/Coordination%20GenAI.pdf)<br>[Daily Notes](https://typst.app/project/roWPq3UVmcXvuuZUvlFFKM) |
| **Argumenter ses choix** | - W1 : Présentation et justification des choix technologiques (SDFusion écarté au profit de TEXTure) face au CTO et au PO. | [Slides W1](./data/Duckify%20Meeting%20Week%201.pptx) |
| **Posture pro facilitante** | - Proactivité dans le partage des points de blocage.<br>- Organisation d'une réunion d'intégration (W2) pour valider la structure technique avec l'équipe. | Daily notes & [PR #36](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) |

---

## 3. Auto-réflexion & Amélioration Continue

### 3.1 Ce qui fonctionne bien (Les succès)
- **Vitesse d'exécution sur l'infrastructure :** L'architecture complexe (API SSH → Docker) a été mise en place plus rapidement que prévu, offrant une base fiable à l'équipe dès la Semaine 2.
- **Approche méthodique de la R&D :** Le passage d'une recherche théorique (W1) à des tests systématiques sur 8 solutions (W2) a permis de cartographier précisément l'état de l'art technique.
- **Proactivité face aux blocages matériels :** L'identification rapide du manque de RAM sur le serveur Calypso m'a poussé à migrer vers les clusters Chacha/Disco via SLURM de manière anticipée.

### 3.2 Ce qui a posé problème (Les défis)
- **L'enfer des dépendances (Reproductibilité) :** La majorité des solutions open-source testées (ex: Text2Tex) souffrent d'environnements obsolètes (Python 3.8/3.9, conflits Conda, dépendances PyTorch/Kaolin cassées).
- **Limites des modèles actuels :** Le modèle TEXTure produit encore des hallucinations et des artefacts visuels indésirables sur le mesh du canard.
- **Courbe d'apprentissage SLURM :** Bien que l'accès aux clusters soit acquis, la maîtrise totale des scripts SLURM pour lancer les environnements Conda et les jobs GPU reste complexe.

### 3.3 Plan d'action & Ajustements pour la suite
1. **Structurer les tests en Sprints :** Au lieu de tester 8 solutions de front, isoler 2 à 3 solutions par jour avec des protocoles stricts de comparaison.
2. **Prioriser la standardisation :** Documenter très précisément les erreurs de reproductibilité pour isoler des environnements Docker/Conda viables sur le long terme.
3. **Optimiser les résultats existants :** Avant de chercher de nouveaux frameworks, faire du *Prompt Engineering* approfondi sur TEXTure pour tenter de réduire les artefacts.
4. **Focus SLURM :** Déployer mes scripts de test de manière protocolaire exclusivement sur Chacha/Disco pour les modèles lourds.

---

## 4. Hiring Process Q&A (Préparation aux entretiens)

**Q1. Quelle a été ta principale contribution technique jusqu'à présent ?**
*Réponse :* J’ai conçu et implémenté une pipeline complète pour automatiser la génération de textures IA. J'ai orchestré le flux sécurisé depuis un PC local vers une API via SSH sur un serveur distant, qui déclenche ensuite un conteneur Docker exécutant le modèle IA, avant de renvoyer le résultat 3D prêt à l'emploi.

**Q2. Pourquoi avoir écarté certaines solutions IA d'apparence performantes comme SDFusion ou Text2Tex ?**
*Réponse :* Chaque rejet était motivé par une contrainte business ou technique stricte. SDFusion a été écarté car il altère la géométrie originale du mesh, ce qui est incompatible avec nos contraintes d'impression 3D et de robotique. Text2Tex a été écarté car son environnement Conda était obsolète, entraînant des conflits insolubles de dépendances, ce qui nuit à la reproductibilité et à la mise en production.

**Q3. Quel est l'intérêt d'avoir pris le rôle de scribe lors du lancement technique ?**
*Réponse :* Dans un projet complexe, cela permet de figer les directives et les contraintes matérielles immédiatement. Cela garantit que chaque membre de l'équipe part avec une vision identique des "tenants et aboutissants", évitant ainsi le travail redondant ou hors-sujet.

**Q4. Quel obstacle majeur as-tu rencontré cette semaine, et comment l’as-tu géré ?**
*Réponse :* Le principal obstacle a été l'instabilité (Dependency Hell) des dépôts open-source testés. J'ai géré cela avec une approche très méthodique : création d'environnements Conda isolés ou de conteneurs Docker, tests comparatifs documentés, et dans certains cas, intervention directe dans le code source pour forcer la rétrocompatibilité des librairies.

**Q5. Comment avez-vous résolu les problèmes de RAM (OOM) lors de vos tests ?**
*Réponse :* J'ai rapidement identifié que le serveur initial (Calypso) était un goulot d'étranglement matériel. J'ai donc été proactif en demandant les accès aux clusters de calcul haute performance (Chacha/Disco) et j'ai commencé à adapter mes pipelines pour qu'elles tournent via le gestionnaire de tâches SLURM.