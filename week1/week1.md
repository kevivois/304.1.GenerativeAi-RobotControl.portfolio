# Portfolio de Compétences - Semaine 1 (W1)
**Projet :** Duckify
**Date :** 22 Février 2026 

---

## 1. Rapport Hebdomadaire 

### Actions clés & Résultats
- **Cadrage stratégique :** Définition des milestones réalistes pour la W1 suite aux discussions avec les enseignants et l'équipe.
- **Scribe & Coordination :** Prise de notes des directives et des tenants et aboutissants lors de la réunion de coordination du groupe LLM-DESIGN
- **Conception LLM :** Création et gestion du backlog technique sur JIRA pour la partie "LLM-Design".
- **Recherche technique :** Exploration et tests de modèles génératifs pour la création de textures à partir de prompts personnalisés.
- **Communication leadership :** Présentation des recherches et de la solution LLM retenue au Product Owner (PO) et au CTO.

### Artifacts (Preuves)
- **Coordination & Directives :** [Notes de réunion LLM-DESIGN](./data/Coordination%20GenAI.pdf)
- **Planification :** [Presentation Brainstorming (p. 7-8)](./data/Brainstorming-3.pdf)
- **Suivi de projet :** Screenshot JIRA (data/jira-tasks.png)
- **Recherche technique :** [Document llm-research.typ](./data/llm-design-research.pdf)
- **Présentation PO/CTO :** [Friday Meeting Slides (9-14 & 26)](./data/Duckify%20Meeting%20Week%201.pptx)
- **Suivi quotidien :** [Daily Meeting Notes](./data/Daily%20Meetings.pdf)

---

## 2. Justification des Compétences 

| Compétence ciblée | Action & Justification | Preuve |
| :--- | :--- | :--- |
| **Communiquer clairement**  | Rôle de scribe : documentation des directives et enjeux pour assurer l'alignement de l'équipe LLM-DESIGN. | [Notes de réunion LLM-DESIGN](./data/Coordination%20GenAI.pdf) |
| **Analyser un problème complexe**  | Identification des opportunités et contraintes liées à la génération de textures par LLM. | [Document llm-research.typ](./data/llm-design-research.pdf) |
| **Posture pro facilitante**  | Participation proactive aux réalisations techniques et partage transparent des points de blocage. | [Daily Meeting Notes](./data/Daily%20Meetings.pdf) |
| **Argumenter ses choix** | Présentation et justification des choix technologiques face au CTO et au PO. | [Friday Meeting Slides (9-14 & 26)](./data/Duckify%20Meeting%20Week%201.pptx) |

---

## 3. Auto-réflexion

### 3.1 Ce qui a fonctionné
- La répartition des tâches dans mon groupe a permis de travailler efficacement à la recherche de solutions IA.
- Nous avons trouvé une solution IA fonctionnelle (TEXTure) pour générer de la texture à partir d'un modèle et d'un prompt.

### 3.2 Ce qui n'a pas fonctionné
- La solution Text2Tex a été écartée car l'environnement (Conda) vieux de 2 ans présentait des conflits entre `mathutils` et Python 3.9.
- Le serveur Calypso manque de RAM pour faire tourner la méthode *Paint-it*.
- Le modèle *TEXTure* actuel produit encore trop d'hallucinations et d'artefacts visuels sur le modèle du canard.
- 

### 3.3 Ce que je changerai
- Demander plus tôt l'accès aux clusters Disco ou Chacha pour tester les modèles gourmands en RAM.
- Prioriser le prompt engineering pour stabiliser les résultats de TEXTure avant d'explorer de nouveaux frameworks.
- Analyser la date de dernière mise à jour des repos GitHub avant de tenter une installation locale pour éviter les stacks obsolètes.

---

## 4. Hiring Process Q&A (3 Questions) 

**1. "Pourquoi avoir écarté le modèle SDFusion pour la génération de textures ?"**
- Réponse : Car il modifie la géométrie (mesh) du modèle 3D. Pour les besoins d'impression et de contrôle robotique du projet Duckify, le mesh original doit rester intact.

**2. "Comment avez-vous résolu les problèmes de dépendances sur le projet TEXTure ?"**
- Réponse : En intervenant directement dans le code pour fixer les versions des packages Python incompatibles, permettant ainsi d'obtenir nos premiers résultats visuels fonctionnels.

**3. "Quel est l'intérêt d'avoir agi comme scribe lors de la réunion de coordination ?"**
- Réponse : Cela permet de figer les directives et les contraintes techniques immédiatement. Cela garantit que chaque membre de l'équipe LLM-DESIGN part avec une vision identique et claire des "tenants et aboutissants" du projet.
