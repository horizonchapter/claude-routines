# Structure Notion

Une page **Routines Claude** (`<PAGE_ROUTINES>`) qui contient :

## Page Réglages (`<PAGE_REGLAGES>`)
Lignes de texte que les routines lisent :
- **Focus actuel** : ton projet prioritaire.
- **Demain je travaille sur** : rempli par toi, prioritaire pour la veille.
- **Proposition de Claude pour demain** : rempli par le suivi du soir.
- **Thèmes** : tes projets (01 à 08, par exemple).
- **Chaînes YouTube suivies** et **Chaînes découvertes**.
- **Destinataires famille**, **Mode d'envoi** (brouillon ou envoi), **Signature**.

## Bases de données

| Base | Propriétés principales |
|---|---|
| **Vidéos** (`<VIDEOS>`) | Titre, Publié le, Chaîne, Lien, Thème, Abonnement (case), Pourquoi utile, Action à essayer, Résumé basé sur, Statut (À regarder / Vu / Utile / Pas intéressant), Important (case), Famille (idée Claude / proposé / envoyé), Semaine (relation) |
| **Actualités** (`<ACTUALITES>`) | mêmes propriétés + Source et Type, sans Chaîne ni Abonnement |
| **Semaines** (`<SEMAINES>`) | Titre, Début, Fin, relations Vidéos et Actualités |
| **Journal de bord** (`<JOURNAL_DE_BORD>`) | Fait, Date, Outil, Projet, Décisions, Prochaine étape, Bloqué par |
| **Journal d'amélioration** (`<JOURNAL_AMELIORATION>`) | Observation, Date, Projet, Proposition (skill / mod / habitude / outil), Détail, Statut, Récurrent |
| **Suivi du soir** (`<SUIVI_DU_SOIR>`) | Jour, Date, En une phrase, Note de la journée, Proposition pour demain |

## Page Procédure mail famille (`<PAGE_PROCEDURE_MAIL>`)
Le gabarit du mail : objet, petit mot du jour, récap, une carte par élément, version texte, liens directs (pas de redirection), un message par destinataire.

Astuce : une formule « Nouveau » (`dateBetween(now(), prop("Publié le"), "days") <= 1`) permet d'afficher une étiquette sur les éléments du jour.
