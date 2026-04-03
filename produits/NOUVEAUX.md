# NOUVEAUX SaaS — Créés from scratch

Dernière mise à jour : 03/04/2026
Même architecture commune que MUTATIONS.md (Agent 4 couches + PWA).

---

## MOIS 1 — E-COMMERCE

### 1. CHARGEBACKSHIELD — Bouclier anti-fraude prédictif (Score 35/41)

**Cible :** E-commerce Shopify | **Problème :** 10K$/an (800$/mois chargebacks)

Le système est truqué contre les merchants. Tracking, confirmation livraison, messages clients — ils perdent quand même 80% des disputes. Un chargeback de 100$ coûte 461$ réellement (produit + shipping + fees + temps). Dépasser 0.9% de ratio = amendes 25-100K$/mois + perte du droit de traiter les paiements.

Les outils existants (Chargeflow, Disputifier) sont RÉACTIFS. Personne ne prévient AVANT l'expédition.

| Feature | Ce que l'agent fait |
|---------|-------------------|
| Pre-Ship Score | Score risque 0-100 par commande AVANT expédition. Analyse : adresse mismatch, email jetable, vélocité achat, historique IP, comportement navigation. Push : "Commande #4521 risque 87% — confirmer ou bloquer ?" |
| Smart Hold | Commandes >75% risque → attente auto avec notification. Commandes safe → passent sans friction. |
| Auto-Evidence Builder | Chargeback reçu → l'agent compile le dossier automatiquement (tracking, emails, screenshots) dans le format Visa/Mastercard. Contestation en 1 clic. |
| Pattern Detection | Patterns de fraude cross-merchants. Un pattern chez un merchant protège TOUS les autres. Network effect. |
| Ratio Monitor | Surveille le ratio en temps réel. Alerte AVANT le seuil 0.9%. "Ratio à 0.72%. À ce rythme → 0.9% dans 18 jours." |
| Friendly Fraud Detector | Identifie les clients qui achètent puis disputent. Marqués pour les futures commandes. |
| Revenue Dashboard | Combien sauvé : chargebacks évités + gagnés. "Ce mois : 4800$ sauvés, 1200$ récupérés. ROI abonnement : 60x." |

**Pricing :** Free (50 commandes/mois) → 49$/mois (500) → 99$/mois (2000) → 199$/mois (illimité)

**Moat :** Data ML + network effect (chaque merchant renforce la détection pour tous)

---

## MOIS 2 — AGENCES + E-COM RENFORCÉ

### 2. CLIENTPULSE — Le cerveau IA du freelancer (Score 36/41)

**Cible :** Agences/Freelancers marketing | **Problème :** 15-25K$/an (6 outils + 20h/sem non-productif)

Le freelancer travaille 50-60h/semaine. 30-35h productives. Le reste : prospection, proposals, reporting, admin, relances. 6-8 outils à 200-500$/mois.

| Module | Ce que l'agent fait |
|--------|-------------------|
| PROSPECT | Scanne le site d'un prospect → mini-audit CRO/SEO 60 sec → message d'approche personnalisé. Taux de réponse 5-10x vs cold email generic. |
| PROPOSE | Brief en 3 phrases → proposal complète en 2 min (scope, timeline, pricing, livrables). Templates par service. Signature électronique. |
| DELIVER | Kanban par client. Deadlines, livrables. L'agent alerte : "Client X n'a pas répondu depuis 7 jours." |
| REPORT | Connecte GA4 + Meta Ads + Google Ads → rapport mensuel 1 clic avec insights IA en phrases. White-label PDF. |
| BILL | Factures auto. Suivi paiements. Relances J+7, J+14, J+30 automatiques. |
| RETAIN | Détecte signaux de churn : "Client Y n'ouvre plus les rapports depuis 2 mois. Risque élevé. Suggestion : call stratégique gratuit." |

**Pricing :** Free (2 clients) → 29$/mois (5 clients) → 79$/mois (15 clients) → 149$/mois (illimité, white-label)

**Moat :** Data clients + historique + templates = switching cost massif après 6 mois

### 3. PROFITPILOT — Comptabilité e-com IA (Score 33/41)

**Cible :** E-commerce | **Problème :** 20K$/an (15-20h/mois compta + erreurs + déductions manquées)

Le merchant sait combien Shopify lui verse. Il ne sait pas combien il GAGNE après COGS, shipping, ads, fees, returns, taxes.

| Feature | Ce que l'agent fait |
|---------|-------------------|
| True Profit par produit | Profit RÉEL temps réel : revenue - COGS - shipping - ads - fees - returns. "Yoga Mat : 49$ revenue, 4.20$ profit réel." |
| Daily P&L | Mis à jour quotidiennement. "Hier : 847$ revenue, 203$ profit réel (24% marge)." |
| Margin Alerts | Alerte si un produit passe en marge négative. "Accessories en négatif depuis 12 jours." |
| Ad Spend Tracker | Attribue le coût pub à chaque produit. "60% du budget ads va vers des produits à marge <10%." |
| Tax Ready | Catégorisation auto. Rapport fiscal 1 clic. Détection déductions manquées. |
| Cashflow Forecast | Prédit le cashflow 30/60/90 jours. "Compte à 0 dans 47 jours. Réduire ads de 20% = +23 jours de runway." |

**Pricing :** 29$/mois (1 store) → 79$/mois (multi-stores + fiscal) → 149$/mois (prédictions + advisory IA)

### 4. ADAUDIT — Auditeur publicitaire IA (Score 30/41)

**Cible :** Agences marketing | **Problème :** 12K$+/an budget ads gaspillé

| Feature | Ce que l'agent fait |
|---------|-------------------|
| Waste Detector | Budget gaspillé : audiences non-performantes, creative fatigue, enchères trop élevées, audiences chevauchées. |
| Creative Fatigue Alert | Détecte quand un ad perd en performance. "Ad 'Summer Collection' -34% CTR en 2 semaines. 3 angles alternatifs." |
| ROAS par produit | ROAS par produit, pas par campagne. "Produit A : 4.2x. Produit B : 0.9x. Vous perdez sur B." |
| Client Report IA | Rapport mensuel auto avec insights langage simple. White-label. |
| Multi-account | 10+ comptes clients depuis un dashboard. |

**Pricing :** 49$/mois (1 compte) → 149$/mois (10 comptes) → 299$/mois (illimité)

---

## MOIS 3 — CREATORS + CROSS-SELL

### 5. CREATORSUITE — Studio IA tout-en-un (Score 31/41)

**Cible :** Content Creators YouTube/TikTok/Podcast | **Problème :** 1.6K$/an outils + 15h/sem non-créatif

67% des cas de burnout = rythme insoutenable. 1 vidéo de 15 min devrait devenir 5 Shorts + 5 posts LinkedIn + 3 tweets + 1 newsletter. Le repurposing prend 4-6h/épisode. La plupart ne le font pas.

| Module | Ce que l'agent fait |
|--------|-------------------|
| Auto-Transcribe | Vidéo/audio → transcription (Whisper/Deepgram). Timestamps, speakers, chapitres. |
| Repurpose Engine | Transcription → 5 tweets, 3 posts LinkedIn, 1 newsletter, 10 citations, 3 threads. Ton adapté par plateforme. 1 vidéo → 20+ contenus en 2 min. |
| Clip Detector | Identifie les 3-5 meilleurs moments pour Shorts/Reels. Timestamps + raison. En 30 secondes au lieu de 1h. |
| Clip Cutter | Extraction auto avec captions, format vertical, transition. FFmpeg. |
| Thumbnail Analyzer | Score ta thumbnail. Génère 3 alternatives. Prédit le CTR. |
| Title Optimizer | 5 variantes basées sur keywords YouTube + analyse des titres qui performent dans la niche. |
| Smart Schedule | Poste sur toutes les plateformes au meilleur horaire. |
| Performance Coach | "Cette semaine : meilleur vidéo, pourquoi, quoi reproduire." Pas un dashboard — un COACH. |

**Pricing :** Free (2 vidéos/mois) → 19$/mois (10 vidéos) → 49$/mois (illimité) → 99$/mois (teams)

### 6. LEADQUIZ — Voir MUTATIONS.md

### 7. [WILDCARD] — Issu des douleurs communautés (Mois 3)

Identifié pendant les mois 1-2 via douleurs-observees.md de R et F. Critères : problème observé 5+ fois, willingness-to-pay confirmée, aucune solution existante.

---

## CROSS-SELL MATRIX COMPLÈTE

| Si le client utilise | On propose | Pitch |
|---------------------|-----------|-------|
| StoreMD | ListingLab | "Store healthy mais listings faibles" |
| ListingLab | StoreMD | "Listings top mais store a des problèmes" |
| StoreMD + ListingLab | ChargebackShield | "Vous convertissez, protégez vos revenus" |
| ChargebackShield | ProfitPilot | "Vous bloquez la fraude, connaissez votre vrai profit" |
| ClientPulse | AdAudit | "Vous gérez vos clients, optimisez leurs ads" |
| AdAudit | ClientPulse | "Vous auditez les ads, gérez tout le cycle" |
| CreatorSuite | LeadQuiz | "Vous repurposez, capturez des leads" |

Bundle e-com : StoreMD + ListingLab + ChargebackShield + ProfitPilot = 199$/mois (vs 316$)
Bundle agence : ClientPulse + AdAudit = 179$/mois (vs 228$)

---

## RECHERCHE EN COURS — Scraping communautés

Les features ci-dessus sont basées sur la recherche web (articles, rapports, données concurrents). Une phase de scraping profond est en cours pour affiner avec les douleurs RÉELLES des communautés :

1. Script PRAW → 500 derniers posts par sub cible, filtrés par keywords de douleur
2. Apify → reviews 1-2 étoiles des apps concurrentes Shopify
3. Terrain → douleurs-observees.md rempli par R et F pendant le warming

Les résultats du scraping et du terrain viendront compléter et ajuster les features de chaque produit.
