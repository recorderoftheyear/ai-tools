---
name: executer-tests-defensifs
description: Exécute les suites de tests défensifs prédéfinies du projet et consigne les écarts observés.
---

# Exécuter les tests défensifs applicatifs

Version initiale du skill : v0.2.0.

1. Identifie la fonctionnalité, les règles attendues et la commande de test documentée par le projet. En vocal, pose une question à la fois.
2. Vérifie que la suite utilise uniquement un environnement local ou de préproduction approuvé, des comptes fictifs et des données de test. Si la cible ou la configuration est incertaine, arrête-toi et demande la précision nécessaire.
3. Examine les assertions avant l'exécution. Par exemple, un enseignant peut consulter un dossier de sa classe. Un dossier fictif hors de sa classe doit donner lieu à un refus, sans renvoyer ses données. Utilise le client de test du projet et les fixtures prévues.
4. Exécute uniquement la suite défensive identifiée, avec les commandes du projet. Si elle manque, propose des tests fonctionnels ciblés et fais valider leur périmètre avant de les exécuter. Exclue la production, les tests de charge et les outils offensifs.
5. Rapporte chaque contrôle avec son résultat attendu, le résultat observé, la preuve expurgée et la prochaine action. Distingue réussi, échoué, bloqué et non exécuté. Après correction, relance le test ciblé et indique ce que le résultat confirme.
