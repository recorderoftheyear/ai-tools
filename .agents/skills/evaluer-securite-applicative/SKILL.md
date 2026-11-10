---
name: evaluer-securite-applicative
description: Évalue les contrôles de sécurité d’une application à partir de son architecture, de son code et de sa configuration, puis documente et reteste les écarts.
---

# Évaluer la sécurité d’une application

Version : v0.3.1.

1. **Cadrer.** Confirme les composants inclus, le propriétaire, les exclusions et l’environnement local ou de préproduction autorisé. Utilise des comptes et des données fictifs. Si l’environnement reste incertain, poursuis la revue documentaire et marque les tests comme bloqués.
2. **Cartographier.** À partir du code, de la documentation et de la configuration fournis, recense les interfaces, les rôles, les données sensibles, les intégrations et les frontières de confiance. Indique la source de chaque élément et les zones encore inconnues.
3. **Évaluer.** Déduis les contrôles attendus de cette carte et des règles métier. Priorise les accès, la séparation des données, les sessions, la validation des entrées, les secrets et la configuration selon les risques observés. Pour chaque contrôle, précise le comportement attendu et la preuve nécessaire.
4. **Vérifier.** Examine le code et la configuration. Réutilise les tests du projet. Si aucun test pertinent n’existe, écris des tests fonctionnels ciblés avec le client de test et les fixtures du projet. Par exemple, vérifie qu’un rôle autorisé peut effectuer une action et qu’un rôle sans ce droit reçoit un refus et qu’aucune donnée protégée n’est renvoyée. Exécute les vérifications approuvées en local ou en préproduction. Limite les actions aux revues et aux tests fonctionnels défensifs.
5. **Rapporter et retester.** Pour chaque contrôle, consigne le comportement attendu, le résultat observé, la preuve expurgée, le statut et la prochaine action. Distingue vérifié, écart confirmé, non vérifié et bloqué. Priorise les corrections selon leur impact et leur exposition. Après correction, relance le test ciblé et consigne le nouveau résultat.

Utilise le canal choisi par la personne, à l’écrit ou en vocal. À l’écrit, regroupe les questions liées quand cela facilite la réponse. En vocal, pose une question à la fois. Dans les deux modes, termine chaque étape avec la prochaine action et les preuves encore manquantes.
