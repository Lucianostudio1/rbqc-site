# RBQC — Brief SEO pour Agent
> À utiliser tel quel comme contexte d'entrée pour l'agent SEO.
> Domaine : rbqc.ca · Langue : français québécois · Hébergement : Netlify (HTML statique)
> Date : 2026-09-18

---

## 1. Contexte du projet

**Qui** : RBQC (Rires Bruts Québec) — agence de clipping vidéo spécialisée humour et podcasts québécois francophones.

**Quoi** : Transformer des shows, spectacles et podcasts en clips courts distribués sur TikTok, Reels, Facebook et YouTube Shorts.

**Trois formules** :
- Clipping à la pièce : 2$/clip
- Pay-for-performance : 0,50$/1 000 vues
- Commission sur billets : 10%

**Chiffres prouvables** : 29M impressions · 398K interactions · 72% rétention · 1 715 clips · 12 mois · 3 marques (RBQC, Québec LOL, Punch Line QC)

**Cible** : Humoristes stand-up, podcasteurs, créateurs de contenu québécois francophones.

**Ton** : Tutoiement québécois naturel. Direct, chiffré, pas de jargon marketing générique.

---

## 2. Architecture technique

```
rbqc.ca/                          → index.html
rbqc.ca/services.html             → Formules + process
rbqc.ca/portfolio.html            → Résultats chiffrés
rbqc.ca/faq.html                  → 16 questions / 5 catégories
rbqc.ca/about.html                → À propos
rbqc.ca/contact.html              → Formulaire + infos
rbqc.ca/blog/                     → Index blogue
rbqc.ca/blog/clipping-pour-comediens-quebec.html → Article pilier
```

**CSS** : `css/style.css` (global) + `css/pages/[page].css` (par page)
**Breakpoints** : 768px (tablette/mobile) + 480px (petits téléphones)
**Sitemap** : `/sitemap.xml` ✅ · **Robots** : `/robots.txt` ✅

---

## 3. État SEO page par page

### index.html — Accueil
| Champ | Valeur actuelle | Longueur | Statut |
|-------|----------------|----------|--------|
| `<title>` | RBQC — Clipping Vidéo pour Humour et Podcasts Québécois | 57c | ✅ |
| `<meta description>` | RBQC transforme tes podcasts et shows d'humour en clips viraux sur TikTok, Reels et Shorts. 29M impressions, 72% de rétention. Distribution sans risque. | 152c | ✅ |
| `<h1>` | Le rire québécois mérite d'être vu partout. | ~43c | ⚠ Pas de mot-clé principal |
| `og:title` | RBQC — Clips Viraux pour Humoristes et Podcasts Québécois | 57c | ✅ |
| `canonical` | https://rbqc.ca/ | — | ✅ |
| Schema | ProfessionalService · areaServed Canada | — | ✅ |

**H2s** : Pas de H1 avec mot-clé → aucun H2 visible dans le HTML (sections sans balises H2 explicites)

**Gap** : H1 purement brand/émotionnel, zéro mot-clé SEO. Pas de H2 structurés visibles.

---

### services.html
| Champ | Valeur actuelle | Longueur | Statut |
|-------|----------------|----------|--------|
| `<title>` | Services de Clipping Vidéo pour Humoristes Québécois | 52c | ✅ |
| `<meta description>` | Clipping à 2$/clip, pay-for-performance à 0,50$/1 000 vues, ou commission 10% sur billets. Distribution TikTok, Reels, Facebook et Shorts. Sans risque. | 152c | ✅ |
| `<h1>` | Clipping pour humoristes et podcasts québécois. | ~47c | ✅ |
| Schema | Service · 3 Offers avec prix CAD | — | ✅ |

**H2s** :
1. Trois formules de clipping, sans risque.
2. De ton show à 4 plateformes, en 4 étapes.
3. Sans RBQC vs avec RBQC : la différence.
4. Tes questions sur le clipping, répondues.
5. Choisissons ta formule.

**Gap** : H2 #3 et #5 peu optimisés pour la recherche. "Sans RBQC" pourrait être reformulé.

---

### portfolio.html
| Champ | Valeur actuelle | Longueur | Statut |
|-------|----------------|----------|--------|
| `<title>` | Résultats — Clips Humour Québécois qui Performent Vraiment | 58c | ✅ |
| `<meta description>` | 29M impressions, 398K interactions, 72% de rétention. Résultats réels du clipping pour humoristes et podcasteurs québécois sur 12 mois. | 136c | ✅ |
| `<h1>` | Nos clips d'humour vendent des billets. La preuve en chiffres. | ~59c | ⚠ `hero-label`, pas `hero-title` — vérifier balisage H1 |
| Schema | AboutPage (à changer en CollectionPage ou ProfessionalService) | — | ⚠ |

**H2s** :
1. 29M impressions, 12 mois, 3 marques québécoises.
2. Facebook, TikTok, Reels, Shorts : le portrait complet.
3. Combien de vues, combien de billets.
4. Les clips qui ont explosé.
5. Quand un clip devient un billet vendu.
6. Parlons de ton projet.

**Gap** : Schema `AboutPage` incorrect pour une page de résultats. H2 #6 = CTA, pas SEO.

---

### faq.html
| Champ | Valeur actuelle | Longueur | Statut |
|-------|----------------|----------|--------|
| `<title>` | FAQ — Toutes vos Questions sur le Clipping Vidéo \| RBQC | 55c | ✅ |
| `<meta description>` | Toutes vos questions sur le clipping vidéo pour humoristes et podcasteurs québécois. Formules, prix, droits, distribution, délais — réponses complètes. | 148c | ✅ |
| `<h1>` | Tes questions sur le clipping, répondues. | ~41c | ⚠ Mot-clé principal dilué |
| Schema | FAQPage · 5 questions | — | ✅ mais seulement 5 des 16 questions dans le JSON-LD |

**H2s (catégories)** :
1. Comprendre le clipping
2. Les formules et les prix
3. La distribution
4. Droits et propriété
5. Démarrer avec RBQC

**Gap** : H1 faible. Schema FAQPage incomplet (5/16 questions). H2 catégories ne contiennent pas les mots-clés de longue traîne.

---

### about.html
| Champ | Valeur actuelle | Longueur | Statut |
|-------|----------------|----------|--------|
| `<title>` | À Propos — L'Agence Clipping de l'Humour Québécois | 51c | ✅ |
| `<meta description>` | RBQC est la seule agence de clipping dédiée à l'humour, au stand-up et aux podcasts québécois. Découvre notre approche et nos résultats sur 12 mois. | 148c | ✅ |
| `<h1>` | La seule agence de clipping faite pour l'humour québécois. | ~57c | ✅ |
| Schema | AboutPage · Organization | — | ✅ |

**H2s** :
1. Pourquoi RBQC existe.
2. 3 marques, 29M impressions, une seule mission.
3. Pipeline automatisé, œil humain sur chaque clip.
4. L'humour québécois mérite sa propre agence.

**Gap** : H2s peu orientés mots-clés de recherche (plus branding que SEO).

---

### contact.html
| Champ | Valeur actuelle | Longueur | Statut |
|-------|----------------|----------|--------|
| `<title>` | Contact — Démarre ton Clipping Vidéo Humour avec RBQC | 54c | ✅ |
| `<meta description>` | Prêt à transformer ton contenu en clips viraux ? Contacte RBQC pour discuter de ta formule de clipping. Réponse en 24h. Humoristes et podcasteurs québécois. | 152c | ✅ |
| `<h1>` | Ton show mérite d'être clippé comme du monde. | ~46c | ⚠ Pas de mot-clé |
| Schema | ContactPage · Organization | — | ✅ |

**Gap** : H1 émotionnel sans mot-clé. Page contact rarement la cible SEO principale, acceptable.

---

### blog/index.html
| Champ | Valeur actuelle | Longueur | Statut |
|-------|----------------|----------|--------|
| `<title>` | Blogue RBQC — Ressources pour Humoristes et Podcasteurs Québécois | 65c | ⚠ 65c (trop long, idéal 50-60c) |
| `<meta description>` | Conseils, guides et ressources sur le clipping vidéo, la distribution sur les réseaux sociaux et la croissance d'audience pour artistes québécois. | 145c | ✅ |
| `<h1>` | Ressources pour artistes québécois. | ~35c | ⚠ Trop générique |
| Schema | Blog · Organization | — | ✅ |

**H2s** :
1. Les dernières publications.
2. Nouveaux articles chaque mois.

**Gap** : Title trop long. H1 et H2 peu optimisés. 1 seul article publié.

---

### blog/clipping-pour-comediens-quebec.html
| Champ | Valeur actuelle | Longueur | Statut |
|-------|----------------|----------|--------|
| `<title>` | Clipping Vidéo pour Comédiens Québécois : le Guide Complet | 58c | ✅ |
| `<meta description>` | Tout savoir sur le clipping vidéo pour humoristes et podcasteurs québécois : comment ça marche, combien ça coûte, et comment monétiser tes clips. | 144c | ✅ |
| `<h1>` | Le guide complet du clipping vidéo pour comédiens québécois. | ~58c | ✅ |
| Schema | BlogPosting · Organization | — | ✅ |

**H2s** :
1. C'est quoi le clipping vidéo, concrètement ?
2. Pourquoi c'est le bon moment pour les humoristes québécois.
3. TikTok, Reels, Facebook et Shorts : comment chaque plateforme travaille pour toi.
4. Combien de vues, combien de billets : les vrais chiffres.
5. Comment monétiser tes clips et démarrer avec RBQC.

**Statut** : Page la mieux optimisée du site. H2s riches en mots-clés longue traîne. ✅

---

## 4. Mots-clés déjà utilisés (ne pas sur-optimiser)

```
clipping vidéo québec
clips humour québécois
agence clipping podcast québécois
formule pay-for-performance clipping
service clipping pour humoristes
résultats clipping vidéo
clips humour viraux québec
distribution TikTok Reels Shorts humoristes
clipping vidéo comédiens québécois
```

---

## 5. Gaps prioritaires pour l'agent SEO

### 🔴 Priorité haute

1. **index.html H1** — purement émotionnel, zéro mot-clé. Option : injecter "clipping vidéo" dans le H1 tout en gardant le ton.

2. **faq.html Schema FAQPage incomplet** — seulement 5 questions sur 16 dans le JSON-LD. Ajouter les 11 manquantes pour maximiser les rich snippets Google.

3. **portfolio.html Schema** — `AboutPage` incorrect. Utiliser `ProfessionalService` ou `WebPage` avec `about`.

4. **blog/index.html title** — 65 caractères, trop long. Réduire à 50-60c.

### 🟡 Priorité moyenne

5. **H2s des sections SEO** — about.html et index.html ont des H2s branding sans mots-clés de recherche. Reformuler pour capturer des requêtes longue traîne.

6. **faq.html H1** — "Tes questions sur le clipping, répondues" → devrait contenir "clipping vidéo québec" ou similaire.

7. **blog/index.html H1** — "Ressources pour artistes québécois" → trop générique, pas de mot-clé core.

8. **Image alt texts** — Pas d'images sur le site (clips en iframe ou absents). À surveiller si des images sont ajoutées.

9. **Mots-clés gap à cibler** (non encore utilisés significativement) :
   - `montage clips courts québec`
   - `distribution réseaux sociaux humoristes`
   - `viral clips stand-up québécois`
   - `agence social media humour québec`
   - `comment vendre billets spectacle réseaux sociaux`
   - `clipping podcast québec francophone`

### 🟢 Priorité basse / future

10. **Deuxième article de blogue** — 1 seul article indexé est insuffisant pour la topical authority.
11. **Liens internes** — Ajouter des liens contextuels entre l'article pilier → services → portfolio.
12. **og:image** — Référence à `rbqc.ca/og-image.png` qui n'existe peut-être pas. À créer.

---

## 6. Structure mobile vs desktop — impact SEO

### Ce qui est identique (bon signe pour Google)
- Tous les titres, meta, canonical, schema sont dans le `<head>` — pas affectés par le responsive
- H1, H2, H3 présents sur mobile et desktop (pas masqués par `display:none`)
- Le contenu FAQ est accordéon JS — **potentiel problème** : Google indexe le contenu caché dans les accordéons, mais c'est moins fiable. Envisager `hidden` CSS pur plutôt que JS si problème d'indexation constaté.

### Différences mobile
- Nav desktop : 4 liens (Services, Résultats, Blogue, Contact) — pas de FAQ ni About dans la nav principale. Google peut interpréter la profondeur de lien.
- Footer nav : masqué en dessous de 480px (`display: none`) — les liens footer ne sont pas cliquables sur très petits phones, mais restent dans le DOM donc indexables.
- `section { padding: 64px 20px }` à 480px — le contenu reste entier, rien de masqué.

### Recommandation mobile SEO
- S'assurer que les textes des accordéons FAQ sont bien dans le DOM (pas injectés en JS après coup) ✅ — c'est déjà le cas.
- Vérifier via Google Search Console l'indexation mobile après déploiement.

---

## 7. Infos techniques pour l'agent

```
Plateforme        : Netlify (déploiement Git)
CMS               : Aucun — HTML statique pur
CSS               : css/style.css (global) + css/pages/[page].css (par page)
JS                : Inline dans chaque HTML, bas de page
Fonts             : Google Fonts (Big Shoulders Display 700/900 + Work Sans 400/500/600)
Sitemap           : https://rbqc.ca/sitemap.xml (8 URLs, à jour)
Robots            : Allow: * · Sitemap déclaré
Schema présents   : ProfessionalService, Service (3 Offers), AboutPage, FAQPage,
                    ContactPage, Blog, BlogPosting
Canonical         : Présent sur toutes les pages ✅
OG tags           : Présents sur toutes les pages ✅
Twitter card      : summary_large_image sur toutes les pages ✅
```

---

## 8. Instructions pour l'agent SEO

1. **Ne pas toucher** : Les mots-clés déjà utilisés (section 4) — le site est cohérent là-dessus.
2. **Ton** : Français québécois, tutoiement. Jamais de traduction mot-à-mot du français standard.
3. **Preuve chiffrée** : Réutiliser 29M impressions, 398K interactions, 72% rétention, 1 715 clips dans les meta/H2 quand pertinent.
4. **Mobile-first** : Tout changement de contenu doit être identique mobile/desktop (pas de `display:none` sur contenu SEO).
5. **Fichiers à modifier** : Les meta/title/H1/H2 sont dans les fichiers `.html` directement. Les schémas JSON-LD sont dans les `<head>` de chaque page.
6. **Format de retour souhaité** : Liste de changements par fichier avec la valeur actuelle → valeur proposée, prête à implémenter.
