### Exercice 2 : Git et Docker

#### 1. Méthodologie et Git

**Question A : User Story pour "Abonnement Premium"**

*   **En tant que** utilisateur régulier de DevOpsGPT,
*   **je veux** pouvoir souscrire à un abonnement "Premium",
*   **afin de** bénéficier de fonctionnalités exclusives comme des réponses plus rapides et un historique de conversation illimité.

**Question B : Commandes Git (Workflow complet simulé)**

Voici la séquence complète des commandes pour simuler le développement, la fusion et le tag, comme nous l'avons exécuté.

1.  **Créer la branche et simuler le développement :**
    ```bash
    # Crée la branche et bascule dessus
    git checkout -b feature-premium-subscription

    # Crée un fichier temporaire pour simuler l'ajout de code
    touch premium_feature.tmp
    git add premium_feature.tmp

    # Fait le commit sur la branche de fonctionnalité
    git commit -m "feat: Add placeholder for premium subscription"
    ```

2.  **Fusionner la fonctionnalité sur `main` :**
    ```bash
    # Revenir sur la branche principale
    git checkout main

    # Fusionner la branche de fonctionnalité dans main
    git merge feature-premium-subscription
    ```

3.  **Pousser les changements sur GitHub :**
    ```bash
    # Pousser la branche main et la nouvelle branche de fonctionnalité
    git push origin main
    git push origin feature-premium-subscription
    ```

4.  **Créer et pousser le tag de version :**
    ```bash
    # Créer le tag
    git tag -a v1.0.0 -m "Version 1.0.0: Initial release with premium feature"

    # Pousser le tag sur le serveur
    git push origin v1.0.0
    ```

5.  **Nettoyage (optionnel mais bonne pratique) :**
    ```bash
    # Supprimer le fichier temporaire et commiter le nettoyage
    git rm premium_feature.tmp
    git commit -m "chore: Remove temporary file"
    git push origin main

    # Supprimer la branche de fonctionnalité distante qui a été fusionnée
    git push origin --delete feature-premium-subscription
    ```
