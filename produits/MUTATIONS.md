# FLÈCHE 1 (V2) — SaaS EXISTANTS → Mutations profondes

**Date :** 03 avril 2026
**Lens :** Pas de limite de build. La complexité = le moat. Claude Code build tout.

---

## PRINCIPE

On ne "pivote" plus Leak Detector avec un nouveau titre et 3 prompts modifiés. On le MUTE en quelque chose de fondamentalement plus puissant en exploitant le core engine (Playwright + Claude API + scoring) comme base d'un produit qui résout un problème à 10K$/an, pas à 29$/mois.

---

## 1. LEAK DETECTOR → STOREMD : Le médecin IA permanent de ta boutique

### Le problème réel (pas le symptôme)

La conversion est le problème le plus coûteux. 1000 visiteurs à 0.5% de conversion = 5 ventes. À 2.5% = 25 ventes. C'est 20 ventes perdues pour 1000 visiteurs. À 50$ de panier moyen, un store de 10K visiteurs/mois perd 10 000$ par mois.

Les outils CRO existants (Hotjar, Lucky Orange, Google Optimize RIP) montrent des heatmaps et des recordings. Le merchant VOIT le problème mais ne sait pas QUOI FAIRE. Et c'est un audit ponctuel — il le fait une fois, corrige 2 trucs, et ne revient jamais.

### Ce que StoreMD fait (bien au-delà de Leak Detector)

**Leak Detector = un diagnostic ponctuel.** StoreMD = un médecin IA permanent qui surveille ta boutique 24/7.

| Feature | Leak Detector (actuel) | StoreMD (mutation) |
|---------|----------------------|-------------------|
| Audit ponctuel | ✅ Score /100 sur 8 catégories | ✅ Inclus comme "premier check-up" |
| Monitoring continu | ❌ | ✅ Re-scan automatique hebdomadaire, alertes si un score baisse |
| Diagnostic spécifique Shopify | ❌ Generic landing page | ✅ Analyse product pages, collection pages, checkout flow, cart page |
| Benchmark concurrence | ❌ | ✅ Scanne 3-5 concurrents et compare les scores |
| Recommandations actionnables non-tech | ❌ Jargon CRO | ✅ "Déplace ton bouton Ajouter au panier au-dessus de la ligne de flottaison" avec screenshot annoté |
| A/B test suggestions | ❌ | ✅ L'IA suggère quoi tester en priorité basé sur l'impact estimé |
| Historique et trends | ❌ | ✅ Dashboard avec évolution du score dans le temps |
| Score par device | ❌ | ✅ Score séparé mobile vs desktop (70%+ du trafic e-com = mobile) |
| Speed monitoring | Basique | ✅ Core Web Vitals tracking + alertes si ça se dégrade |
| Intégration Shopify | ❌ | ✅ App Shopify native (V2) — install en 1 clic, accès aux données boutique |

### Stack technique

- **Core existant** : Playwright (scraping), Claude API (analyse), scoring engine
- **À ajouter** : Celery + Redis (jobs récurrents de monitoring), Supabase (historique scores), webhook alertes (email/Slack), API Shopify (V2 pour install native)
- **Complexité** : HAUTE — et c'est le point. Un vibe coder ne peut pas reproduire un monitoring CRO continu avec benchmark concurrence en une après-midi.

### Pricing

| Plan | Prix | Ce qu'il inclut |
|------|------|----------------|
| Free | 0$ | 1 audit ponctuel, 1 page, résultats limités |
| Starter | 29$/mois | 1 store, scan hebdo, 5 pages, historique 30 jours |
| Pro | 79$/mois | 1 store, scan quotidien, pages illimitées, benchmark 3 concurrents, alertes |
| Agency | 199$/mois | 10 stores, tout inclus, white-label rapports, API access |

### Revenue potentiel

Un store qui perd 10K$/mois en conversions ratées paie 79$/mois les yeux fermés. 500 stores Pro = 39K$ MRR. Le pricing est justifié par le ROI client.

### Moat

- **Data accumulation** : plus de scans = meilleur benchmark sectoriel. Personne ne part une fois qu'il a 6 mois d'historique.
- **Complexité technique** : monitoring continu + benchmark + historique + alertes = pas reproduisable en un weekend.
- **Intégration Shopify App Store** : une fois dans le store, c'est un canal de distribution permanent avec 4.6M+ boutiques.

---

## 2. FICHEPRODUITAI → LISTINGLAB : Le labo d'optimisation de listings IA

### Le problème réel

Ce n'est pas juste "mes descriptions sont mauvaises". C'est un problème systémique : le merchant a 200-5000 produits, chaque listing a 8-12 éléments à optimiser (titre, description, images alt-text, meta title, meta description, tags, variant names, collection assignments), et il ne sait pas LESQUELS de ses listings sont les plus faibles ni PAR OÙ commencer.

### Ce que ListingLab fait (au-delà de la simple génération)

| Feature | Apps existantes (GoWise, SEO On) | ListingLab |
|---------|--------------------------------|-----------|
| Génération description IA | ✅ | ✅ Inclus |
| Analyse catalogue complet | ❌ Product par product | ✅ Scan de TOUT le catalogue d'un coup — identifie les 20% de listings les plus faibles |
| Score par listing | ❌ | ✅ Score /100 : titre, description, SEO, images, trust signals, competitor comparison |
| Priorisation | ❌ | ✅ "Ces 15 listings vous font perdre le plus de ventes — commencez par eux" |
| Réécriture ciblée | ❌ Réécriture aveugle | ✅ Réécriture SEULEMENT de ce qui est faible, garde ce qui marche |
| Benchmark concurrence | ❌ | ✅ Compare chaque listing avec les top sellers de la même catégorie |
| SEO complet | Basique (meta tags) | ✅ Keywords research, search volume, difficulty — spécifique à la niche du produit |
| Multi-langue | Certains | ✅ Génération/optimisation en 20+ langues (marchés internationaux) |
| Bulk operations | Certains | ✅ Réécriture batch de 500 listings en 1 clic |
| A/B testing titres | ❌ | ✅ Génère 3 variantes de titre avec prédiction de CTR |
| Connexion Shopify native | Variable | ✅ Pull et push direct dans Shopify — pas de CSV |
| Suivi dans le temps | ❌ | ✅ Le score évolue — on voit l'impact des changements |

### Stack

- FastAPI + Next.js + Supabase + Claude API
- API Shopify (pull produits, push modifications)
- Scraping concurrence (Playwright)
- Keyword research API (Datamuse, Google Trends API, ou custom)

### Pricing

| Plan | Prix | Produits |
|------|------|---------|
| Free | 0$ | 5 analyses, pas de réécriture |
| Starter | 29$/mois | 100 produits, réécriture, SEO basique |
| Pro | 79$/mois | 1000 produits, benchmark, A/B titles, multi-langue |
| Enterprise | 199$/mois | Illimité, API, white-label |

---

## 3. QUIZFORGE → LEADQUIZ : Quiz de lead generation pour e-commerce et coaches

### Le pivot

QuizForge tel que planifié (SCORM export, formation) = niche étroite, willingness-to-pay faible.

**LeadQuiz** = quiz interactifs comme outil de LEAD GENERATION pour les e-commerçants et les coaches. "Trouvez votre type de peau" → résultat personnalisé → recommandation produit → capture email → vente.

| Feature | Typeform/Interact | LeadQuiz |
|---------|------------------|----------|
| Création quiz | ✅ | ✅ + IA génère le quiz à partir de la description du catalogue |
| Design | Bon | ✅ Templates e-commerce et coaching prêts à l'emploi |
| Recommandation produit | Limité | ✅ Connecté au catalogue Shopify — recommande les VRAIS produits |
| Capture email | ✅ | ✅ + intégration Klaviyo, Mailchimp, Brevo |
| Analytics | Basique | ✅ Conversion par question, drop-off analysis, revenue attribué |
| IA | ❌ | ✅ L'IA analyse les résultats et optimise le quiz automatiquement |
| Prix | 39-249$/mois | 19-79$/mois (undercut) |

### Revenue : 2-5K$ MRR à M6. Niche mais forte rétention.

---

## SYNTHÈSE V2 — Mutations profondes

| Produit original | Mutation | Complexité | Moat | Revenue M6 |
|-----------------|----------|-----------|------|-----------|
| Leak Detector | **StoreMD** — Médecin CRO permanent | HAUTE (monitoring continu, benchmark, alertes) | Data accumulation + App Store Shopify | 5-15K$ MRR |
| FicheProduitAI | **ListingLab** — Labo d'optimisation catalogue | HAUTE (scan catalogue complet, benchmark, bulk) | Data + intégration Shopify + SEO engine | 5-15K$ MRR |
| QuizForge | **LeadQuiz** — Quiz lead gen e-com/coaches | MOYENNE | Templates + intégration catalogue | 2-5K$ MRR |
| PayloadDiff | ❌ KILL | — | — | — |
| DevToolsAPI | ❌ KILL | — | — | — |
