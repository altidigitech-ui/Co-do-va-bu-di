# MUTATIONS — SaaS existants transformés en agents IA

Dernière mise à jour : 03/04/2026

## Architecture commune

Chaque SaaS partage le même squelette :

**Stack :** FastAPI + Next.js 14 (PWA) + Supabase + Stripe + Claude API + Celery + Redis

**Agent IA 4 couches :**
1. DÉTECTER — Webhooks, cron jobs, événements temps réel
2. ANALYSER — Claude API interprète, compare, diagnostique en langage humain
3. AGIR — Notification push + email + action recommandée en 1 clic
4. APPRENDRE — Le client accepte ou refuse → l'agent s'améliore

**PWA :** Service worker + manifest.json. Installable Android + iOS. Notifications push. Offline mode.

---

## 1. STOREMD — Le médecin IA permanent de ta boutique (Score 34/41)

**Base :** Leak Detector | **Cible :** E-commerce Shopify | **Mois :** 1

### Le problème (10-120K$/an)
Le merchant ne sait pas que son store est cassé jusqu'à ce que les ventes baissent. Une baisse de 0.1% de conversion sur un store à 100K$/mois = 1200$/mois perdu. Personne ne surveille le store 24/7. Un app update casse le mobile, un theme update ralentit le checkout, une image en 4000px tue le speed score — il le découvre des semaines plus tard.

### Features

| Feature | Ce que l'agent fait |
|---------|-------------------|
| Health Score 24/7 | Score /100 mis à jour chaque nuit. Mobile + Desktop séparés. Le merchant ouvre l'app le matin et voit la santé de son store. |
| Diagnostic 3 couches | Analyse Traffic Quality → Product Engagement → Cart-to-Purchase. Identifie LAQUELLE des 3 couches est cassée. Pas des graphiques — des phrases. |
| Alertes régressives | Détecte quand un score BAISSE vs veille/semaine. Push notification immédiate : "Score mobile tombé à 61 (-14). Cause probable : app X installée hier." |
| App Impact Scanner | Mesure l'impact de CHAQUE app Shopify sur le speed. "14 apps installées, 5 inutilisées depuis 30+ jours. Les retirer = 2.3s de load time en moins." |
| Benchmark concurrence | Scanne 3-5 concurrents. Compare les scores. "Votre score mobile : 61. Vos concurrents : 78, 82, 73." |
| Historique 90 jours | Timeline évolution du score avec événements marqués. Corrélation visuelle avec les changements effectués. |
| Fix Generator | Pour chaque problème → action corrective en langage simple. Pas "Optimize LCP" mais "Désinstallez Popup Manager. +1.8s de vitesse." |
| Weekly Report Push | Rapport lundi matin en push + email. Score, tendance, top 3 actions. Le merchant ne fait rien. |

### L'agent en action
Dimanche 3h → StoreMD scanne → compare avec vendredi → détecte mobile checkout 0.8s plus lent → identifie app update samedi → lundi 8h push : "Your mobile checkout slowed down. Reviews+ updated yesterday. Recommended: update or contact support."

### Pricing
Free (1 audit ponctuel) → 29$/mois (1 store, scan hebdo) → 79$/mois (scan quotidien, benchmark 3 concurrents) → 199$/mois (10 stores, white-label, API)

### Moat
Data accumulation (6 mois d'historique = irremplaçable) + intégration Shopify App Store + complexité technique

---

## 2. LISTINGLAB — Le labo d'optimisation de catalogue (Score 32/41)

**Base :** FicheProduitAI | **Cible :** E-commerce Shopify | **Mois :** 1

### Le problème (5-30K$/an)
200-5000 produits, 8-12 éléments par listing à optimiser. Le merchant ne sait pas lesquels sont faibles ni par où commencer. Les outils existants génèrent à l'aveugle. Personne ne fait : analyse existant → score → diagnostic → réécriture ciblée → benchmark.

### Features

| Feature | Ce que l'agent fait |
|---------|-------------------|
| Catalogue Scan | Scanne TOUS les listings via API Shopify. Score /100 par listing. Vue d'ensemble en 1 écran. |
| Priorisation par impact | Classe par REVENUE potentiel. "Ce listing : 500 vues/mois mais 0.3% conversion. Le fixer = 2000$/mois." |
| Diagnostic par élément | Pour chaque listing faible : quel élément est le problème (titre, description, images, SEO). |
| Rewrite ciblé | Réécrit UNIQUEMENT ce qui est faible. Garde ce qui marche. |
| Benchmark catégorie | Compare chaque listing aux top sellers de la même catégorie (scraping concurrence). |
| Bulk Operations | Réécrire 50-500 listings en 1 clic. Review + approve avant push Shopify. Pas de CSV. |
| SEO Engine | Keywords par produit. Volume, difficulté, suggestions. |
| Multi-langue | Optimisation en 20+ langues (marchés internationaux). |
| New Product Watch | Webhook Shopify : nouveau produit ajouté → analyse auto → alerte si faible → version optimisée proposée en 5 min. |

### Pricing
Free (5 analyses) → 29$/mois (100 produits) → 79$/mois (1000 produits, benchmark, A/B titles) → 199$/mois (illimité, API, white-label)

### Moat
Data catalogue + intégration Shopify bidirectionnelle + SEO engine

---

## 3. LEADQUIZ — Quiz lead gen connecté catalogue (Score 28/41)

**Base :** QuizForge | **Cible :** E-com + Coaches | **Mois :** 3

### Le problème
Typeform (39$/mois) et Interact (89$/mois) ne sont PAS connectés au catalogue Shopify. Le quiz recommande des produits mais le lien est manuel. Analytics basiques.

### Features

| Feature | Ce que l'agent fait |
|---------|-------------------|
| Quiz Generator | 3 phrases de description → quiz complet en 2 min (questions, logique, résultats). |
| Catalogue Connect | API Shopify. Résultats = VRAIS produits avec lien "Ajouter au panier". |
| Email Capture | Capture email AVANT résultats. Intégration Klaviyo, Mailchimp, Brevo. |
| Revenue Attribution | Connecte résultats quiz → achats réels Shopify. ROI du quiz en temps réel. |
| Auto-Optimize | L'agent analyse les drop-offs par question. Suggère des modifications. A/B test auto. |

### Pricing
Free (1 quiz, 50 réponses/mois) → 19$/mois (3 quiz, 500 réponses) → 49$/mois (illimité) → 79$/mois (multi-stores)

---

## CROSS-SELL E-COM

| Si le client utilise | On propose | Pitch |
|---------------------|-----------|-------|
| StoreMD | ListingLab | "Store healthy mais listings faibles" |
| ListingLab | StoreMD | "Listings optimisés mais store a des problèmes" |
| StoreMD + ListingLab | ChargebackShield | "Vous convertissez bien, protégez vos revenus" |
| Tout | ProfitPilot | "Vous vendez — mais quel est votre VRAI profit ?" |

Bundle e-com : StoreMD + ListingLab + ChargebackShield + ProfitPilot = 199$/mois (au lieu de 316$). Le merchant qui a les 4 ne quitte jamais.
