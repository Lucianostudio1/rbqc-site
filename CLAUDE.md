# RBQC — Contexte du projet

## C'est quoi
RBQC (Rires Bruts Québécois) est un service québécois de clipping et distribution vidéo courte. On transforme les podcasts, capsules, lives et shows de créateurs en clips courts publiés sur TikTok, Instagram Reels, Facebook et YouTube Shorts.

## Marque
- Nom : RBQC
- Domaine : rbqc.ca
- Courriel de contact : contact@rbqc.ca
- Langue : français québécois, informel, direct
- Ton : énergie de scène/comédie, pas du SaaS générique corporatif

## Direction visuelle
- Fond papier chaud (#f4efe4 / #ece4d3), encre quasi noire (#16171c)
- Accents : rouge punch (#e0402a) et jaune moutarde/spotlight (#f2b705)
- Typo titres : Big Shoulders Display (condensée, bold, majuscules)
- Typo texte : Work Sans
- Éviter le look AI générique (fond crème + terracotta, cartes SaaS identiques, gradients)

## Cible
Humoristes et talents émergents (ex. cohortes École nationale de l'humour), podcasteurs francophones, créateurs YouTube québécois.

## Tarifs (3 formules actives)
- Clipping à la pièce : 2 $/clip — montage court-format livré en 48-72 h, idéal pour tester
- Payé à la performance : 0,50 $/1 000 vues générées — clipping + distribution inclus, tu paies que ce qui performe
- Commission sur billets : 10 % par billet vendu via lien ou code promo tracké RBQC — zéro déboursé

## Structure du site (8 pages)
Accueil, Services, Tarifs, Blogue (avec au moins un article publié : clipping-pour-comediens-quebec.html), FAQ, À propos/Contact, plus 2 autres pages. Nav desktop uniforme : 4 items primaires + CTA. Nav mobile et footer incluent Blogue et FAQ.

## État technique actuel
- Hébergé sur Netlify, domaine rbqc.ca connecté via nameservers Netlify (plus chez OVH)
- Google Workspace configuré : Gmail actif sur contact@rbqc.ca, SPF et DKIM authentifiés
- Sitemap étendu aux 8 URLs

## Reste à faire
- Favicon
- Image Open Graph (1200x630px) pour les partages sur réseaux sociaux
- Page 404 personnalisée
- Vérifier que le formulaire de contact envoie bien à contact@rbqc.ca
- Politique de confidentialité (Loi 25, si le formulaire collecte des infos personnelles)
- Google Search Console + Analytics/Plausible
- Remplacer les chiffres placeholder (nombre de clips, vues cumulées) par les vraies stats Facebook avant l'outreach

## Nom officiel de la marque principale
**Rires Bruts Québec** (pas "Québécois") — cohérent avec le sigle RBQC. À utiliser partout : schema, footer, À propos, portfolio.

## Ce qui existe déjà (assets)
- 3 comptes Facebook performants utilisés comme preuve sociale
- Kit Média HTML (version niche humour + version généraliste)
- Liste de prospects (RBQC_Prospects, Google Sheets)
- 3 templates de courriel d'outreach + séquence de relance J0/J3/J7

## Instructions pour Claude
- Toujours utiliser le skill `ui-ux-pro-max` pour tout travail visuel, design, ou modification de l'interface
- Respecter strictement la direction visuelle ci-dessus — aucun drift vers un look SaaS générique
- Langue de travail : français québécois
