# FLÈCHE 2 (V2) — Nouveaux SaaS à créer (problèmes à 10K$/an)

**Date :** 03 avril 2026
**Lens :** La complexité = le moat. On construit ce qui est DIFFICILE à reproduire.
**Filtre :** Chaque produit résout un problème qui coûte > 5K$/an au client.

---

## VERTICAL E-COMMERCE

---

### 1. CHARGEBACKSHIELD — Prévention fraude IA prédictive

**Le problème (800$/mois par store en moyenne) :**
Les merchants posent littéralement la question "comment les chargebacks sont-ils légaux ?" quand ils perdent des litiges avec preuves de tracking, confirmation de livraison, et messages clients. Les banques se rangent du côté des clients 80% du temps. Un seul chargeback de 4200$ peut tuer une petite boutique. Les outils existants sont RÉACTIFS — ils aident APRÈS le chargeback. Personne ne prévient AVANT.

**La solution :**
IA qui analyse chaque commande AVANT l'expédition et score le risque de chargeback. Signals : adresse de livraison différente de la facturation, email jetable, comportement d'achat atypique, historique IP, vitesse de commande, combinaison produit/quantité suspecte. Si le score de risque est élevé → alerte au merchant → action recommandée (confirmation email, appel, annulation).

**En plus :** génération automatique de dossiers de contestation quand un chargeback arrive. L'IA compile les preuves (tracking, emails, screenshots) dans le format exact que les banques exigent.

**Concurrence :**
| Outil | Prix | Limite |
|-------|------|--------|
| Chargeflow | 25% du chargeback récupéré | RÉACTIF — intervient après. Cher (25% commission). |
| NoFraud | 19$+/mois | Orienté fraude paiement, pas chargeback friendly fraud |
| Shopify Protect | Gratuit (Shop Pay) | Uniquement Shop Pay Checkout, très limité |

**LE GAP :** Aucun outil ne fait de la PRÉDICTION + PRÉVENTION + CONTESTATION automatisée dans un seul produit pour les petits merchants Shopify.

**Stack :** FastAPI + Supabase + ML scoring (features engineering sur les données commande) + Claude API (génération dossiers contestation) + Shopify API (webhooks commandes)

**Pricing :** Free (50 commandes/mois) → 49$/mois (500 commandes) → 99$/mois (2000) → 199$/mois (illimité)

**Moat :** MASSIF. Chaque commande analysée enrichit le modèle. Plus de data = meilleure prédiction. Network effect : les patterns de fraude détectés chez un merchant protègent tous les autres.

**Score : 35/41** — Le problème coûte le plus cher (800$/mois), la willingness-to-pay est maximale (ROI 10x), et le moat data est le plus fort.

---

### 2. PROFITPILOT — Comptabilité e-commerce automatisée IA

**Le problème (20K$/an) :**
La comptabilité DIY prend 15-20h par mois (600-800$ en coût d'opportunité), les comptables coûtent 300-1000$/mois. Les déductions fiscales manquées valent des milliers, les pénalités d'audit potentielles aussi, et les erreurs mènent à de mauvaises décisions business.

Shopify donne les données de ventes, mais c'est seulement 20% de ce qui est nécessaire pour une comptabilité correcte. Les frais de transaction, apps, ads, shipping, returns, refunds — tout est dans des systèmes différents avec des formats différents.

**La solution :**
"TurboTax for Shopify". Connecte Shopify + Stripe + PayPal + Meta Ads + Google Ads + compte bancaire → l'IA catégorise automatiquement TOUT → profit & loss en temps réel → alerte si les marges baissent → rapport fiscal 1-clic → prédiction de cashflow.

**Ce que ça fait concrètement :**
- Profit réel par produit (pas juste le revenue — TOUT inclus : COGS, shipping, ads, fees, returns)
- Dashboard : "Aujourd'hui tu as fait 847$ de revenue mais seulement 203$ de profit réel"
- Alertes : "Ton produit X te coûte plus qu'il ne rapporte depuis 2 semaines"
- Rapport fiscal : "Voici tes charges déductibles ce trimestre — tu rates 1200$ de déductions"
- Prédiction : "À ce rythme, tu seras en cash négatif dans 6 semaines"

**Concurrence :**
| Outil | Prix | Limite |
|-------|------|--------|
| QuickBooks | 30-200$/mois | PAS spécifique e-commerce. Nécessite catégorisation manuelle. |
| A2X | 19-99$/mois | Bon mais JUSTE la réconciliation Shopify→QuickBooks. Pas de P&L, pas d'alertes, pas de prédiction. |
| BeProfit | 25-150$/mois | Dashboard profit mais pas de comptabilité complète, pas de fiscal |

**LE GAP :** Aucun outil ne fait comptabilité + profit tracking + alertes + fiscal + prédiction cashflow en un seul endroit pour les e-commerçants. Ils utilisent 3-4 outils ou un comptable.

**Pricing :** 29$/mois (1 store) → 79$/mois (multi-stores + fiscal) → 149$/mois (prédictions + advisory IA)

**Moat :** Data financière = la donnée la plus sticky. Personne ne migre ses données comptables. Le switching cost est ÉNORME.

**Score : 33/41**

---

## VERTICAL AGENCES / FREELANCERS

---

### 3. CLIENTPULSE — Le cerveau IA du freelancer marketing

**Le problème (le vrai, pas le symptôme) :**
Le freelancer marketing ne perd pas juste du temps en reporting. Il perd du temps sur TOUT le cycle client : prospection → proposal → onboarding → exécution → reporting → facturation → retention. Et il utilise 6-8 outils séparés (Apollo pour la prospection, Google Docs pour les proposals, Notion pour le project management, Looker Studio pour les rapports, Stripe pour la facturation, Mailchimp pour les emails). Chaque outil coûte 20-100$/mois. Total stack : 200-500$/mois.

Les heures réelles de travail incluent la prospection, les proposals, la comptabilité et la maintenance logicielle. Le freelancer travaille 50-60h/semaine mais seulement 30-35h génèrent directement du revenue.

**La solution :**
Un HUB unique pour freelancers marketing qui couvre le cycle complet avec l'IA partout :

| Module | Ce qu'il fait | Ce que l'IA ajoute |
|--------|--------------|-------------------|
| **Prospect** | Scan de sites web prospects → mini-audit CRO/SEO → outreach template | IA génère l'audit + le message personnalisé (= ProspectScan intégré) |
| **Propose** | Templates proposals par service, pricing calculator, signature électronique | IA rédige la proposal à partir du brief client en 2 min |
| **Deliver** | Kanban simple par client, deadlines, livrables, fichiers | IA alerte si un projet est en retard ou si un client n'a pas répondu depuis 7 jours |
| **Report** | Connecte GA + Meta + Google Ads → rapport mensuel auto | IA ÉCRIT les insights et recommandations (= ReportPilot intégré) |
| **Bill** | Facturation auto, suivi paiements, relances | IA envoie les relances au bon timing |
| **Retain** | Suivi satisfaction, upsell suggestions, NPS auto | IA détecte les signaux de churn ("le client ouvre moins les rapports") |

**Concurrence :**
| Outil | Prix | Ce qu'il fait | Ce qu'il manque |
|-------|------|---------------|----------------|
| HubSpot Free CRM | 0-800$/mois | CRM + marketing | Trop complexe, pas adapté freelancer, le pricing scale très vite |
| Pipedrive | 15-99$/mois | CRM ventes | Pas de reporting client, pas de proposals, pas d'audit |
| AgencyAnalytics | 79-399$/mois | Reporting | JUSTE du reporting. Pas de CRM, pas de proposals, pas de billing. |
| Proposify | 49$/mois | Proposals | JUSTE des proposals. |
| Toggl Track | 10-20$/mois | Time tracking | Pas de CRM, pas de reporting. |

**LE GAP :** Les freelancers utilisent 6 outils à 200-500$/mois. ClientPulse remplace tout pour 49-99$/mois. Et l'IA fait le travail que le freelancer fait manuellement en 20h/semaine.

**Stack :** FastAPI + Next.js + Supabase + Claude API + intégrations (GA API, Meta API, Stripe, Resend pour emails)

**Pricing :** Free (2 clients) → 29$/mois (5 clients) → 79$/mois (15 clients) → 149$/mois (illimité + white-label)

**Moat :** Data clients + historique projets + templates personnalisés = switching cost massif. Un freelancer qui a 12 mois de données dans ClientPulse ne migre JAMAIS.

**Score : 36/41** — Le plus haut score. Résout LE problème systémique du freelancer, pas un symptôme. Remplace 6 outils. Le moat data est maximum.

---

### 4. ADAUDIT — Audit publicitaire IA pour agences

**Le problème :**
Les agences marketing gèrent les Meta Ads et Google Ads de leurs clients. L'optimisation est complexe, les erreurs coûtent cher, et les clients demandent "pourquoi mes ads ne marchent pas ?". L'agence passe des heures à analyser les comptes publicitaires manuellement.

**La solution :**
Connecte le compte Meta Ads + Google Ads du client → l'IA analyse : budget gaspillé sur des audiences non-performantes, creative fatigue (ads qui tournent depuis trop longtemps), enchères sous-optimales, audiences qui se chevauchent, landing pages qui ne matchent pas les ads. Génère un rapport "Voici 12 000$ de gaspillage ce mois-ci et voici comment le récupérer."

**Pricing :** 49$/mois (1 compte) → 149$/mois (10 comptes) → 299$/mois (illimité)

**Score : 30/41** — Fort mais les intégrations Meta/Google sont complexes à maintenir.

---

## VERTICAL CONTENT CREATORS

---

### 5. CREATORSUITE — Le studio IA tout-en-un du créateur

**Le problème (le vrai) :**
Un créateur YouTube/podcast utilise actuellement : Descript (editing 24$/mois) + VidIQ (7$/mois) + Canva (13$/mois) + Buffer (6$/mois) + Opus Clip (15$/mois) + ConvertKit (29$/mois) + Castmagic (39$/mois) = 133$/mois minimum. Et il passe quand même 15-20h/semaine sur des tâches non-créatives.

**La solution :**
Un seul outil qui fait TOUT le workflow post-création :

| Module | Ce qu'il fait |
|--------|--------------|
| **Transcribe** | Vidéo/audio → transcription parfaite (Whisper) |
| **Repurpose** | Transcription → 5 tweets, 3 posts LinkedIn, 1 newsletter, 10 citations, 3 threads |
| **Clip** | Vidéo longue → identifie les 5 meilleurs moments → extrait les clips (Shorts/Reels) avec captions |
| **Thumbnail** | Analyse les thumbnails de ta niche → score ta thumbnail → génère 3 alternatives → A/B test prédictif |
| **SEO** | Keywords YouTube + suggestions de titre → analyse la concurrence sur chaque keyword |
| **Schedule** | Publie les clips + posts sur toutes les plateformes au meilleur horaire |
| **Analytics** | Dashboard simplifié "cette semaine : meilleure vidéo, pourquoi, quoi refaire" |
| **Monetize** | Media kit auto-généré + calculateur pricing sponsoring |

**Concurrence :** Fragmentée (voir au-dessus — 7 outils séparés). AUCUN tout-en-un à < 50$/mois.

**Stack :** FastAPI + Next.js + Supabase + Whisper/Deepgram (transcription) + Claude API (repurposing, SEO, analytics insights) + FFmpeg (clip extraction) + YouTube/TikTok/LinkedIn APIs (scheduling + analytics)

**Pricing :** Free (2 vidéos/mois) → 19$/mois (10 vidéos) → 49$/mois (illimité, tous modules) → 99$/mois (teams, multi-chaînes)

**Moat :** Le tout-en-un est le moat. Personne n'a construit ça parce que c'est complexe. Avec Claude Code, vous pouvez.

**Score : 31/41** — Gros potentiel volume mais pricing plus bas et concurrence IA qui arrive vite.

---

## MATRICE FINALE — Par impact business

| Rang | Produit | Vertical | Coût du problème /an | Pricing | Moat | Score |
|------|---------|----------|---------------------|---------|------|-------|
| 🥇 | **ClientPulse** | Agences/Freelancers | 15-25K$ (6 outils + 20h/sem perdues) | 29-149$/mois | Data + workflow + switching cost | 36/41 |
| 🥈 | **ChargebackShield** | E-commerce | 10K$ (800$/mois en chargebacks) | 49-199$/mois | Data ML + network effect | 35/41 |
| 🥉 | **StoreMD** | E-commerce | 10-120K$ (conversions perdues) | 29-199$/mois | Data + monitoring continu + App Store | 34/41 |
| 4 | **ProfitPilot** | E-commerce | 20K$ (temps + erreurs + déductions) | 29-149$/mois | Data financière = ultra sticky | 33/41 |
| 5 | **ListingLab** | E-commerce | 5-30K$ (listings faibles = ventes perdues) | 29-199$/mois | Data + intégration Shopify | 32/41 |
| 6 | **CreatorSuite** | Content Creators | 1.6K$ (7 outils) + temps | 19-99$/mois | Tout-en-un complexe | 31/41 |
| 7 | **AdAudit** | Agences | 12K$+ (budget ads gaspillé) | 49-299$/mois | Intégrations Meta/Google | 30/41 |
| 8 | **LeadQuiz** | E-com + Coaches | Variable | 19-79$/mois | Templates + intégration catalogue | 28/41 |

---

## RECOMMANDATION SÉQUENCE (sans limite de build)

### Sprint 1 — Pendant le warming (S1-S3)

**F build en parallèle du warming :**

1. **StoreMD** = mutation de Leak Detector. Le core existe. Ajouter : monitoring récurrent (Celery), historique (Supabase), benchmark (Playwright multi-sites), alertes (Resend), dashboard trends (Next.js + Recharts). Time : 1 semaine pour le MVP monitoring, 2 semaines pour le benchmark et dashboard.

2. **ListingLab** = FicheProduitAI mutée. Context.md prêt. Ajouter : scan catalogue complet (API Shopify), scoring par listing, priorisation des faibles, bulk rewrite. Time : 1-2 semaines MVP.

### Sprint 2 — Après validation (S4-S6)

3. **ClientPulse** OU **ChargebackShield** selon quelle vertical a le mieux répondu en validation.

- Si e-commerce domine → **ChargebackShield** (le problème le plus coûteux, le moat le plus fort)
- Si agences/freelancers domine → **ClientPulse** (le score le plus haut, remplace 6 outils)

### Sprint 3 — Mois 2-3

4. Le produit non-choisi au Sprint 2
5. **ProfitPilot** si l'audience e-commerce est solide
6. **CreatorSuite V1** (text repurposing) si les creators convertissent

### La vision à M6

Un portfolio de 4-5 SaaS concentrés sur 2 verticals (e-commerce + agences), distribués dans les mêmes communautés, cross-sell entre tous les produits, moat data croissant sur chacun.
