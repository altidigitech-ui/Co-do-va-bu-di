# MUTATIONS — SaaS existants transformés en agents IA

Dernière mise à jour : 04/04/2026
Source : 50+ threads Reddit (5000+ commentaires) + recherche web

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
**Validation terrain :** 8+ threads, 500+ commentaires (bots, vitesse, apps destructrices, conversion, fraude, vol de store)

### Le problème (10-120K$/an)
Le merchant ne sait pas que son store est cassé jusqu'à ce que les ventes baissent. Un merchant avait 100K visiteurs/jour (au lieu de 600-1000) à cause des bots — analytics complètement faussées. Un autre a vu ses ventes tomber à ZÉRO après une bannière cookies mal configurée — taux de rebond de 75% à 96%. Une app email (Orderly Emails) a SUPPRIMÉ les collections de dizaines de stores du jour au lendemain — un merchant a perdu 8 ans de SEO. Un merchant s'est fait copier 2000+ produits par un site au Pakistan.

### Features

| Feature | Ce que l'agent fait | Validation terrain |
|---------|-------------------|--------------------|
| Health Score 24/7 | Score /100 mis à jour chaque nuit. Mobile + Desktop séparés. | Thread ventes à zéro (20 upvotes) : le merchant ne savait pas pourquoi ses ventes avaient chuté |
| Diagnostic 3 couches | Analyse Traffic Quality → Product Engagement → Cart-to-Purchase. Identifie LAQUELLE est cassée. | Thread conversion (10 upvotes) : "CPC 0.20$ = trafic de supermarché, pas des acheteurs" |
| Alertes régressives | Détecte quand un score BAISSE vs veille/semaine. Push notification immédiate. | Thread ventes à zéro : taux de rebond passé de 75% à 96% sans que le merchant comprenne |
| App Impact Scanner | Mesure l'impact de CHAQUE app Shopify sur le speed et le score. | Thread vitesse (102 upvotes) : "90% des apps peuvent être supprimées" — "une section chargeait TOUT le catalogue d'images pour en afficher 4" |
| Bot Traffic Filter | Sépare trafic humain vs bots dans les métriques. Montre le "vrai" taux de conversion. | Thread bots (29 upvotes) : 3 MILLIONS de hits en 30 jours sur 2 pages. "Taux de conversion faussés, entonnoirs bruyants" |
| App Risk Monitor | Surveille les actions des apps installées. Alerte si une app fait des changements massifs. | Thread Orderly Emails (25 upvotes) : app a SUPPRIMÉ les collections de dizaines de stores. "Shopify a vraiment besoin d'un backup intégré" |
| Collection Backup auto | Snapshot quotidien des collections, menus, theme settings. Restauration 1 clic. | Thread Orderly Emails : "j'ai dû recréer chaque collection, y compris des textes en différentes langues dont certains avaient 9 ans" |
| Content Theft Scanner | Vérifie périodiquement si tes images/descriptions apparaissent sur d'autres sites. | Thread vol (26 upvotes) : "2000+ produits dupliqués avec les mêmes images. Mon entreprise de 7 ans s'effondre" |
| Security Monitor | Alerte connexions anormales, changements critiques au store. | Thread fraude 25K$ (124 upvotes) : hack via vol de cookies, ligne de crédit frauduleuse ouverte. "Enquête 90 jours, store gelé" |
| AI Crawler Monitor | Vérifie si les bots IA (ChatGPT, Perplexity) crawlent tes pages produits ou juste les blogs. | Thread IA/SEO : "les crawlers IA accèdent aux blogs mais PAS aux pages produits. Vous pouvez être exclu sans le savoir" |
| Benchmark concurrence | Scanne 3-5 concurrents. Compare les scores. | Thread vitesse : merchant demande comment savoir si son site est rapide par rapport aux autres |
| Fix Generator | Pour chaque problème → action corrective en langage simple. | Thread vitesse : "Pas 'Optimize LCP' mais 'Désinstallez Popup Manager. +1.8s de vitesse'" |
| Weekly Report Push | Rapport lundi matin en push + email. Score, tendance, top 3 actions. | Thread quotidien : "à 16h j'ai fait beaucoup mais rien qui fasse avancer les choses" |
| Uninstall Residue Detector | Scanne le theme code pour détecter les résidus d'apps désinstallées (sitemaps orphelins, scripts morts, snippets liquid cassés). "3 résidus trouvés : Avada SEO (snippet liquid), PageFly (3 sitemaps), Reviews+ (script JS). Les retirer gagnerait 0.8s." | Reviews Avada (4+) + PageFly (4+) : "code staying behind after uninstall", "it bricked my site", "like a virus" |
| Pixel Health Check | Vérifie que les pixels Meta/Google se déclenchent correctement après chaque changement d'app ou de theme. | Review Avada : "freezing Facebook Pixel. They only load after a user clicks. You LOSE vital PageView data." |
| App Update Tracker | Après chaque mise à jour d'app Shopify, re-scanne et compare les scores. Alerte si régression. "L'app X a été mise à jour il y a 2h. Votre score mobile est passé de 78 à 64." | Reviews PageFly (3+) : "every update makes it worse", "they update the app and all websites start to look different" |
| Permission Monitor | Alerte quand une app demande des permissions excessives ou nouvelles (accès données clients, modification theme). | Review PageFly : "popup saying: update the app and grant us access to customer data like name, phone, email. Can't access my store without granting access." |

### L'agent en action
Dimanche 3h → StoreMD scanne → compare avec vendredi → détecte mobile checkout 0.8s plus lent → identifie app update samedi → lundi 8h push : "Your mobile checkout slowed down. Reviews+ updated yesterday." Le merchant n'a rien demandé.

### Pricing
Free (1 audit ponctuel) → 29$/mois (1 store, scan hebdo) → 79$/mois (scan quotidien, benchmark, bot filter) → 199$/mois (10 stores, white-label, API)

### Moat
Data accumulation (6 mois d'historique = irremplaçable) + Bot filter exclusif + App Risk Monitor unique sur le marché

---

## 2. LISTINGLAB — Le labo d'optimisation de catalogue (Score 32/41)

**Base :** FicheProduitAI | **Cible :** E-commerce Shopify | **Mois :** 1
**Validation terrain :** 4+ threads, 100+ commentaires (import produits, pages OOS, images, variantes)

### Le problème (5-30K$/an)
Un merchant de bandes dessinées passe des heures chaque semaine à "extraire des tableurs distributeurs, nettoyer les données, rechercher des images et vérifier les prix." Un autre doit "visiter chaque lien Google Drive, télécharger les images, les renommer, puis passer au produit suivant — redondant, ennuyeux, chronophage." Des merchants envoient du trafic payant vers des pages en rupture de stock sans le savoir — "un entonnoir sans issue."

### Features

| Feature | Ce que l'agent fait | Validation terrain |
|---------|-------------------|--------------------|
| Catalogue Scan | Scanne TOUS les listings via API Shopify. Score /100 par listing. Vue d'ensemble en 1 écran. | Aucun outil existant ne fait analyse → score → diagnostic → rewrite ciblé → benchmark |
| Priorisation par impact | Classe par REVENUE potentiel. "Ce listing : 500 vues/mois mais 0.3% conversion. Le fixer = 2000$/mois." | Thread OOS : les merchants ne savent pas quels listings perdent de l'argent |
| Diagnostic par élément | Pour chaque listing faible : quel élément est le problème (titre, description, images, SEO). | Thread images (8 upvotes) : merchants ne savent pas quoi optimiser en premier |
| Rewrite ciblé | Réécrit UNIQUEMENT ce qui est faible. Garde ce qui marche. | Concurrents (GoWise, SEO On) réécrivent tout à l'aveugle |
| Bulk Import Intelligent | Drag & drop CSV/tableur distributeur → l'agent matche images aux produits, formate les données, crée les listings. | Thread BD (5 upvotes) : "extraire tableurs, nettoyer données, chercher images = perte de temps" |
| Dead Listing Detector | Alerte quand un listing reçoit du trafic mais est OOS. Suggère produit de remplacement. | Thread OOS : "un entonnoir sans issue — les magasins perdent 40-50% de revenus potentiels" |
| Image Optimizer | Compression, redimensionnement, format WebP, alt text SEO auto-générés. En bulk. RÈGLE ABSOLUE : jamais d'optimisation destructrice. Garde TOUJOURS l'original. Preview avant/après obligatoire. Réversion en 1 clic. | Thread images (44 commentaires) : merchants utilisent ChatGPT pour compresser 1 image à la fois. "2048x2048, sous 200Ko, format WebP" + Reviews Avada (3+) : "image optimization ruined my shop's product photos", "messed up ALL first images of my products." |
| Product Variant Organizer | Analyse un catalogue et SUGGÈRE la meilleure structure de variantes. | Thread bonbons (9 upvotes) : merchant galère avec variantes complexes (taille × saveur × quantité) |
| SEO Engine | Keywords par produit. Volume, difficulté, suggestions. | Thread images : "le texte alternatif est non négociable pour le SEO" |
| Multi-langue | Optimisation en 20+ langues. | Merchants EU qui vendent en FR, DE, ES, IT |
| New Product Watch | Webhook Shopify : nouveau produit → analyse auto → alerte si faible → version optimisée proposée en 5 min. | Merchants ajoutent des produits régulièrement sans les optimiser |
| Benchmark catégorie | Compare chaque listing aux top sellers de la même catégorie. | Thread images : "les 5 best sellers ont des descriptions de 150-200 mots avec 3 bullet points" |
| Bulk Operations | Réécrire 50-500 listings en 1 clic. Review + approve avant push Shopify. | Merchants avec 200-5000 produits ne peuvent pas optimiser un par un |
| Zero Lock-in | Les optimisations sont pushées DANS Shopify via API. Si tu désinstalles ListingLab, tes listings restent optimisés. Jamais de revert. | Reviews Avada (3+) : "work reverted upon cancelling", "when you stop, it reverts everything — from my point of view this is a scam" |
| Safe Mode | Avant toute modification bulk, preview des changements. Le merchant approuve CHAQUE batch avant push. Jamais de modification silencieuse. | Reviews Avada (8+) + PageFly (5+) : "changes theme code WITHOUT permission", "disconfigured my entire store" |

### Pricing
Free (5 analyses) → 29$/mois (100 produits) → 79$/mois (1000 produits, benchmark, A/B titles) → 199$/mois (illimité, API, white-label)

### Moat
Data catalogue + intégration Shopify bidirectionnelle + Bulk Import Intelligent + SEO engine

---

## 3. LEADQUIZ — Quiz lead gen connecté catalogue (Score 28/41)

**Base :** QuizForge | **Cible :** E-com + Coaches | **Mois :** 3
**Validation terrain :** 1 thread, 20 commentaires (quiz marketing, lead gen)

### Le problème
Typeform (39$/mois) et Interact (89$/mois) ne sont PAS connectés au catalogue Shopify. "L'email capturé après un quiz convertit 2-3x mieux qu'un popup générique." Cas concret : fleuriste +14% conversion + 10K$ revenu.

### Features

| Feature | Ce que l'agent fait | Validation terrain |
|---------|-------------------|--------------------|
| Quiz Generator | 3 phrases → quiz complet en 2 min. | Thread quiz : "les quiz fonctionnent quand les clients se sentent dépassés par le choix" |
| Catalogue Connect | API Shopify. Résultats = VRAIS produits avec lien "Ajouter au panier". | Aucun concurrent ne connecte quiz → catalogue Shopify nativement |
| Email Capture mi-parcours | Capture email AVANT résultats (pas à la fin). Intégration Klaviyo, Mailchimp, Brevo. | Thread quiz : "collectez des emails à mi-parcours, pas à la fin. Le taux de désabonnement vous tue" |
| Revenue Attribution | Connecte résultats quiz → achats réels Shopify. ROI du quiz en temps réel. | Thread quiz : les outils existants ne mesurent pas le revenu attribué au quiz |
| Auto-Optimize | Analyse drop-offs par question. Suggère des modifications. A/B test auto. | Thread quiz : "la question 3 perd 40% des répondants — la reformuler" |
| Max 5 questions | Design forcé à la concision. | Thread quiz : "pas plus de 6-7 questions. Les gens décrochent" |

### Pricing
Free (1 quiz, 50 réponses/mois) → 19$/mois (3 quiz, 500 réponses) → 49$/mois (illimité) → 79$/mois (multi-stores)

---

## CROSS-SELL E-COM

| Si le client utilise | On propose | Pitch |
|---------------------|-----------|-------|
| StoreMD | ListingLab | "Store healthy mais listings faibles" |
| ListingLab | StoreMD | "Listings optimisés mais store a des problèmes" |
| StoreMD + ListingLab | ChargebackShield | "Vous convertissez bien, protégez vos revenus" |
| Tout e-com | ProfitPilot | "Vous vendez — mais quel est votre VRAI profit ?" |

**Bundle e-com :** StoreMD + ListingLab + ChargebackShield + ProfitPilot = 199$/mois (au lieu de 316$). Le merchant qui a les 4 ne quitte jamais.
