# Portfolio de Compétences - Projet Duckify
**Période :** Février/Mars 2026 (Semaines 1 à 3)

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
  - [Pull Request #36 - AI API Pipeline](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) : model.py (Docker), app.py (API locale), client.py (Connexion PC).
  - [Document AI Testing & Documentation](https://typst.app/project/r73B9i9BnakW76rGmJycGx)
  - [Daily Meeting Notes W1 & W2 (Lien TYPST : Naviguez dans le dossier typst afin de trouver toutes les notes)](https://typst.app/project/roWPq3UVmcXvuuZUvlFFKM)

### Semaine 3 : Déploiement MV-Adapter, SLURM & Pivot Architectural
- **Déploiement & Maîtrise SLURM :** Installation réussie de la solution MV-Adapter sur le cluster Disco. Résolution d'un problème complexe  de dépendances (environnement Conda, versions CUDA/C++) et maîtrise acquise du gestionnaire SLURM pour l'exécution des jobs GPU.
- **Documentation & Tracking rigoureux :** Documentation détaillée des méthodes Text2Texture et Image2Texture. Création d'un outil de suivi centralisé (Excel) pour le Prompt Engineering, répertoriant chaque test, ses paramètres, résultats et conclusions.
- **Pivot Architectural :** Décision stratégique d'abandonner l'inférence sur le serveur Calypso au profit exclusif du cluster Disco, suite aux limitations matérielles identifiées. Planification du refactoring de la Pull Request de l'API pour s'adapter à cette nouvelle infrastructure.
- **Communication & Restitution :** Prise du rôle de scribe pour le Daily du 05.03.2026. Présentation complète des avancées et de la solution MV-Adapter au CTO et à l'équipe le vendredi, avec intégration active des feedbacks. Alignement total avec les retours des scribes sur les réunions de la semaine.
- **Livrables W3 :**
  - [Documentation AI Solution (+ MV-Adapter)](https://typst.app/project/r73B9i9BnakW76rGmJycGx)
  - [Excel de Tracking - Tests Text2Texture](https://docs.google.com/spreadsheets/d/1NpckWJFnlC7U_zsNBi_d-7OBQRsPJaKOQ3xO2CpFwcs/edit?usp=sharing)
  - [Notes de Daily Meeting (Scribe du 05.03) - PDF](./data/Daily%20Meetings_05.03.2026.pdf)
  - [Rapport de Réunion CTO/Équipe - PDF](./data/Weekly-meeting%20-%2006.03.2026.pdf)
  - [Slides de Présentation W3 (Slides 3, 5, 6, 10) - PPTX](https://hessoit-my.sharepoint.com/:p:/r/personal/nathan_antoniet_hes-so_ch/Documents/presentation-week-3.pptx?d=wd7dc986a100d49fb85e629c7f265e3d0&csf=1&web=1&e=6lrqrL)

---

## 2. Matrice des Compétences Validées

| Compétence ciblée | Actions menées (W1 à W3) | Preuves |
| :--- | :--- | :--- |
| **Analyser un problème complexe** | - W2 : Analyse des problèmes de reproductibilité des environnements IA.<br>- W3 : Mise en place d'une matrice de tracking systématique (Excel) pour analyser finement l'impact du Prompt Engineering sur MV-Adapter. | [Testing W2/W3](https://typst.app/project/r73B9i9BnakW76rGmJycGx)<br>[Excel Tracking W3](https://docs.google.com/spreadsheets/d/1NpckWJFnlC7U_zsNBi_d-7OBQRsPJaKOQ3xO2CpFwcs/edit?usp=sharing) |
| **Concevoir une solution architecturale** | - W2 : Développement d'une pipeline robuste via API et SSH.<br>- W3 : Capacité à pivoter techniquement (abandon de Calypso pour Disco) pour garantir la scalabilité du système, impliquant un refactoring prévu. | [PR #36 - Architecture](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) |
| **Maîtriser les outils techniques** | - W2 : Intégration avancée de Docker et gestion des tunnels SSH.<br>- W3 : Maîtrise validée du calcul distribué via SLURM sur le cluster Disco et résolution de conflits complexes de compilation (C++/CUDA). |  [PR #36](https://github.com/Toys-R-Us-Rex/Duckify/pull/36) |
| **Communiquer clairement** | - W1/W3 : Rôle de scribe assumé à plusieurs reprises pour aligner l'équipe technique.<br>- W3 : Présentation des avancées et réception proactive des feedbacks du CTO. | [Notes W1](./data/Coordination%20GenAI.pdf) & [W3](./data/Weekly-meeting%20-%2006.03.2026.pdf)<br>[Slides de présentation W3](https://hessoit-my.sharepoint.com/:p:/r/personal/nathan_antoniet_hes-so_ch/Documents/presentation-week-3.pptx?d=wd7dc986a100d49fb85e629c7f265e3d0&csf=1&web=1&e=6lrqrL) |
| **Argumenter ses choix** | - W1 : Justification des choix technologiques face au CTO.<br>- W3 : Argumentation du pivot d'infrastructure (Calypso vs Disco) basée sur des preuves empiriques et des tests de charge. | [Slides W1](./data/Duckify%20Meeting%20Week%201.pptx)<br>[Slides W3](https://hessoit-my.sharepoint.com/:p:/r/personal/nathan_antoniet_hes-so_ch/Documents/presentation-week-3.pptx?d=wd7dc986a100d49fb85e629c7f265e3d0&csf=1&web=1&e=6lrqrL) |
| **Posture pro facilitante** | - Proactivité dans le partage des points de blocage et structuration d'outils collaboratifs (Excel partagé) pour que toute l'équipe puisse suivre les itérations IA. | [Excel Tracking W3](https://docs.google.com/spreadsheets/d/1NpckWJFnlC7U_zsNBi_d-7OBQRsPJaKOQ3xO2CpFwcs/edit?usp=sharing) |

---

## 3. Auto-réflexion & Amélioration Continue

### 3.1 Ce qui fonctionne bien (Les succès)
- **Maîtrise de la nouvelle infrastructure :** La courbe d'apprentissage sur SLURM a été franchie avec succès en W3. L'installation de MV-Adapter sur Disco prouve ma capacité à dompter des environnements serveurs complexes.
- **Rigueur scientifique dans les tests :** La création du fichier Excel de tracking permet enfin de sortir de l'empirisme. Chaque modification de paramètre ou de prompt est documentée, justifiée et analysée, ce qui accélère grandement la prise de décision.
- **Agilité architecturale :** Avoir le pragmatisme de stopper l'intégration sur Calypso pour refactoriser la pipeline vers Disco démontre une bonne capacité d'adaptation face aux réalités matérielles.

### 3.2 Ce qui a posé problème (Les défis)
- **Le "Dependency Hell" sur Disco :** La mise en place de MV-Adapter a été très chronophage à cause des conflits de librairies (compilation C++, versions PyTorch, incompatibilités de tenseurs).
- **Le coût du refactoring :** Le changement de serveur (Calypso → Disco) rend obsolète une partie du travail de la PR #36 de la Semaine 2, imposant une charge de travail imprévue pour adapter le code.
- **La reunion avec le CTO du vendredi 06.03.2026** : Le CTO nous pousse à faire une décision sur quel méthode AI utiliser avant la fin de semaine 4, cette décision aura beaucoup d'impact sur la suite du projet et donc se doit d'etre investie pleinement durant la semaine 4

### 3.3 Plan d'action & Ajustements pour la suite
1. **Refactoring de la Pipeline :** Mettre à jour en priorité le code de la PR pour que l'API et le client communiquent de manière fluide et sécurisée avec le cluster Disco.
2. **Choix final de l'algorithme :** Utiliser les données du fichier Excel de tracking et de mon collègue (M.Caporizzi) pour trancher définitivement, lors de la W4, entre la méthode *Text2Texture* et *Image2Texture* de MV-Adapter.
3. **Optimisation des résultats :** Poursuivre le prompt engineering strict pour éradiquer les dernières hallucinations visuelles (visages dupliqués, etc.) sur les meshes.

---

## 4. Hiring Process Q&A (Préparation aux entretiens)

**Q1. Quelle a été ta principale contribution technique jusqu'à présent ?**
*Réponse :* J’ai conçu et implémenté une pipeline complète pour automatiser la génération de textures IA. J'ai orchestré le flux sécurisé depuis un PC local vers une API, en gérant dynamiquement la migration de notre infrastructure d'un serveur limité (Calypso) vers un cluster de calcul haute performance (Disco) via SLURM & La mise en place de la solution MV-Adapter fonctionnelle & executable sur Disco avec SLURM.

**Q2. Comment as-tu géré la complexité des tests IA pour éviter de tourner en rond ?**
*Réponse :* Devant la multitude de paramètres et de prompts possibles avec MV-Adapter, j'ai mis en place un outil de tracking centralisé (Google Sheets). Chaque itération y est répertoriée avec ses inputs (prompt, seed, paramètres), ses outputs visuels, et une conclusion claire. Cela a transformé des tests hasardeux en un véritable protocole scientifique, facilitant le choix de la méthode finale.

**Q3. As-tu déjà eu à jeter du code ou revoir ton architecture en cours de route ? Comment as-tu réagi ?**
*Réponse :* Absolument, lors de la Semaine 3. J'avais codé une API fonctionnelle pour le serveur Calypso en Semaine 2. Cependant, face aux limites matérielles (RAM) de Calypso identifiées lors de mes tests de charge, j'ai pris la décision d'abandonner cette voie. J'ai assumé de devoir refactoriser ma Pull Request pour adapter la pipeline au cluster Disco. Il vaut mieux refactoriser tôt que de maintenir une architecture techniquement condamnée.

**Q4. Quel obstacle majeur as-tu rencontré cette semaine, et comment l’as-tu géré ?**
*Réponse :* L'installation de MV-Adapter sur le cluster a été un véritable "Dependency Hell" (conflits CUDA, erreurs de Linker C++). J'ai géré cela de manière chirurgicale : forçage des variables d'environnement des compilateurs Conda et création de liens symboliques pour guider le cluster, le tout automatisé dans un script SLURM pour garantir la reproductibilité.