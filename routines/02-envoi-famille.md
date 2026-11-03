# 2. Envoi famille 18h
- **Horaire** : tous les jours à 18 h 04
- **Modèle** : Sonnet 5.5
- **Ordinateur requis** : non

```
Tâche : envoyer le mail du jour à la famille de l'utilisateur. Réponds en français, économise les tokens. Pour lire Notion, utilise le mode « rows » avec un filtre, une base à la fois (pas de SQL : son plan Notion le limite).

0. STOP : cherche dans Gmail les réponses reçues ces 2 derniers jours venant des adresses de la page Réglages (<PAGE_REGLAGES>) et contenant « STOP ». Pour chaque adresse trouvée, retire-la de « Destinataires famille » dans les Réglages (seule modification autorisée) et signale-le dans le résumé final.
1. Interroge Vidéos (<VIDEOS>) puis Actualités (<ACTUALITES>) : UNIQUEMENT les lignes avec Famille = « proposé » (c'est le choix de l'utilisateur ; « idée Claude » n'est qu'une suggestion, ne l'envoie jamais). S'il n'y en a aucune, réponds « Rien à envoyer » et arrête-toi.
2. Lis la page Réglages : destinataires, mode d'envoi, signature.
3. Lis la page « Procédure — mail famille » (<PAGE_PROCEDURE_MAIL>) et applique-la exactement : objet, mail HTML soigné avec petit mot du jour, récap « Au programme », une carte par élément, liens directs d'origine, version texte, un message séparé par destinataire, puis Famille = « envoyé » après un envoi réussi.
4. Interdits : écrire à une adresse absente des Réglages, envoyer autre chose, modifier les Réglages au-delà du retrait STOP, publier.
FIN : 2 lignes : nombre d'éléments envoyés, destinataires, et les éventuels STOP traités.
```
