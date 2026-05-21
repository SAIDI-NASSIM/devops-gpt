### Exercice 2 : Git et Docker

#### 1. Méthodologie et Git

**Question A : User Story pour "Abonnement Premium"**

*   **En tant que** utilisateur régulier de DevOpsGPT,
*   **je veux** pouvoir souscrire à un abonnement "Premium",
*   **afin de** bénéficier de fonctionnalités exclusives comme des réponses plus rapides et un historique de conversation illimité.

**Question B : Commandes Git**

1.  **Créer la branche, faire un commit et la pousser :**
    ```bash
    # Crée la branche et bascule dessus
    git checkout -b feature-premium-subscription

    # Après avoir modifié les fichiers, les ajouter
    git add .

    # Faire le commit
    git commit -m "feat: Implement premium subscription feature"

    # Pousser la branche sur le dépôt distant
    git push --set-upstream origin feature-premium-subscription
    ```

2.  **Créer un tag de version après fusion sur `main` :**
    ```bash
    # Basculer sur la branche principale
    git checkout main

    # S'assurer qu'elle est à jour
    git pull origin main

    # Créer le tag
    git tag -a v1.0.0 -m "Version 1.0.0: Initial release with premium feature"
    ```

3.  **Pousser le tag sur le serveur GitHub :**
    ```bash
    git push origin v1.0.0
    ```
