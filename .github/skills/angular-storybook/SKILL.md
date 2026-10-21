---
name: angular-storybook
description: Storybook est un atelier frontend pour créer des composants et des pages UI en isolation. Ce skill est exclusivement destiné aux projets Angular 22 pour initialiser Storybook, générer ou mettre à jour des fichiers .stories.ts, des composants et des pages UI.
---

1. Métadonnées

Nom : Agent Angular Storybook
Identifiant : angular-storybook
Version : 1.0.0
Statut : DRAFT
Spécialité : Storybook pour Angular 22 : création de composants et de pages UI en isolation, documentation et vérification de leurs différents états.
Domaine technique : Angular 22, Storybook, TypeScript, Component Story Format (CSF), documentation et tests d’interface utilisateur.
Langue principale : Français
Date de création : 2026-10-21
Dernière révision : 2026-10-21

2. Objectif du skill

Ce skill permet à un agent IA de :
Configurer et utiliser Storybook exclusivement dans des projets Angular 22 afin de créer et maintenir, en isolation, des stories représentant les différents états de composants et de pages UI. Il aide également à documenter ces éléments et à préparer leur vérification à partir des stories.

Résultat attendu :
À la fin de son utilisation, le skill doit permettre de produire :
Une configuration Storybook compatible avec le projet Angular 22 ciblé, ainsi que des fichiers `.stories.ts` valides pour les composants ou pages demandés. Les stories doivent couvrir les états pertinents, être consultables dans l'atelier Storybook et être accompagnées des contrôles réalisés.

Problème traité:
Le développement direct dans l'application Angular rend difficile l'exploration isolée des composants, des pages UI, des états peu fréquents et des cas limites sans démarrer l'application complète. L'absence de stories structurées limite également la documentation et la vérification répétable de l'interface.

Valeur ajoutée:
Le skill fournit une méthode spécialisée pour intégrer Storybook à Angular 22, décrire les états rendus avec des stories et exploiter ces stories comme support de documentation et de vérification UI. Il accélère le travail de l'IA tout en conservant la compatibilité avec la configuration et les composants du projet existant.

Le skill doit apporter une procédure, des connaissances, des critères ou des méthodes spécifiques. Il ne doit pas simplement reformuler les instructions générales de l'agent.

3. Périmètre fonctionnel

Inclus:
- Vérifier l’environnement Angular 22 et l’état de l’installation Storybook.
- Initialiser ou ajuster Storybook sans écraser les personnalisations existantes.
- Créer ou mettre à jour des stories TypeScript pour des composants et pages Angular.
- Décrire les inputs, outputs, signals, états visuels, cas limites et dépendances nécessaires.
- Utiliser les mécanismes Storybook adaptés : args, parameters, decorators, autodocs et tests lorsque demandés.
- Vérifier la découverte, le rendu et la compilation des stories.

Exclus:
- Projets non Angular ou versions Angular non confirmées.
- Développement de fonctionnalités métier hors composants/pages nécessaires aux stories.
- Mise à jour ou rétrogradation d’Angular, TypeScript ou Storybook sans demande explicite.
- Publication, déploiement ou configuration Chromatic sans autorisation.

Cas d'utilisation
Le skill peut être utilisé lorsque :
- Storybook doit être initialisé dans un projet Angular 22.
- Les stories d’un composant, d’une page ou d’un groupe de composants doivent être créées ou mises à jour.
- Les variantes, états et cas limites d’une interface doivent être documentés ou vérifiés.

Cas de non-utilisation
Ne pas utiliser ce skill lorsque :
- La demande concerne un autre framework ou une version Angular non confirmée.
- La demande porte uniquement sur le backend, le déploiement ou une fonctionnalité métier sans objectif Storybook.

Si une demande sort du périmètre, ne tente pas de la traiter comme si elle relevait de ce skill. Signale la limite et recommande une capacité adaptée si elle est connue.

4. Contrat d'entrée

Données nécessaires

| Champ | Obligatoire | Description | Exemple ou format |
|---|---|---|---|
| `task` | Oui | Action demandée : initialiser, générer, modifier ou vérifier. | `generate` |
| `context` | Oui | Racine du projet, version Angular, composants et configuration connus. | `Projet Angular 22` |
| `constraints` | Selon le cas | Conventions, dépendances, états à couvrir et limites. | `Ne pas modifier le composant` |
| `scope` | Selon le cas | Fichiers et commandes autorisés. | `*.stories.ts` |
| `artifacts` | Selon le cas | Composants, pages, stories et configuration disponibles. | `src/app/ui/button` |
| `acceptance_criteria` | Selon le cas | Conditions vérifiables de réussite. | `Build Storybook réussi` |
| `permissions` | Oui pour toute action outillée | Fichiers modifiables, commandes autorisées et validations requises. | `édition + npm run storybook` |

Les permissions doivent préciser les fichiers modifiables, les commandes autorisées et les validations nécessaires.

Préconditions
Avant de commencer, vérifier :
- que le projet est bien Angular 22 dans `package.json` et `package-lock.json`
- que les fichiers et composants ciblés existent et sont compilables, sauf demande de création
- que la configuration Storybook existante et les scripts npm ont été examinés
- que l’installation ou la modification de dépendances est autorisée

Distinguer les préconditions indispensables des informations simplement utiles.
Si une donnée indispensable manque, demander sa fourniture ou retourner un état bloqué. Ne pas inventer les informations nécessaires.
Si une donnée facultative manque, poursuivre lorsque cela reste fiable et sans risque disproportionné, en indiquant les hypothèses pertinentes.

5. Connaissances et ressources requises

Connaissances techniques :
- Configuration Angular 22, composants standalone ou NgModules selon le projet.
- TypeScript et Component Story Format (CSF).
- Stories, args, parameters, decorators, autodocs et pages Storybook.
- Tests d’interaction, d’accessibilité et visuels uniquement lorsqu’ils sont configurés et demandés.

Ressources :
- Documentation générale : https://storybook.js.org/docs
- Installation : https://storybook.js.org/docs/get-started/install
- Frameworks, dont Angular : https://storybook.js.org/docs/get-started/frameworks
- Création de stories : https://storybook.js.org/docs/writing-stories
- Tests UI : https://storybook.js.org/docs/writing-tests
- Documentation des composants : https://storybook.js.org/docs/writing-docs
- Configuration : https://storybook.js.org/docs/configure
- Fichiers de référence : `package.json`, `package-lock.json`, `angular.json`, `tsconfig*.json` et `.storybook/`.
- Exemples validés : stories existantes du projet et exemples officiels Storybook.
- Outils compatibles : npm, scripts Storybook du projet et outils de test disponibles.
- Skills complémentaires : aucun skill obligatoire.

Autorité des sources

En cas de contradiction entre les sources, appliquer les règles suivantes :
- Respecter les instructions prioritaires, les politiques de sécurité et les permissions.
- Privilégier les spécifications et documentations officielles applicables.
- Privilégier les informations du projet qui ont été explicitement validées.
- Vérifier la version et la date de pertinence des informations techniques.
- Distinguer les faits documentés des interprétations.
- Signaler les contradictions non résolues.

Ne pas considérer une source comme fiable uniquement parce qu'elle est récente ou présentée avec assurance.

6. Procédure d'exécution

Appliquer la procédure ci-dessous dans l'ordre. Adapter les étapes uniquement lorsque cela est explicitement prévu ou techniquement nécessaire.

Étape 1 — Analyser la demande

Objectif : comprendre précisément le résultat à produire.

Actions :
- Déterminer le mode : `setup`, `generate`, `update` ou `verify`.
- Identifier les composants/pages, états et critères attendus.
- Distinguer les actions autorisées des actions nécessitant une validation.
- Refuser le périmètre non Angular 22 ou demander une clarification.

Résultat intermédiaire :
Objectif, cible, contraintes et critères d’acceptation explicitement identifiés.

Condition de passage :
La tâche et son périmètre sont suffisamment précis pour examiner le projet.

Étape 2 — Examiner le contexte

Objectif : disposer des informations nécessaires à une exécution fiable.

Actions :
- Lire `package.json`, `package-lock.json`, `angular.json` et les `tsconfig` pertinents.
- Vérifier la version Angular, la version Storybook, le builder et les scripts disponibles.
- Chercher `.storybook/`, les fichiers `*.stories.ts` et les configurations existantes.
- Lire les composants ciblés, leurs imports, providers, inputs, outputs et états.
- Déterminer si le projet utilise standalone, NgModules, signals, RxJS ou des mocks.

Résultat intermédiaire :
État réel du projet, dépendances, points d’intégration et informations manquantes.

Condition de passage :
Les versions, la configuration et les fichiers concernés sont connus.

Étape 3 — Définir la stratégie

Objectif : déterminer une méthode proportionnée au problème.

Actions :
- Réutiliser la configuration Storybook existante si elle est valide.
- Si Storybook est absent, proposer ou exécuter l’initialisation officielle autorisée.
- Choisir une story TypeScript/CSF adaptée au composant ou à la page.
- Définir une story de base puis les états utiles : variantes, vide, chargement, erreur, désactivé et cas limite si pertinents.
- Prévoir les `args`, `parameters`, `decorators`, providers et mocks strictement nécessaires.
- Définir les contrôles à exécuter avant de modifier les fichiers.

Résultat intermédiaire :
Plan minimal, compatible avec les versions et conventions constatées.

Condition de passage :
Le plan respecte le périmètre et les permissions.

Étape 4 — Exécuter la procédure spécialisée

Objectif : réaliser la capacité définie par le skill.

Actions :
- Installer ou configurer Storybook uniquement dans le périmètre autorisé.
- Créer ou modifier les fichiers `*.stories.ts` proches des composants concernés.
- Utiliser les types Storybook appropriés et conserver un typage strict.
- Déclarer le composant, son titre, ses args et ses états sans dupliquer sa logique métier.
- Ajouter la documentation ou les tags autodocs lorsque cela répond au besoin.
- Ajouter des tests d’interaction ou d’accessibilité seulement si l’environnement les supporte et si la demande le justifie.
- Préserver les fichiers de configuration et les stories non concernés.

Pour chaque action, préciser si nécessaire :
- Les entrées requises.
- La méthode applicable.
- L'outil à utiliser.
- Le résultat intermédiaire attendu.
- Les conditions d'échec.
- Les contrôles de sécurité.
- Les conditions de poursuite.

Résultat intermédiaire :
Configuration et stories créées ou modifiées, avec une liste précise des fichiers touchés.

Condition de passage :
Les fichiers sont modifiés sans dépasser le périmètre autorisé.

Étape 5 — Vérifier le résultat

Objectif : établir si le résultat répond effectivement au besoin.

Actions :
- Vérifier que les stories sont détectées par Storybook.
- Lancer le script Storybook disponible, par exemple `npm run storybook`, si autorisé.
- Lancer le build Storybook disponible, par exemple `npm run build-storybook`, si configuré.
- Vérifier la compilation TypeScript et les erreurs de rendu.
- Exécuter les tests configurés ; un contrôle non exécuté reste explicitement non exécuté.
- Vérifier les états demandés, les imports, les providers et les args.

Résultat intermédiaire :
Contrôles réussis, échoués ou non exécutés, avec preuve et impact.

Condition de passage :
Les critères d’acceptation sont évalués et les écarts sont documentés.

Étape 6 — Produire le livrable

Objectif : fournir un résultat exploitable par l'agent appelant.

Actions :
- Lister les fichiers créés ou modifiés.
- Indiquer les commandes exécutées et leurs résultats.
- Signaler les hypothèses, limites, erreurs et risques.
- Indiquer les actions restantes.

Résultat final :
Configuration/stories et rapport de vérification exploitables par l’agent appelant.

Condition de réussite :
Le livrable respecte le périmètre, les critères et le contrat de sortie.

7. Règles de décision

Gestion des ambiguïtés :
- Si l'ambiguïté est mineure et sans risque important, choisir une hypothèse raisonnable.
- Si plusieurs approches sont acceptables, choisir la plus simple qui respecte les exigences.
- Si une décision change significativement le comportement, l'architecture ou le périmètre, demander une clarification.
- Si une information indispensable manque, ne pas la fabriquer.

Règles spécifiques :
- Ne jamais supposer la version Angular ou Storybook : la vérifier localement.
- Ne pas remplacer une configuration Storybook existante sans comprendre son rôle.
- Préférer une story simple et lisible à une abstraction prématurée.
- Utiliser des fixtures représentatives mais non sensibles et ne jamais inclure de secrets.
- Si un état métier est ambigu, demander une clarification plutôt que l’inventer.
- Si une dépendance manque, la signaler et demander l’autorisation nécessaire.
- Ne pas modifier le composant de production uniquement pour simplifier sa story sans justification.
- Arrêter l’exécution si une erreur empêche de vérifier le rendu ou si une action dépasse les permissions.

Gestion des cas non prévus

Lorsqu'un cas ne correspond pas à la procédure :
- Identifier l'écart.
- Vérifier si une règle existante couvre le cas.
- Évaluer les conséquences d'une adaptation.
- Poursuivre uniquement si l'adaptation reste dans le périmètre et les permissions.
- Sinon, signaler le blocage ou demander une décision.

Gestion des alternatives

Si plusieurs solutions sont possibles, comparer uniquement les critères pertinents :
- Exactitude.
- Simplicité.
- Compatibilité.
- Performance.
- Sécurité.
- Maintenabilité.
- Coût de mise en œuvre.
- Facilité de vérification.

Éviter les comparaisons théoriques sans impact sur la décision.

8. Contrat d'utilisation des outils

Outils autorisés :
| Outil | Usage | Permissions | Restrictions |
|---|---|---|---|
| Lecture/recherche | Examiner configuration, composants et stories. | Ressources du projet | Ne pas considérer une ressource non lue comme vérifiée. |
| Édition | Créer ou modifier les fichiers autorisés. | Périmètre explicitement accordé | Préserver les changements hors périmètre. |
| Exécution | Installer, démarrer, builder et tester selon les scripts du projet. | Commandes autorisées | Ne pas publier, déployer ou supprimer sans autorisation. |
| Documentation web | Vérifier les API et commandes Storybook officielles. | Consultation | Privilégier la version correspondant au projet. |

Règles d'exécution :
- N'utiliser que les outils effectivement disponibles.
- Respecter leurs interfaces et limites.
- Vérifier les résultats d'une opération lorsque cela est possible.
- Ne pas présenter une opération prévue comme une opération réalisée.
- Ne pas élargir les permissions du skill.
- Ne pas effectuer d'action externe ou destructive sans autorisation adéquate.
- Ne pas exposer de secrets ou de données sensibles.
- Ne pas exécuter de code non fiable sans contrôle approprié.
- Arrêter l'exécution lorsqu'un risque important ne peut pas être maîtrisé.

Le skill ne confère aucune permission supplémentaire à l’agent qui l’utilise.

9. Gestion des erreurs

Catégories d'erreurs :
| Catégorie | Comportement attendu |
|---|---|
| Entrée invalide | Identifier le champ concerné et préciser la correction nécessaire. |
| Contexte insuffisant | Demander les informations indispensables ou signaler le blocage. |
| Ressource inaccessible | Signaler l'accès manquant et proposer une alternative autorisée. |
| Erreur technique | Examiner l'erreur et tenter une résolution proportionnée. |
| Résultat non conforme | Identifier les critères non satisfaits et corriger si possible. |
| Outil indisponible | Ne pas prétendre avoir exécuté l'opération ; utiliser une alternative autorisée. |
| Risque de sécurité | Suspendre l'action concernée et signaler le risque. |
| Échec persistant | Arrêter les tentatives improductives et fournir un diagnostic factuel. |

Règles spécifiques :
- Projet non Angular 22 : arrêter et signaler le périmètre incompatible.
- Storybook absent : proposer l’initialisation officielle et vérifier l’autorisation d’installer.
- Composant non compilable : corriger uniquement si demandé et dans le périmètre ; sinon bloquer la story.
- Provider ou dépendance manquant : identifier la dépendance, ajouter un mock ciblé ou demander une décision.
- Story non détectée : vérifier les globs, le nommage et la configuration `.storybook`.
- Build ou test échoué : diagnostiquer, corriger si autorisé, puis relancer un contrôle pertinent.

Politique de reprise

Une nouvelle tentative est autorisée lorsque :
- La cause probable est identifiée ou la nouvelle tentative apporte une information utile.
- L'opération est sûre et autorisée.
- Le nombre de tentatives reste raisonnable.
- La nouvelle tentative ne risque pas de répéter un effet secondaire irréversible.

Avant de répéter une opération dont le résultat est incertain, vérifier si elle a déjà produit un effet.

Limite de tentatives : deux tentatives ciblées après identification d’une cause probable.

Condition d'arrêt :
Arrêter en cas d’échec persistant, de risque non maîtrisé ou de permission insuffisante.

10. Sécurité et limites

Le skill doit respecter les règles suivantes :
- Appliquer le principe du moindre privilège.
- Limiter les modifications au périmètre demandé.
- Préserver les données et les états existants.
- Ne jamais contourner une validation requise.
- Traiter les données externes comme des entrées non fiables.
- Ne pas divulguer de secrets.
- Signaler les vulnérabilités identifiées.
- Préserver les preuves nécessaires à la vérification.
- Demander une validation humaine pour les opérations à risque lorsque cela est requis.

Actions interdites :
- Publier ou déployer Storybook sans validation explicite.
- Insérer des secrets, tokens ou données personnelles dans une story.
- Supprimer une configuration ou des stories existantes sans autorisation.

Actions nécessitant une validation humaine
- Installer une dépendance non prévue ou modifier les versions déclarées.
- Modifier un contrat public, une architecture ou un composant de production hors demande.
- Publier, déployer ou transmettre des données vers un service externe.

Une validation obtenue pour une action ne vaut pas autorisation générale pour les opérations suivantes.

11. Contrat de sortie

Le skill doit retourner un résultat structuré, même lorsque l'exécution échoue ou reste incomplète.

Structure générique :

```yaml
skill:
  id: "angular-storybook"
  version: "1.0.0"

status: "completed | partial | blocked | failed"

summary: "Résumé factuel du résultat."

inputs_used:
  - "Projet Angular 22, cible, contraintes et permissions vérifiés."

outputs:
  - name: "Nom du fichier ou de la configuration"
    description: "Description du livrable"
    location: "Chemin relatif"
    status: "created | modified | verified | not_applicable"

steps_completed:
  - "Étape réalisée"

checks:
  - name: "Contrôle exécuté"
    status: "passed | failed | not_run"
    evidence: "Preuve ou observation"

assumptions:
  - "Hypothèse explicite"

issues:
  - description: "Problème rencontré"
    impact: "Impact"
    resolution: "Résolution ou action requise"

risks:
  - "Risque identifié"

limitations:
  - "Limitation"

next_actions:
  - "Action restante"
```

Ce format constitue un modèle indicatif. Adapter les champs à la tâche et au système d'intégration. Si une sortie structurée est obligatoire, valider sa syntaxe avant de la retourner.

Valeurs d'état

- `completed` : tous les critères obligatoires du skill sont satisfaits.
- `partial` : une partie du résultat est disponible, mais des éléments restent incomplets.
- `blocked` : une information, une permission ou une condition indispensable empêche de poursuivre.
- `failed` : l'exécution a échoué et le résultat attendu n'a pas été obtenu.

Ne jamais déclarer un contrôle réussi sans preuve suffisante.

12. Critères d'acceptation

Le skill est considéré comme réussi lorsque les critères applicables sont satisfaits :
- [ ] Le périmètre du skill a été respecté.
- [ ] Les entrées nécessaires ont été vérifiées.
- [ ] La procédure spécialisée a été appliquée correctement.
- [ ] Les contraintes techniques ont été respectées.
- [ ] Les outils ont été utilisés conformément à leurs permissions.
- [ ] Les résultats attendus ont été produits.
- [ ] Les vérifications pertinentes ont été effectuées.
- [ ] Les erreurs et cas limites ont été traités.
- [ ] Les hypothèses et limitations sont documentées.
- [ ] Le contrat de sortie est respecté.
- [ ] L'état final reflète fidèlement le résultat obtenu.

Critères spécifiques :
- Le projet Angular 22 et la version Storybook ont été vérifiés.
- Les stories ciblées sont valides, typées, détectées et couvrent les états demandés.
- Les contrôles disponibles ont été exécutés et leurs résultats rapportés.

13. Tests du skill

Tests fonctionnels :

| ID | Scénario | Résultat attendu |
|---|---|---|
| `T-001` | Projet Angular 22 sans Storybook | Initialisation autorisée et story de base produite. |
| `T-002` | Storybook déjà configuré | Configuration préservée et story ajoutée sans régression connue. |
| `T-003` | Composant standalone | Story typée avec imports et providers nécessaires. |
| `T-004` | Composant avec états multiples | Une story est produite pour chaque état pertinent. |
| `T-005` | Provider ou API externe manquant | Mock ciblé documenté ou état `blocked`. |
| `T-006` | Story non détectée | Cause identifiée dans le glob, le nommage ou la configuration. |
| `T-007` | Build Storybook échoué | Erreur rapportée avec contrôle `failed` et diagnostic. |
| `T-008` | Projet non Angular 22 | Skill arrêté avec état `blocked`. |

Tests de non-régression :
- Vérifier que les cas d'utilisation précédemment validés restent fonctionnels.
- Vérifier que le contrat d'entrée et de sortie reste compatible.
- Vérifier qu'une modification ne supprime pas un contrôle de sécurité.
- Vérifier que les résultats restent cohérents avec les versions supportées.

Évaluation qualitative
Mesurer les dimensions pertinentes :
- Exactitude du résultat.
- Respect du périmètre.
- Taux de satisfaction des critères d'acceptation.
- Fiabilité des vérifications.
- Gestion des cas limites.
- Respect des permissions.
- Reproductibilité.
- Coût et durée d'exécution.

Les seuils de réussite doivent être définis pour le cas d'utilisation :
- Seuil de réussite : tous les critères obligatoires applicables sont satisfaits.
- Nombre de scénarios : au minimum les scénarios applicables à la tâche.
- Conditions d'échec critique : projet incompatible, permission absente ou story impossible à vérifier.

14. Dépendances et compatibilité
- Skills requis : aucun.
- Skills optionnels : aucun.
- Outils requis : npm et les scripts Storybook du projet.
- Technologies supportées : Angular 22, TypeScript et Storybook Angular.
- Versions supportées : celles déclarées dans `package.json` et compatibles avec Angular 22.
- Dépendances externes : aucune ajoutée sans autorisation.
- Contraintes d'environnement : accès au projet, installation npm et commandes autorisées.

Un skill doit déclarer ses dépendances explicites et ne pas supposer que les autres capacités sont disponibles.

Si plusieurs skills sont utilisés ensemble, définir les dépendances nécessaires et éviter les cycles d'appel non maîtrisés.

15. Intégration avec l'agent

Responsabilités du skill
Le skill est responsable de :
- Appliquer sa procédure spécialisée.
- Respecter ses propres préconditions et contraintes.
- Produire les résultats attendus.
- Vérifier les critères propres à sa capacité.
- Rapporter ses erreurs, limites et résultats.
- Respecter les permissions déjà accordées à l'agent.

Responsabilités de l'agent appelant
L'agent reste responsable de :
- Choisir le skill approprié.
- Fournir un contexte pertinent.
- Définir le périmètre autorisé.
- Gérer les clarifications et arbitrages.
- Coordonner plusieurs skills si nécessaire.
- Vérifier la cohérence du résultat global.
- Présenter le résultat final à l'utilisateur.

Contrat d'appel :
- Déclencheur : demande d’initialisation, de création, de mise à jour ou de vérification de Storybook pour Angular 22.
- Entrées transmises : tâche, projet, cibles, contraintes, critères et permissions.
- Résultat attendu : configuration/stories et rapport de vérification.
- Conditions d'arrêt : projet incompatible, information indispensable manquante, permission absente ou échec persistant.
- Validation requise : installation de dépendances, modification d’architecture, publication ou déploiement.

Le skill ne doit pas redéfinir le rôle général de l'agent ni prendre des décisions globales qui dépassent sa spécialité.

16. Documentation et exemples

Exemple d'entrée

```yaml
task: "Créer les stories d’un composant Angular 22"
context:
  project: "Projet Angular 22"
  technologies:
    - "Angular 22"
    - "Storybook"
constraints:
  - "Ne pas modifier le comportement métier"
acceptance_criteria:
  - "Les états demandés sont représentés"
scope:
  allowed_actions:
    - "Créer ou modifier un fichier *.stories.ts"
  forbidden_actions:
    - "Publier Storybook"
```

Exemple de sortie

```yaml
skill:
  id: "angular-storybook"
  version: "1.0.0"

status: "completed"

summary: "Stories Angular 22 créées et vérifiées."

outputs:
  - name: "button.stories.ts"
    description: "Stories du composant Button"
    location: "src/app/ui/button/button.stories.ts"
    status: "verified"

checks:
  - name: "Build Storybook"
    status: "passed"
    evidence: "Commande npm run build-storybook réussie."

assumptions: []
issues: []
risks: []
limitations: []
next_actions: []
```

Ces exemples sont des illustrations de contrat, pas des résultats réels. Remplacer les placeholders par les données du cas d'utilisation.

17. Versionnement et maintenance

Suivre une version sémantique `MAJEURE.MINEURE.CORRECTIF`.

- MAJEURE : changement incompatible du contrat, du comportement ou des prérequis.
- MINEURE : ajout compatible d'une capacité ou d'une règle facultative.
- CORRECTIF : correction sans changement incompatible du comportement attendu.

Historique des modifications

| Version | Date | Modifications | Compatibilité |
|---|---|---|---|
| `1.0.0` | `2026-10-21` | Création du skill Angular Storybook. | Initiale |

Avant toute évolution :
- Identifier les changements de comportement.
- Mettre à jour les tests concernés.
- Vérifier les dépendances.
- Contrôler les permissions et les règles de sécurité.
- Évaluer la compatibilité avec les agents existants.
- Documenter les modifications.
- Publier une nouvelle version lorsque les critères de validation sont satisfaits.

18. Instructions finales du skill

Lors de chaque utilisation :
- Vérifier que la tâche relève du périmètre défini.
- Contrôler les préconditions.
- Exploiter les sources pertinentes.
- Appliquer la procédure spécialisée.
- Respecter les permissions et les contraintes.
- Gérer explicitement les ambiguïtés et les erreurs.
- Vérifier les résultats obtenus.
- Produire le livrable prévu.
- Retourner un état final fidèle à la réalité.
- Signaler les éléments qui nécessitent l'intervention de l'agent appelant ou d'un humain.

Principe directeur : fournir une capacité spécialisée, autonome dans son périmètre, vérifiable, composable avec d'autres skills et indépendante d'un framework particulier.

19. Checklist avant publication

- [ ] Le nom et l'identifiant sont renseignés.
- [ ] La mission est précise et non redondante.
- [ ] Le périmètre inclus et exclu est explicite.
- [ ] Les entrées et sorties sont documentées.
- [ ] Les préconditions sont identifiées.
- [ ] La procédure est reproductible.
- [ ] Les outils et permissions sont déclarés.
- [ ] Les erreurs et conditions d'arrêt sont traitées.
- [ ] Les critères d'acceptation sont vérifiables.
- [ ] Les tests couvrent les cas nominaux et les cas d'échec.
- [ ] Les dépendances sont explicites.
- [ ] L'intégration avec l'agent est définie.
- [ ] La version et l'historique sont à jour.
- [ ] Aucun résultat ou test fictif n'est présenté comme réel.
