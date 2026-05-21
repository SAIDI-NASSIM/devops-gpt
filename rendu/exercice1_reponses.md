### Exercice 1 : Conception Logicielle

#### 1. Diagramme de Contexte

Le diagramme de contexte illustre les interactions entre le système **DevOpsGPT** et ses acteurs externes.

*   **Acteurs externes :**
    *   **Utilisateur** : Interagit avec le système pour poser des questions et recevoir des réponses.
    *   **API GPT-4** : Fournit les capacités de génération de langage pour répondre aux questions.
    *   **Base de données** : Stocke les informations persistantes, comme l'historique des conversations.

*   **Flux de données principaux :**
    1.  **Utilisateur -> DevOpsGPT** : Envoi d'une `Question`.
    2.  **DevOpsGPT -> Utilisateur** : Affichage d'une `Réponse`.
    3.  **DevOpsGPT -> API GPT-4** : Envoi d'un `Prompt` (la question de l'utilisateur, potentiellement enrichie).
    4.  **API GPT-4 -> DevOpsGPT** : Réception d'une `Réponse générée`.
    5.  **DevOpsGPT -> Base de données** : Sauvegarde de l' `Historique de la conversation` (question + réponse).

#### 2. Organigramme (Étapes de fonctionnement)

Voici les étapes quand un utilisateur envoie un message :

1.  **Début** : L'utilisateur envoie un message.
2.  **Réception** : Le système reçoit le message.
3.  **Vérification** : Le système vérifie si le message contient des mots interdits (insultes).
    - **Si oui** : Le processus s'arrête et un message d'erreur peut être affiché.
    - **Si non** : On passe à l'étape suivante.
4.  **Envoi à l'IA** : Le message est envoyé à l'API GPT-4.
5.  **Sauvegarde** : La réponse de l'API est sauvegardée dans la base de données.
6.  **Affichage** : La réponse est montrée à l'utilisateur sur l'interface.
7.  **Fin**.

#### 3. Dictionnaire de données pour un "Message"

Voici les informations à stocker pour chaque message échangé.

| Nom de la donnée | Type          | Description                                                  |
| ---------------- | ------------- | ------------------------------------------------------------ |
| `ID_Message`     | Numérique     | Un numéro unique pour identifier chaque message.             |
| `Contenu`        | Texte (String)| Le texte du message, que ce soit la question ou la réponse.  |
| `Date_Creation`  | Date/Heure    | La date et l'heure exactes de la création du message.        |
| `Auteur`         | Texte (String)| Qui a écrit le message : "Utilisateur" ou "IA".              |
