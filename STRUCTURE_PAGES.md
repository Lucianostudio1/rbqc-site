# RBQC — Structure des pages (refonte)

**Usage :** Ce document décrit la nouvelle architecture de contenu de chaque page du site rbqc.ca.
Il est conçu pour être analysé par un agent SEO afin de recommander les mots-clés les plus pertinents
par section, en fonction de l'intention de recherche et de la cible.

**Statut :** Recommandations SEO remplies (sept. 2026). Chaque page a maintenant un bloc **SEO de la page** (mot-clé principal, secondaires, title, meta, H1, slug, schema, maillage) et chaque section a une ligne **Mots-clés à intégrer**. Claude Code peut implémenter directement à partir de ce fichier.

**Service :** Clipping vidéo court-format + distribution automatique sur TikTok, Reels, Facebook, YouTube Shorts
**Marché :** Québec francophone
**Cible :** Humoristes, podcasteurs, coachs/formateurs, créateurs YouTube, entreprises locales québécoises
**Langue :** Français québécois, ton direct, énergie de scène — aucun jargon SaaS générique

---

## 0 — DÉCISIONS À TRANCHER AVANT L'IMPLÉMENTATION

1. **Tarifs.** ✅ TRANCHÉ — 3 formules : 2 $/clip · 0,50 $/1 000 vues · 10 % par billet. CLAUDE.md mis à jour.
2. **Nom de la marque.** ✅ TRANCHÉ — **Rires Bruts Québec** (pas Québécois). CLAUDE.md mis à jour.
3. **Nav "Résultats" vs page "Notre terrain de jeu".** ✅ TRANCHÉ — "Résultats" dans la nav, "Notre terrain de jeu" comme surtitre sur la page.
4. **Slugs.** ✅ TRANCHÉ — Ne pas renommer `services.html` ni `portfolio.html`.

---

## ARGUMENT DE VENTE PRINCIPAL (mise à jour sept. 2026)

**Angle : le volume fait la différence, pas la perfection de chaque clip.**

Le vrai argument de RBQC n'est pas "on va faire exploser tes vidéos". C'est : **on publie en volume, et c'est le volume qui génère les résultats**. Sur 1 715 clips publiés, un pourcentage significatif perce — et c'est cette proportion qui génère des impressions, des abonnés et des ventes de billets.

Cet angle répond à l'objection naturelle : "j'ai vu des vidéos sur vos pages avec peu de vues." La réponse : c'est normal et prévu. Ce n'est pas chaque clip qui explose — c'est l'ensemble du catalogue qui livre la performance cumulée.

**Message clé à intégrer partout :**
- Ce n'est pas 1 clip parfait. C'est 100 clips publiés dont une portion perce.
- 29M d'impressions = résultat de 1 715 clips, pas de 10 clips parfaits.
- Le risque est réduit par le volume : même si 80% des clips font peu de vues, les 20% qui performent couvrent la mise et plus.

**Sections à mettre à jour (prêtes à intégrer dès que l'agent SEO retourne sa proposition) :**
- Homepage — section Stats : reformuler autour du volume (1 715 clips publiés → X% qui performent)
- Homepage — section Services : "le volume fait la différence" comme argument de chaque formule
- Portfolio — section timeline : lier la croissance au volume de publication
- Portfolio — intro de la section 3 brands : "ce n'est pas la chance, c'est le volume"
- Services — processus étape 3 : expliquer que chaque lot de clips = plusieurs chances de percer

**Chiffres disponibles (CSV Metricool, 12 mois) :**
- RBQC : 846 posts, 20,9M impressions, top clip 558K vues
- Québec LOL : 589 posts, 5,75M impressions, top clip 188K vues
- Punch Line QC : 280 posts, 2,3M impressions, top clip 171K vues
- **Total : 1 715 posts, 28,9M impressions**
- 72% de rétention moyenne

---

## STRATÉGIE DE MOTS-CLÉS (vue d'ensemble)

**Constat principal :** le mot "clipping" est un anglicisme très peu cherché au Québec. Les gens tapent plutôt "montage vidéo TikTok", "monteur vidéo", "clips courts", "extraits de podcast", "vidéos courtes". On garde "clipping" comme terme de marque (c'est ce qui différencie RBQC et ça correspond au vocabulaire du milieu), mais on le **jumelle toujours** avec un terme descriptif que les gens cherchent vraiment.

**Paires à utiliser ensemble :**
clipping vidéo + montage de clips courts
clips TikTok + vidéos courtes
extraits de podcast + clips de podcast
distribution + publication sur TikTok, Reels, Facebook et YouTube Shorts

**Cocon sémantique par cible :**

| Cible | Requêtes probables |
|---|---|
| Humoristes | clips spectacle humour, promouvoir son spectacle d'humour, vendre des billets de spectacle, TikTok humoriste québécois |
| Podcasteurs | clips de podcast, montage podcast TikTok, faire connaître son podcast, extraits de podcast pour Reels |
| Coachs/formateurs | recycler ses webinaires, vidéos courtes pour coach, contenu court à partir de formations |
| Créateurs YouTube | YouTube Shorts à partir de vidéos longues, repurposing vidéo |
| Entreprises locales | gestion TikTok entreprise Québec, montage vidéo réseaux sociaux Montréal |

**Termes géo à placer naturellement :** Québec, québécois, francophone, Montréal (1 à 2 fois max par page, pas de bourrage).

**Répartition des intentions :**
Accueil et Services = transactionnel / décision.
Résultats = preuve / commercial investigation.
FAQ = objections, questions longues (excellent pour les réponses IA et "Autres questions posées").
Blogue = informationnel, longue traîne, levier principal de trafic.

**Règle anti-cannibalisation :** un seul mot-clé principal par page. Si deux pages visent la même requête, la plus générale (Accueil) garde le terme court et la plus spécifique prend la variante longue.

---

## SEO GLOBAL (toutes les pages)

- `<html lang="fr-CA">` sur chaque page
- Balise canonical absolue sur chaque page (`https://rbqc.ca/...`)
- Open Graph + Twitter Card sur chaque page (og:title, og:description, og:image 1200x630, og:locale `fr_CA`)
- Schema **Organization** dans le layout global : name "Rires Bruts Québec", alternateName "RBQC", url, logo, email contact@rbqc.ca, sameAs (liens TikTok, Instagram, Facebook, YouTube des 3 brands), areaServed "Québec"
- Un seul H1 par page, contenant le mot-clé principal ou sa variante proche
- Images : attribut `alt` descriptif en français (ex. "Clip TikTok d'un humoriste québécois sur scène"), formats WebP, `loading="lazy"` sauf le hero
- Footer : phrase de positionnement courte avec les mots-clés de marque, ex. "RBQC, service de clipping vidéo et de clips courts pour l'humour et les podcasts au Québec."
- Title : 50 à 60 caractères. Meta description : 140 à 160 caractères, avec un verbe d'action.

---

## PAGE 1 — Accueil (`index.html`)

**Rôle :** Première impression. Accroche, chiffres-clés condensés, 3 formules résumées, preuve humaine (Messenger), CTA.
**Intention visiteur :** "C'est quoi RBQC et est-ce que ça peut m'aider ?"
**Action souhaitée :** Cliquer vers Services ou Contact.

### SEO de la page
- **Mot-clé principal :** clipping vidéo humour et podcast Québec
- **Mots-clés secondaires :** agence de clipping québécoise, clips courts pour humoristes, montage de clips TikTok, clips de podcast, vidéos courtes TikTok Reels YouTube Shorts
- **Title :** `RBQC | Clipping vidéo pour humoristes et podcasts au Québec`
- **Meta description :** `On transforme tes shows, podcasts et lives en clips courts publiés sur TikTok, Reels, Facebook et YouTube Shorts. 29M+ impressions sans pub. Parlons-en.`
- **Slug :** `/` (inchangé)
- **Schema :** Organization (global) + WebSite
- **Maillage sortant :** Services (ancre "comment ça marche"), Résultats (ancre "nos résultats"), Contact, 1 article de blogue en vedette

### Sections

#### 1.1 — Hero
- **H1 proposé :** `Clipping vidéo pour l'humour et les podcasts québécois`
- **Sous-titre proposé :** `Tes shows, podcasts et lives deviennent des clips courts publiés sur TikTok, Reels, Facebook et YouTube Shorts. Toi, tu fais juste envoyer le fichier.`
- CTA primaire : Discuter d'une collab
- CTA secondaire : Comment ça marche →
- Pastilles plateformes : TikTok · Reels · Facebook · YouTube Shorts
- **Mots-clés à intégrer :** clipping vidéo, clips courts, podcasts québécois, humour québécois, TikTok, Reels, YouTube Shorts

#### 1.2 — Chiffres clés (condensé — 3 stats maximum)
- 29M+ impressions (12 mois, 3 pages opérées par RBQC)
- 72% taux de rétention moyen
- 558K vues — clip le plus performant
- **H2 proposé :** `Des clips qui se font voir pour vrai`
- **Mots-clés à intégrer :** impressions, vues, rétention, sans publicité payante
- **Note technique :** chiffres en texte HTML, mention de période visible.

#### 1.3 — Services résumé (3 cartes)
- Clipping à la pièce — 2 $/clip
- Payé à la performance — 0,50 $/1 000 vues
- Commission sur billets — 10 % par billet vendu
- Lien vers services.html pour le détail
- **H2 proposé :** `3 façons de travailler ensemble`
- **Mots-clés à intégrer :** prix par clip, paiement à la performance, commission sur billets de spectacle

#### 1.4 — Preuve humaine (screenshot Messenger)
- Fan qui découvre un clip et demande comment acheter des billets
- **H2 proposé :** `Un clip, un fan, un billet vendu`
- **Mots-clés à intégrer :** vendre des billets de spectacle, promotion de spectacle d'humour, sans budget publicitaire
- **Note technique :** alt de l'image : `Message d'un fan qui demande où acheter des billets après avoir vu un clip RBQC`. Flouter les noms et photos de profil (Loi 25).

#### 1.5 — CTA final
- **H2 proposé :** `T'as du contenu qui dort ? On s'en occupe.`
- **Mots-clés à intégrer :** aucun à forcer, garder le ton

---

## PAGE 2 — Comment ça marche (`services.html`)

**Rôle :** Expliquer le processus de A à Z + détailler les 3 formules. Page de décision.
**Intention visiteur :** "OK je suis intéressé, mais comment ça fonctionne concrètement ?"
**Action souhaitée :** Contacter RBQC pour démarrer.

### SEO de la page
- **Mot-clé principal :** service de montage de clips courts pour podcast et spectacle
- **Mots-clés secondaires :** prix montage vidéo TikTok, montage de clips pour Reels, publication automatique TikTok et YouTube Shorts, sous-titres vidéo courte, tarif clipping vidéo
- **Title :** `Comment ça marche : clipping et distribution vidéo | RBQC`
- **Meta description :** `Tu envoies ton podcast ou ton show, on le découpe en clips courts et on les publie sur 4 plateformes. 3 formules : à la pièce, à la performance ou à la commission.`
- **Slug :** `/services.html` (inchangé)
- **Schema :** Service (serviceType "Montage et distribution de clips vidéo courts", provider RBQC, areaServed Québec) avec 3 `Offer`
- **Maillage sortant :** FAQ (ancre "questions fréquentes"), Résultats, Contact, article blogue "clipping pour comédiens"

### Sections

#### 2.1 — Hero
- **H1 proposé :** `De ton show à 4 plateformes : comment marche le clipping RBQC`
- **Mots-clés à intégrer :** clipping, clips courts, 4 plateformes, podcast, spectacle

#### 2.2 — Processus en 4 étapes (`<ol>` HTML)
- **H2 proposé :** `4 étapes, zéro prise de tête`
- **H3 par étape :** `1. Tu envoies ton fichier` / `2. On sélectionne et on monte les meilleurs moments` / `3. On publie sur TikTok, Reels, Facebook et Shorts` / `4. Tu reçois ton rapport de performance`
- **Mots-clés à intégrer :** montage vidéo court, meilleurs moments, sous-titres, format vertical 9:16, publication automatique, meilleures heures, rapport mensuel, suivi des ventes de billets

#### 2.3 — 3 formules détaillées
- **H2 proposé :** `Choisis ta formule`
- **H3 :** `Clipping à la pièce` / `Payé à la performance` / `Commission sur billets vendus`
- **Mots-clés à intégrer :** prix par clip, combien coûte un monteur vidéo TikTok, payer au nombre de vues, commission sur billets de spectacle, sans frais fixes, sans engagement

#### 2.4 — Comparaison Avant / Après RBQC (`<table>` HTML)
- **H2 proposé :** `Avant RBQC / Avec RBQC`
- **Mots-clés à intégrer :** recycler son contenu, contenu long en contenu court, calendrier de publication, visibilité sur les réseaux sociaux

#### 2.5 — CTA
- `Choisissons ta formule ensemble` · contact@rbqc.ca · Réponse en moins de 24 h

---

## PAGE 3 — Notre terrain de jeu (`portfolio.html`)

**Rôle :** Prouver la crédibilité opérationnelle de RBQC via les 3 brands construites par RBQC.
**Intention visiteur :** "Est-ce que RBQC a déjà prouvé que ça marche, ou c'est juste théorique ?"
**Action souhaitée :** Être convaincu, puis aller vers Contact.
**Angle unique :** RBQC n'a pas attendu d'avoir des clients — on a bâti 3 audiences francophones from scratch.

### SEO de la page
- **Mot-clé principal :** résultats clipping vidéo humour québécois
- **Mots-clés secondaires :** étude de cas TikTok Québec, pages d'humour québécois, croissance Facebook sans publicité, Rires Bruts Québec, Québec LOL, Punch Line QC
- **Title :** `Résultats : 3 audiences humour bâties de zéro | RBQC`
- **Meta description :** `Avant de clipper pour toi, on a bâti nos propres pages d'humour québécois : 29M+ impressions sans pub. Chiffres, clips phares et courbe de croissance.`
- **Slug :** `/portfolio.html` (inchangé)
- **Schema :** CollectionPage + VideoObject par clip phare
- **Maillage sortant :** Services, Contact, article blogue "29M impressions sans pub" (à écrire)

### Sections

#### 3.1 — Hero
- **Surtitre (eyebrow) :** `Notre terrain de jeu`
- **H1 proposé :** `Avant de clipper pour toi, on a bâti nos propres audiences`
- **Sous-titre :** `3 pages d'humour québécois, 29M+ impressions, zéro dollar en pub.`
- **Mots-clés à intégrer :** pages d'humour québécois, audiences, sans publicité

#### 3.2 — Les 3 études de cas
- **H2 de la section :** `3 pages, 3 preuves`
- **Rires Bruts Québec** — H3 : `Rires Bruts Québec : clips de spectacles d'humour` — chiffres propres, clips phares
- **Québec LOL** — H3 : `Québec LOL : podcasts et capsules humoristiques` — chiffres propres, clips phares
- **Punch Line QC** — H3 : `Punch Line QC : de 0 abonné à [chiffre] en [x] mois` — trajectoire depuis juin 2026
- Thumbnails WebP avec alt descriptifs. Liens vers profils sociaux (`rel="noopener"`).

#### 3.3 — Timeline de croissance
- **H2 proposé :** `Combien de temps avant de voir des résultats ?`
- Jalons : mois 1, mois 3, mois 6, mois 12 — en texte HTML + visuel
- Réponse courte (1 phrase) juste sous le H2, avant le graphique
- **Mots-clés à intégrer :** combien de temps pour percer sur TikTok, croissance organique, résultats en semaines

#### 3.4 — Contexte de marché : Québec vs États-Unis
- **H2 proposé :** `Le clipping a bâti l'humour américain. Au Québec, c'est maintenant.`
- USA : marché saturé (Schulz, Theo Von, Ryan Long)
- Québec : "À notre connaissance, aucune agence spécialisée humour francophone avant RBQC"
- **Mots-clés à intégrer :** agence de clipping, première agence de clipping humour au Québec

#### 3.5 — CTA
- `Ton contenu est la prochaine étude de cas`

---

## PAGE 4 — FAQ (`faq.html`)

**Statut :** Page excellente — reformuler les questions, ajouter les manquantes, ajouter schema FAQPage.

### SEO de la page
- **Title :** `FAQ clipping vidéo : prix, droits, délais | RBQC`
- **Meta description :** `Combien de clips par épisode, qui garde les droits, délais de livraison, suivi des billets vendus : toutes les réponses avant de te lancer avec RBQC.`
- **Schema :** FAQPage

### Questions (format "telles que les gens les tapent")
**Existantes à reformuler :**
- `Combien de clips on peut sortir d'un épisode de podcast ou d'un spectacle ?`
- `Est-ce que je garde les droits sur mes clips ?`
- `Combien de temps ça prend avant de recevoir mes clips ?`
- `Comment vous suivez les billets vendus grâce aux clips ?`
- `Est-ce que je peux tester avec un seul épisode ?`

**À ajouter :**
- `Combien coûte le clipping vidéo ?`
- `Est-ce que vous ajoutez des sous-titres ?`
- `Est-ce que je dois publier moi-même ?`
- `Vous travaillez avec qui à part les humoristes ?`
- `Sur quelles plateformes mes clips sont publiés ?`
- `Quel type de contenu je peux vous envoyer ?`

**Règle de rédaction :** première phrase = réponse directe (oui/non ou chiffre), détail ensuite.

---

## PAGE 5 — Blogue (`blog/index.html`)

### SEO index
- **Title :** `Blogue : clipping, TikTok et humour québécois | RBQC`
- **Meta description :** `Conseils concrets pour humoristes, podcasteurs et créateurs québécois : clips courts, TikTok, Reels, vente de billets. Écrit par l'équipe qui opère 3 pages d'humour.`
- **Schema :** Blog sur l'index, BlogPosting sur chaque article

### Plan éditorial (ordre de priorité)

| # | Slug | Mot-clé principal | Intention |
|---|---|---|---|
| 1 | `vendre-billets-spectacle-reseaux-sociaux.html` | vendre des billets de spectacle avec les réseaux sociaux | Info + commerciale |
| 2 | `clips-podcast-quebecois.html` | faire des clips de podcast pour TikTok et Reels | Info |
| 3 | `29-millions-impressions-sans-pub.html` | croissance TikTok et Facebook sans publicité | Info / preuve |
| 4 | `clips-courts-vs-contenu-long-humoriste.html` | contenu court ou long pour un humoriste | Info |
| 5 | `publication-automatique-tiktok-reels-shorts.html` | publier automatiquement sur TikTok, Reels et YouTube Shorts | Info |
| 6 | `combien-coute-monteur-video-tiktok.html` | combien coûte un monteur vidéo TikTok au Québec | Commerciale |
| 7 | `recycler-webinaire-en-clips-courts.html` | transformer un webinaire en vidéos courtes | Info |
| 8 | `youtube-shorts-a-partir-video-longue.html` | créer des YouTube Shorts à partir d'une vidéo longue | Info |

---

## PAGE 6 — Contact (`contact.html`)

### SEO de la page
- **Title :** `Contact | Parlons de ton projet de clips | RBQC`
- **Meta description :** `Podcast, spectacle, live ou capsule ? Écris-nous à contact@rbqc.ca ou remplis le formulaire. Réponse en moins de 24 h, sans engagement.`
- **Schema :** ContactPage + ContactPoint
- **H1 proposé :** `Parlons de ton projet`
- **Note Loi 25 :** ligne sous le bouton d'envoi, lien vers politique de confidentialité, pas de case précochée.

---

## PAGES SECONDAIRES

### À propos (`about.html`)
- **Title :** `À propos | L'équipe derrière RBQC`
- **Meta description :** `RBQC est né d'une page d'humour québécois. On a appris à faire percer des clips pour nous-mêmes avant de le faire pour les créateurs d'ici.`
- **H1 proposé :** `Qui est derrière RBQC`
- **Schema :** AboutPage + Person (E-E-A-T : nom, rôle, photo)

### Politique de confidentialité
- **Slug :** `/politique-confidentialite.html`
- **Title :** `Politique de confidentialité | RBQC`
- Loi 25 : données collectées, durée, hébergement (Netlify, Google Workspace), droits d'accès/suppression
- Recommandation analytics : Plausible (évite bannière de témoins vs GA4)
- `noindex` via meta robots

### 404 personnalisée (`404.html`)
- **H1 :** `Ce punch-là est tombé à plat.`
- Texte : `La page que tu cherches existe pas (ou plus). Retourne à l'accueil ou écris-nous si t'es perdu.`
- `noindex`, exclure du sitemap

---

## NAVIGATION GLOBALE

**Desktop (4 items + CTA) :**
Services → Résultats → Blogue → Contact | [Travailler avec nous]

**Mobile + Footer (liste complète) :**
Services · Résultats · Blogue · FAQ · À propos · Contact · Politique de confidentialité

**Footer :** ajouter liens vers les 4 profils sociaux RBQC + phrase : "RBQC, service de clipping vidéo et de clips courts pour l'humour et les podcasts au Québec."

**Fil d'Ariane (blogue) :** Accueil > Blogue > Titre, avec schema BreadcrumbList.

---

## TECHNIQUE (après refonte)

- Sitemap : inclure toutes les pages sauf 404 et politique. `lastmod` à jour.
- `robots.txt` avec `Sitemap: https://rbqc.ca/sitemap.xml`
- Google Search Console : soumettre sitemap, demander indexation manuelle Accueil + Services + Résultats
- Plausible Analytics recommandé (pas GA4 — évite bannière de témoins Loi 25)
