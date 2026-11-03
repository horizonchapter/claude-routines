# 1. Veille quotidienne 10h (vidéos + actualités)
- **Horaire** : tous les jours à 9 h 43 (prête pour 10 h)
- **Modèle** : Sonnet 5.5
- **Ordinateur requis** : non

```
Tâche : veille quotidienne de l'utilisateur (prête pour 10 h). Réponds en français. Sois précis, ne fabrique jamais rien, économise les tokens (14 recherches WebSearch au maximum, plus les vérifications nécessaires ; WebFetch une page YouTube à la fois, sinon limite de débit). Pour lire Notion, utilise le mode « rows » avec des filtres, une base à la fois (pas de SQL : son plan Notion le limite).

RÉFÉRENCES NOTION
- Réglages : <PAGE_REGLAGES>
- Vidéos : <VIDEOS>
- Actualités : <ACTUALITES>
- Semaines : <SEMAINES>

ÉTAPE 0 : SEMAINE (Europe/Paris)
- Cherche dans Semaines la page dont Début ≤ aujourd'hui ≤ Fin. Si elle n'existe pas, crée-la : titre « Semaine du JJ/MM au JJ/MM » (lundi au dimanche), Début et Fin remplis.
- Si on est lundi : pour la semaine précédente, compte ses vidéos et actualités (relations Vidéos et Actualités de sa page) et crée dans sa page une sous-page « Récap semaine du JJ/MM au JJ/MM » contenant : total vidéos, total actualités ; total IA (Thème Claude + IA) ; total projets avec le détail par thème (01 à 08) ; total envoyé à la famille (Famille = envoyé) ; les 3 éléments marqués Important ; ce qui a plu (Utile, Important) et ce qui n'a pas plu (Pas intéressant). Ajoute aussi un résumé de 4 lignes en haut de la page de cette semaine précédente. Ne fais ce récap qu'une fois (vérifie qu'il n'existe pas déjà).

ÉTAPE 1 : CONTEXTE ET GOÛTS (APPRENTISSAGE À PARTIR DE SES RETOURS)
- Lis la page Réglages : « Demain je travaille sur » (prioritaire s'il est rempli), sinon « Proposition de Claude pour demain », puis « Focus actuel », thèmes, « Chaînes YouTube suivies », « Chaînes découvertes ».
- Récupère les liens des 14 derniers jours dans Vidéos et Actualités pour éviter les doublons (pour les vidéos, vérifie aussi qu'une vidéo n'a jamais été ajoutée avant : même lien = doublon).
- Retours de l'utilisateur, à lire AVANT toute recherche : interroge Vidéos puis Actualités (une base à la fois) avec filtre sur Statut = Utile, puis Statut = Vu, puis Statut = Pas intéressant, puis Important coché, sur les 90 derniers jours (le plus récent compte le plus). Analyse et retiens :
  1. Utile / Important / Vu = à privilégier : les chaînes, les sources, les sujets, les types de contenu (tutoriel, test, comparatif, formation, actualité produit), la langue, la longueur, le niveau de détail, la fraîcheur.
  2. Pas intéressant = à éviter : même chaîne, même source, même sujet, même style de contenu (par exemple actualités financières, boursières ou sécurité si elles ressortent).
  3. Chaîne, source ou sujet qui revient plusieurs fois en Utile : cherche d'abord ses nouveautés, et cherche des chaînes, sources et sujets voisins.
  4. Construis tes requêtes de recherche à partir de ces enseignements (mots-clés des titres Utile, chaînes et sources appréciées, formats appréciés), pas à partir de requêtes génériques.
  Ces retours priment sur tes propres choix et sur les thèmes par défaut. S'il y a trop peu de retours (moins de 5), utilise les Réglages et dis-le dans le résumé final.

ÉTAPE 2 : 6 VIDÉOS YOUTUBE EN FRANÇAIS SUR L'IA (QUOTA TOUJOURS REMPLI)
- Règle de l'utilisateur : toujours 6 vidéos par jour, jamais moins. Si tu n'en trouves pas assez de récentes, élargis. Les vidéos que l'utilisateur ajoute lui-même ne comptent jamais dans ce quota.
- Sujets : l'IA en général, Claude en priorité (Claude Code, Claude, skills, mods, MCP, agents, automatisation, nouveaux outils), mais aussi les autres IA (ChatGPT/OpenAI, Gemini, etc.), les comparatifs de modèles, les tests, et les formations pour maîtriser parfaitement l'IA. De préférence liées au focus ou à ce qu'il travaille demain, et alignées sur ce que l'étape 1 a appris de ses goûts. Au moins 3 sur Claude.
- Fraîcheur : d'abord les 30 derniers jours (les plus récentes en priorité). S'il en manque pour atteindre 6, remonte jusqu'à 2 à 3 mois en arrière, puis au-delà seulement en dernier recours. Une vidéo plus ancienne reste acceptable si elle est utile pour savoir utiliser Claude ou l'IA ; dans ce cas dis-le dans « Pourquoi utile » (par exemple « plus ancienne, versions de modèles dépassées »).
- Projets (business, e-commerce, SaaS, Roblox, design, marketing, anglais) : facultatif, uniquement en plus des 6 vidéos IA, jamais à leur place.
- Commence par les chaînes suivies et découvertes (cherche leurs vidéos récentes via WebSearch ; les flux RSS YouTube et les pages de chaînes sont inaccessibles aux robots, ne les contourne pas) et coche Abonnement pour celles-ci. Complète avec d'autres chaînes sérieuses. Si une nouvelle chaîne est excellente et régulière, ou si une chaîne revient souvent en Utile, ajoute son nom dans « Chaînes découvertes » (seule modification autorisée dans Réglages).
- Actionnables. Pas de promesses d'argent facile, pas de putaclic.

ÉTAPE 3 : 6 ACTUALITÉS À NE PAS RATER (RECHERCHÉES, TRIÉES ET CLASSÉES)
- Au moins 4 sur l'IA, Claude en priorité (sorties, nouveautés, modèles, outils, annonces importantes de toutes les IA) ; jusqu'à 2 utiles à ses projets.
- 7 derniers jours.
- OÙ CHERCHER (l'utilisateur veut surtout X, Reddit et les blogs, ce sont les sources les plus riches) :
  1) REDDIT, tous les jours, via l'outil Firecrawl (connecté) : 3 recherches firecrawl_search au maximum par jour, avec des requêtes « site:reddit.com/r/NOM » sur r/ClaudeAI, r/LocalLLaMA et un troisième subreddit au choix du jour (r/ClaudeCode, r/singularity, r/OpenAI, r/ChatGPT, r/artificial ou r/Entrepreneur selon le focus). Lis ensuite en entier les 1 à 2 fils les plus pertinents avec firecrawl_scrape. Coût estimé : environ 2 crédits par tranche de 10 résultats.
  2) X, DEUX FOIS PAR SEMAINE SEULEMENT (le mardi et le vendredi, heure de Paris), via Firecrawl : au maximum 2 appels ce jour-là, avec la source dédiée « x-com » (capacité posts/search pour chercher des posts publics par sujet ; capacité users/posts pour analyser les posts d'un compte précis sur une période, par exemple Anthropic, ClaudeDevs, OpenAI, Google DeepMind). Avant le premier appel X, lis le contrat avec firecrawl_find_tools (providers = x-com, capabilities = posts/search puis users/posts, discovery gratuite) et respecte exactement ses options. Chaque appel X coûte 30 crédits : ne dépasse jamais 2 appels X par jour de veille, et aucun les autres jours. Ce sont des échantillons de posts résumés avec leurs liens, pas un fil complet en temps réel.
  3) BLOGS : anthropic.com/news, claude.com/blog, openai.com, blog.google (la source dédiée « blog-google » de Firecrawl existe aussi, 5 crédits par appel, utilise-la seulement si une recherche web ne suffit pas), blogs de développeurs et newsletters IA, via WebSearch.
  4) Médias tech sérieux en complément.
- BUDGET FIRECRAWL (forfait de l'utilisateur : environ 1 000 crédits par mois, le plan exact n'est pas vérifié) : vise environ 660 crédits par mois au total (Reddit tous les jours, X deux fois par semaine). Si un appel Firecrawl répond qu'il n'y a plus de crédits, ou une erreur de quota, arrête immédiatement d'utiliser Firecrawl ce jour-là, bascule sur WebSearch pour le reste, et signale-le dans le résumé final (« crédits Firecrawl épuisés ou erreur »). Ne dépense jamais de crédits au-delà de ce plan, ne lance aucune action payante hors X, Reddit et blog-google, et ne te connecte à aucun compte X ou Reddit de l'utilisateur.
- Les posts X ou Reddit servent à DÉTECTER l'info : le lien enregistré doit être, de préférence, la source primaire vérifiée (annonce officielle, billet de blog) ; un fil Reddit ou un post X peut être enregistré seulement s'il apporte lui-même l'information (test, retour d'usage, fuite signalée comme non confirmée) et que sa date est vérifiée. Si une page n'est pas lisible, remonte à la source primaire pour vérifier, sinon écarte ; ne contourne aucun blocage.
- TRI : avant d'écrire, classe tous les candidats de 1 à 6 par importance réelle pour l'utilisateur (impact sur son usage de Claude et de l'IA, nouveauté, fiabilité de la source, adéquation avec ce que l'étape 1 a appris de ses goûts) ; élimine les doublons de sujet (une seule ligne par événement) ; privilégie une diversité de sujets. Crée les lignes dans l'ordre du classement, la plus importante en premier. Précise dans « Pourquoi utile » pourquoi l'info compte (une phrase). Signale clairement ce qui est rumeur ou non confirmé.
- Titre en français, même si la source est en anglais.

ÉTAPE 4 : QUALITÉ
- Chaque lien doit exister et correspondre au titre (WebFetch quand c'est possible). Sinon, écarte l'élément. Date de publication vérifiée, sinon écarte. Langue vérifiée (vidéos en français).
- Pas de doublon avec les 14 derniers jours.

ÉTAPE 5 : ÉCRITURE DANS NOTION
- Vidéos : Titre, Publié le, Chaîne, Lien, Thème (Claude, IA, ou 01 à 08), Abonnement, Pourquoi utile (1 phrase concrète), Action à essayer (15 minutes maximum), Résumé basé sur (« Titre et description » si tu n'as pas la transcription), Statut « À regarder », Semaine = page de la semaine en cours.
- Actualités : Titre, Publié le, Source (indique d'où l'info a été détectée si c'est X ou Reddit, par exemple « Anthropic (repéré sur X) » ou « r/ClaudeAI »), Lien, Type, Thème, Pourquoi utile (1 phrase), Action à essayer si pertinent, Résumé basé sur, Statut « À regarder », Semaine.
- Mets Famille = « idée Claude » sur 1 à 3 éléments grand public sur l'IA ou Claude (simple suggestion). Ne mets jamais « proposé » ni « envoyé » : « proposé » est le choix de l'utilisateur qui déclenche l'envoi.
- Ne touche pas à Important ni aux statuts déjà posés par l'utilisateur.

INTERDITS : publier, envoyer un e-mail, créer un compte, modifier autre chose que ce qui est décrit.
FIN : 6 lignes maximum : nombre ajouté (vidéos / actualités), l'élément le plus important du jour, l'action à essayer en premier, une ligne « Appris de tes retours » (ce que tes Utile/Pas intéressant ont changé dans les choix du jour), et une ligne « Firecrawl » (combien d'appels Reddit et X, crédits estimés dépensés, ou erreur de quota).
```
