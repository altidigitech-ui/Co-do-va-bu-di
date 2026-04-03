# CONTEXT — Distribution-First Method (V2)

**Source de vérité** pour la stratégie FoundryTwo.
**Dernière mise à jour :** 03 avril 2026
**Utilisé par :** F (Fabrice), R (Romain), Claude
**Statut :** ACTIF — remplace TOUT ce qui précède

---

## 1. POURQUOI CE PIVOT

### Ce qui n'a pas marché

Approche précédente : trouver une idée → coder → chercher où vendre.
Résultats Leak Detector après 3 semaines : ~8 signups, 0€ MRR, cible dev qui DIY tout.

### Ce qui change

1. **Distribution-first** : on ne build rien sans validation communauté
2. **Cible non-dev** : e-commerce sellers, agences marketing, freelancers, content creators
3. **Full-time** : F et R au chômage = 100% dédié
4. **Pas de limite de build** : Claude Code + IA = la complexité technique est un MOAT, pas un frein
5. **Volume × Constance** : le moteur de la distribution

---

## 2. LE LOOP

```
COMMUNAUTÉ → DOULEUR → VALIDATION → BUILD → DISTRIBUTION (VOLUME × CONSTANCE) → REPEAT
```

Chaque produit naît d'une communauté. Chaque décision est filtrée par ce loop.

---

## 3. PRINCIPES FONDAMENTAUX

### La complexité = le moat

Avec Claude Code et les agents IA, tout est codable. La question n'est pas "est-ce qu'on peut le construire ?" mais "est-ce que le problème vaut assez cher pour justifier un produit complexe ?". Plus c'est dur à reproduire, moins il y a de concurrence. On ne cherche pas les quick wins faciles — on cherche les problèmes à 10K$/an que personne ne résout bien.

### Volume × Constance = non-négociable

| Métrique | F minimum/jour | R minimum/jour |
|----------|---------------|---------------|
| Interactions communautés | 15 | 30 |
| Cold outreach (phase distrib) | 10 | 20 |
| Posts contenu | 1 (5/sem) | 1 (7/sem) |

En dessous → le loop ne tourne pas assez vite.

### La Toile = avantage structurel

3 comptes (R, F, F2) = 3 portes d'entrée, 1 destination. Le cross-engagement R↔F amplifie la visibilité de chaque interaction. Un solo founder a 1 voix. On en a 3.

---

## 4. L'ÉQUIPE

| | Romain (R) | Fabrice (F) |
|---|---|---|
| **Rôle** | Growth/Distribution lead | CTO/Builder + Distribution |
| **Temps/jour** | 7-10h | 7-10h |
| **Dans ce repo** | Distribution full-time | Distribution full-time |
| **Angle communautés** | Growth, conversion, acquisition, pricing | Technique, automatisation, stack, workflow |
| **Comptes** | @delgado_ro72224 (perso) | @FabGangi (perso) |
| **Studio** | Gère @foundrytwo | — |

---

## 5. VERTICALS CIBLES

### Verticals GO (infiltration active)

| Vertical | Score /41 | Communautés principales | Lead |
|----------|-----------|------------------------|------|
| **E-commerce sellers** (Shopify/Amazon) | 33 | r/shopify (340K), r/ecommerce (100K), Shopify Entrepreneurs FB (100K) | R |
| **Agences marketing & freelancers** | 31 | r/digital_marketing (200K), r/freelance (200K), Digital Distillery FB (148K) | R |
| **Content creators** (YouTube/TikTok) | 28 | r/NewTubers (579K), r/youtubers (262K), YouTube Creators Hub FB | F |

### Verticals BACKLOG

Coaches/course creators (25/41), restaurants (22/41), real estate (20/41) — revisiter si les 3 premières ne convertissent pas.

---

## 6. PORTEFEUILLE PRODUITS

### 6.1 Mutations des SaaS existants

| Original | Mutation | Cible | Score | Statut |
|----------|---------|-------|-------|--------|
| Leak Detector | **StoreMD** — Médecin CRO permanent : monitoring continu, benchmark concurrence, alertes, historique | E-commerce | 34/41 | Sprint 1 |
| FicheProduitAI | **ListingLab** — Labo d'optimisation catalogue : scan complet, scoring par listing, priorisation, bulk rewrite, benchmark | E-commerce | 32/41 | Sprint 1 |
| QuizForge | **LeadQuiz** — Quiz lead generation : connecté au catalogue Shopify, recommandation produit, analytics | E-com + Coaches | 28/41 | Sprint 3 |

### 6.2 Nouveaux SaaS à créer

| Produit | Vertical | Problème (coût/an) | Score | Sprint |
|---------|----------|-------------------|-------|--------|
| **ClientPulse** — Hub IA du freelancer (prospect→propose→deliver→report→bill→retain) | Agences/Freelancers | 15-25K$ (6 outils + 20h/sem perdues) | 36/41 | Sprint 2 |
| **ChargebackShield** — Prévention fraude IA prédictive + contestation auto | E-commerce | 10K$ (800$/mois chargebacks) | 35/41 | Sprint 2 |
| **ProfitPilot** — Comptabilité e-commerce automatisée IA ("TurboTax for Shopify") | E-commerce | 20K$ (temps + erreurs + déductions) | 33/41 | Sprint 3 |
| **CreatorSuite** — Studio IA tout-en-un (transcribe→repurpose→clip→thumbnail→schedule→analytics) | Creators | 1.6K$ outils + 15h/sem | 31/41 | Sprint 3 |
| **AdAudit** — Audit publicitaire IA (Meta + Google Ads) | Agences | 12K$+ budget gaspillé | 30/41 | Sprint 3 |

### 6.3 SaaS KILL

| Produit | Raison |
|---------|--------|
| PayloadDiff | Cible dev = contraire à la stratégie |
| DevToolsAPI | Idem |
| Leak Detector (tel quel) | Remplacé par StoreMD |
| FicheProduitAI (tel quel) | Remplacé par ListingLab |
| QuizForge SCORM | Remplacé par LeadQuiz |

---

## 7. CADENCE PRODUITS

### Cycle par produit
Le build se fait dans des projets Claude séparés. Ce repo ne gère que la distribution.

| Étape | Durée | Responsable |
|-------|-------|-------------|
| Build | 2-5 jours | F (dans un projet Claude dédié) |
| Distribution + validation | 1-2 semaines | R + F (dans ce repo) |
| Décision GO/KILL | 48h test | R + F |
| Scale ou next | Continu | R + F |

### Cadence
- Build : 3-4 SaaS/mois (Claude Code full-time)
- Distribution : le bottleneck n'est plus le build, c'est la distribution
- Objectif M3 : 12 SaaS testés, 2-3 validés, 1-2 avec MRR
- Objectif M6 : 24 SaaS testés, portfolio de 4-5 SaaS actifs

### Suivi
Le statut de chaque produit est dans produits/STATUS.md.
Quand F finit un build → il met à jour STATUS.md → R commence la distribution.

---

## 8. CONTRAINTES HARD (inchangées)

| Contrainte | Seuil |
|------------|-------|
| Budget total | ≤ 200€ par SaaS pour lancer |
| Revenue M1 | > 0€ réaliste |
| Stack | FastAPI + Next.js 14 + Supabase + Stripe + Claude API |
| Automatisable | ≥ 90% sans intervention humaine |
| Légal clean | Pas de données réglementées |

### Contraintes distribution-first

| Contrainte | Seuil |
|------------|-------|
| Cible NON-dev | Obligatoire |
| Communauté active identifiée | ≥ 1 communauté > 5K membres actifs |
| Willingness-to-pay prouvée | Les gens paient déjà pour des solutions |
| Validation 48h | 10+ signups avant tout build |

### Contraintes RETIRÉES
| Ancienne contrainte | Pourquoi retirée |
|--------------------|-----------------|
| Time-to-market ≤ 4 semaines | Claude Code = build en 2-5 jours. Plus de limite. |
| 1 SaaS/mois | Cadence accélérée : 3-4 SaaS/mois. Le search algorithm est 3-4x plus rapide. |

---

## 9. WARMING & FARMING

Comptes Reddit et Facebook partent de ZÉRO. Plan 30 jours :

| Phase | Jours | Reddit | Facebook |
|-------|-------|--------|----------|
| Cold start | J1-J3 | Browse + upvote. ZERO commentaire. | Setup profil. 1-2 groupes perso. |
| Premiers commentaires | J4-J8 | 3-5 comments/jour subs faciles (r/AskReddit, etc.) | Liker + commenter amis. 1 groupe business/jour. |
| Subs mid-size | J9-J14 | Comments subs cibles (r/ecommerce, r/freelance). Objectif 200-300 karma. | Premiers commentaires dans FB Groups business. |
| Subs majeurs | J15-J21 | Comments r/shopify, r/digital_marketing. Premier post. 500+ karma. | Premiers posts dans FB Groups. Cross-engagement R↔F. |
| Opérationnel | J22-J30 | Posts valeur + audits gratuits + cold DMs. 1000+ karma. | Posts + audits + DMs + mention subtile produit. |

Détails complets dans WARMING-FARMING.md.

---

## 10. MÉTRIQUES

### Phase warming (S1-S3)

| Métrique | Seuil /semaine |
|----------|---------------|
| Interactions communautés (R+F) | 200+ |
| Douleurs documentées | 10+ |
| Karma Reddit (progression) | +150/semaine |

### Phase validation (S4)

| Métrique | Seuil GO |
|----------|----------|
| Signups en 48h | ≥ 10 |
| "Combien ça coûte ?" spontané | ≥ 2 |

### Phase distribution (S5+)

| Métrique | Seuil /semaine |
|----------|---------------|
| Cold outreach (R+F) | 150+ |
| Signups | 20+ |
| Trial → Paid | > 5% |

### Décision KILL vs CONTINUE

| Signal | Action |
|--------|--------|
| 0 signups après 2 semaines de distribution active | KILL le produit |
| > 5 clients payants à M1 | CONTINUE + volume |
| MRR > 500€ à M2 | INVEST |
| MRR > 2000€ + croissance > 20%/mois | DOUBLE DOWN |

---

## 11. CE DOCUMENT REMPLACE

- L'ancien framework de scoring (foundrytwo_saas_research_framework.md) pour les DÉCISIONS PRODUIT
- Le pipeline PayloadDiff → FicheProduitAI → QuizForge → DevToolsAPI
- L'approche build-first
- La cible dev
- La limite time-to-market de 4 semaines
- La cadence 1 SaaS/mois (remplacée par 3-4 SaaS/mois)
- Le suivi du build dans ce repo (le build est dans des projets Claude séparés)

Le framework de scoring /35 reste utilisable pour évaluer de nouvelles idées, mais les contraintes distribution-first et le scoring bonus distribution (+6 max) s'ajoutent obligatoirement.

---

## 12. DÉCISIONS PRISES

| Date | Décision | Rationale |
|------|----------|-----------|
| 03/04/2026 | Pivot distribution-first | 3 semaines LD : 0€ MRR |
| 03/04/2026 | Abandon cible dev | Pire marché pour bootstrap |
| 03/04/2026 | Volume × Constance non-négociable | Delta 10x entre plan et exécution sur LD |
| 03/04/2026 | Full-time F + R | Chômage = runway limité, temps illimité |
| 03/04/2026 | Validation 48h obligatoire | Plus jamais de build sans preuve de demande |
| 03/04/2026 | Complexité = moat | Claude Code = pas de limite. On build ce qui est DUR. |
| 03/04/2026 | KILL PayloadDiff + DevToolsAPI | Cible dev = hors stratégie |
| 03/04/2026 | LD → StoreMD, FPA → ListingLab, QF → LeadQuiz | Mutations profondes, pas des pivots cosmétiques |
| 03/04/2026 | Nouveaux produits : ClientPulse (36), ChargebackShield (35), ProfitPilot (33) | Problèmes à 10-25K$/an, moat data, scoring top |
| 03/04/2026 | Cadence 3-4 SaaS/mois | Claude Code = build en 2-5j. La distribution est le bottleneck. |
| 03/04/2026 | Ce repo = distribution uniquement | Le build se fait dans des projets Claude séparés |
