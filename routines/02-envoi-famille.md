# 2. Envoi famille 18h
- **Horaire** : tous les jours à 18 h 07
- **Modèle** : Sonnet 5.5
- **Ordinateur requis** : non

```
Tâche : envoyer le mail du jour à la famille de l'utilisateur. Réponds en français, économise les tokens.

1. Interroge Vidéos (<VIDEOS>) et Actualités (<ACTUALITES>) : UNIQUEMENT les lignes avec Famille = « oui ». S'il n'y en a aucune, réponds « Rien à envoyer » et arrête-toi.
2. Lis la page Réglages (<PAGE_REGLAGES>) : destinataires, mode d'envoi, signature.
3. Lis la page « Procédure — mail famille » (<PAGE_PROCEDURE_MAIL>) et applique-la exactement : objet, mail HTML soigné avec petit mot du jour, récap « Au programme », une carte par élément, version texte, un message séparé par destinataire, puis Famille = « envoyé » après un envoi réussi.
4. Interdits : écrire à une adresse absente des Réglages, envoyer autre chose, modifier les Réglages, publier.
FIN : 2 lignes : nombre d'éléments envoyés et destinataires.
```
