# CONTEXT — Distribution-First Method

**Source de vérité** pour la stratégie d'acquisition FoundryTwo.
**Dernière mise à jour :** 03 avril 2026
**Utilisé par :** F (Fabrice), R (Romain), Claude
**Statut :** ACTIF — remplace l'approche précédente (build-first)
**Action :** Lundi 06/04/2026

---

## 1. POURQUOI CE PIVOT

### Ce qui n'a pas marché

L'approche précédente : trouver une idée → coder → chercher où vendre.

Résultats après 3 semaines de Leak Detector (lancé 16/03/2026) :
- ~8 signups, 0€ MRR
- 18 cold outreachs en 2 semaines (cible : 8-10/jour)
- Marché cible = devs qui peuvent builder eux-mêmes ces outils
- Zero traction organique, zero viralité

Le problème n'était pas le produit. Le problème était :
1. **Mauvais marché** — vendre des outils dev à des devs = pire niche pour un bootstrap
2. **Pas de distribution** — volume et constance insuffisants (1 cold/jour vs 10)
3. **Pas de communauté** — aucune présence établie avant de pitcher
4. **Build-first** — on construisait puis on cherchait où vendre

### Ce qui change

Deux changements majeurs simultanés :
- **Méthode** : on passe de build-first à distribution-first
- **Disponibilité** : F et R sont full-time (chômage), pas side project

---

## 2. LE LOOP

```
COMMUNAUTÉ → DOULEUR → VALIDATION → BUILD → DISTRIBUTION (VOLUME × CONSTANCE) → REPEAT
```

### Chaque étape en détail

**COMMUNAUTÉ (Semaine 1-2 du cycle)**
- Identifier 3-5 communautés actives dans une vertical non-dev
- S'infiltrer : être présent quotidiennement, répondre aux questions, apporter de la valeur gratuite
- Devenir un visage familier AVANT de pitcher quoi que ce soit
- Mapper : plateformes (Reddit, Facebook Groups, Discord, forums, LinkedIn Groups), volume d'activité, langue, taille, règles
- Observer : quels problèmes reviennent le plus souvent, quelles solutions existent déjà, combien les gens paient

**DOULEUR (En parallèle de l'infiltration)**
- Lister les plaintes récurrentes dans la communauté
- Identifier celles qui passent nos filtres hard (§4)
- Scorer : fréquence de mention × urgence × willingness-to-pay × faisabilité technique
- Sélectionner le top 3 des douleurs candidates

**VALIDATION (48-72h max)**
- Créer une landing page simple pour chaque douleur candidate
- Poster dans 3 communautés ciblées
- Seuil : 10+ signups en 48h = GO. Moins = NEXT
- Optionnel : proposer un audit gratuit / free tool pour valider l'intérêt
- Si aucune douleur ne valide → changer de communauté, pas persister

**BUILD (2-4 semaines)**
- F code avec IA (Claude Code, Cursor) — le build n'est plus le bottleneck
- Stack identique : FastAPI + Next.js 14 + Supabase + Stripe
- MVP strict : core value + billing + landing. Rien d'autre.
- F continue à être actif dans les communautés PENDANT le build (30% de son temps)

**DISTRIBUTION (VOLUME × CONSTANCE) — permanent, ne s'arrête jamais**
- Volume = nombre d'interactions/jour. Non-négociable. Pas "quand j'ai le temps".
- Constance = même débit chaque jour pendant 90 jours minimum. Pas de spike puis silence.
- La distribution commence PENDANT le build, pas après.
- Les premiers clients viennent de la communauté où vous êtes déjà présents.

**REPEAT**
- Le loop recommence pour le produit suivant
- La présence dans les communautés existantes continue (maintenance)
- Chaque communauté infiltrée = un canal permanent pour les futurs produits

---

## 3. L'ÉQUIPE (FULL-TIME)

### Fabrice (F) — CTO/Builder + Distribution

| Bloc | Activité | Volume |
|------|----------|--------|
| Matin | Communautés : réponses, engagement, observation douleurs | 1-2h |
| Journée | Build avec IA (Claude Code, Cursor) | 4-6h |
| Soir | Contenu : posts, réponses, cold outreach | 1-2h |
| **Total** | | **7-10h/jour** |

Distribution F :
- 15-20 interactions/jour dans les communautés (réponses, commentaires de valeur)
- 3-5 posts/semaine (contenu de valeur, pas du pitch)
- Cold outreach quand un produit est validé : 10-15/jour

### Romain (R) — Growth/Distribution FULL-TIME

| Bloc | Activité | Volume |
|------|----------|--------|
| Matin | Communautés : engagement, réponses, repérage douleurs | 2-3h |
| Journée | Cold outreach structuré + contenu | 3-4h |
| Soir | Suivi, DMs, relations, reporting | 2-3h |
| **Total** | | **7-10h/jour** |

Distribution R :
- 30-50 interactions/jour dans les communautés
- 5-7 posts/semaine de contenu de valeur
- Cold outreach actif : 20-30 contacts/jour quand un produit est en distribution
- Suivi des conversations : relance à J+3, J+7

### Volume minimum non-négociable (par jour, par personne)

| Activité | F minimum | R minimum |
|----------|-----------|-----------|
| Interactions communautés (réponses, commentaires) | 15 | 30 |
| Posts contenu de valeur | 1 (5/semaine) | 1 (7/semaine) |
| Cold outreach (quand produit actif) | 10 | 20 |
| DMs / suivis | 5 | 10 |

Ces chiffres sont des planchers, pas des objectifs. En dessous = le loop ne tourne pas assez vite.

---

## 4. CONTRAINTES HARD (inchangées)

Chaque idée doit passer ces filtres. Un seul échec → KILL.

| Contrainte | Seuil |
|------------|-------|
| Budget total | ≤ 200€ pour lancer |
| Time-to-market | ≤ 4 semaines de dev (IA accélère) |
| Revenue M1 | > 0€ réaliste |
| Stack | FastAPI + Next.js 14 + Supabase |
| 1 personne peut le coder | F seul (avec IA) |
| Automatisable | ≥ 90% sans intervention humaine |
| Légal clean | Pas de données réglementées |

### Contraintes NOUVELLES (distribution-first)

| Contrainte | Seuil | Pourquoi |
|------------|-------|----------|
| **Cible NON-dev** | La cible ne sait pas coder | Éviter le marché où tout le monde peut DIY |
| **Communauté active identifiée** | ≥ 1 communauté avec >5K membres actifs | Pas de marché sans canal de distribution gratuit |
| **Willingness-to-pay prouvée** | Les gens paient déjà pour des solutions (même mauvaises) | Pas de "on éduquera le marché" |
| **Time-to-value < 5 min** | L'utilisateur voit le résultat immédiatement | Les non-devs ne tolèrent pas la complexité |
| **Validation 48h** | 10+ signups en 48h depuis les communautés | Pas de build sans preuve de demande |

---

## 5. OÙ CHERCHER LES COMMUNAUTÉS

### 5.1 Plateformes par type de cible

| Cible | Plateformes principales | Plateformes secondaires |
|-------|------------------------|------------------------|
| **E-commerce sellers** | Reddit (r/ecommerce, r/shopify, r/FulfillmentByAmazon), Facebook Groups Shopify | Discord Shopify, forums Seller Central |
| **Marketing / Agencies** | Reddit (r/digital_marketing, r/PPC, r/SEO), Facebook Groups marketing | LinkedIn Groups, Slack communities |
| **Freelancers** | Reddit (r/freelance, r/Upwork), Facebook Groups freelance | Twitter/X, Discord |
| **Small business owners** | Reddit (r/smallbusiness, r/Entrepreneur), Facebook Groups locaux | LinkedIn, forums sectoriels |
| **Content creators** | Reddit (r/NewTubers, r/youtube), Facebook Groups créateurs | Discord, TikTok communities |
| **Real estate** | Facebook Groups agents immobiliers, Reddit (r/realtors) | LinkedIn, forums sectoriels |
| **Restaurants / Food** | Facebook Groups restaurateurs, Reddit (r/restaurateur) | Forums CHR, LinkedIn |
| **Coaches / Formateurs** | Facebook Groups coaching, Reddit (r/lifecoaching) | LinkedIn, Skool communities |

### 5.2 Comment évaluer une communauté

| Critère | Score 1 (mauvais) | Score 3 (moyen) | Score 5 (bon) |
|---------|-------------------|-----------------|---------------|
| **Taille** | <1K membres | 1-10K membres | >10K membres |
| **Activité** | <5 posts/semaine | 5-20 posts/semaine | >20 posts/semaine |
| **Douleurs exprimées** | Discussions vagues | Plaintes spécifiques | "Je paie X pour Y et c'est nul" |
| **Willingness-to-pay** | Tout doit être gratuit | Discussions sur les outils payants | Recommandations d'outils avec prix |
| **Accessibilité** | Groupe fermé, modération dure | Modération normale | Ouvert, engagement bienvenu |
| **Langue** | Non-anglais uniquement | Mix | Anglais-first |
| **Règles promo** | Zero tolérance | Toléré si valeur | Self-promo jour dédié |

Seuil : score ≥ 21/35 pour investir du temps. En dessous = chercher ailleurs.

### 5.3 Signaux d'or dans une communauté

- "Does anyone know a tool that…" → SIGNAL FORT
- "I've been using X but it's too expensive / too complex / missing Y" → SIGNAL FORT
- "I spent 3 hours doing X manually" → SIGNAL FORT
- "Has anyone automated X?" → SIGNAL MOYEN
- Des threads avec 50+ upvotes/likes sur un problème spécifique → SIGNAL FORT
- Des gens qui partagent des spreadsheets/templates DIY → ils ont besoin d'un outil

### 5.4 Signaux rouges

- Communauté morte (dernier post >1 semaine)
- Tout le monde veut du gratuit, personne ne paie
- Le problème est discuté mais personne ne cherche activement une solution
- La communauté est dominée par des vendeurs/spammers
- Barrière de langue ou culturelle trop forte

---

## 6. PROCESS D'INFILTRATION

### Phase 1 : Observation (Jours 1-3)

- Lire les 50 derniers posts les plus populaires
- Lister les 10 plaintes/questions les plus récurrentes
- Identifier les membres influents (ceux avec le plus de replies/upvotes)
- Comprendre le ton, le vocabulaire, les règles non-écrites
- NE PAS POSTER. Observer.

### Phase 2 : Apport de valeur (Jours 4-14)

- Répondre à des questions avec des réponses détaillées et utiles
- Partager des ressources gratuites (templates, guides, comparatifs)
- Aider des gens concrètement sans rien demander en retour
- Objectif : devenir quelqu'un que les gens reconnaissent et trustent
- NE PAS PITCHER. Aider.

### Phase 3 : Validation (Jours 14-17)

- Poster un "je construis X pour résoudre Y, qui est intéressé ?"
- Ou mieux : offrir un audit gratuit / mini-outil gratuit qui résout le problème
- Mesurer : signups, DMs reçus, commentaires positifs
- Seuil GO : 10+ signups en 48h

### Phase 4 : Distribution continue (Jour 17+, permanent)

- Continuer à apporter de la valeur (80% du contenu)
- Partager les updates du produit (20% du contenu)
- Cold outreach aux gens qui ont exprimé le problème
- Transformer les premiers users en ambassadeurs

---

## 7. CALENDRIER D'EXÉCUTION

### Phase 0 : Préparation (03-05 avril 2026)

- [x] Rédiger CONTEXT.md et CLAUDE.md
- [ ] Recherche approfondie des communautés actives non-dev
- [ ] Sélection des 3 verticals prioritaires
- [ ] Mapping des communautés (plateforme, taille, activité, langue)
- [ ] F et R alignés sur les volume minimums quotidiens

### Phase 1 : Infiltration (06-19 avril 2026 — 2 semaines)

- F et R s'infiltrent dans 3-5 communautés chacun
- Observation + apport de valeur quotidien
- Liste des douleurs candidates mise à jour chaque soir
- Vendredi 11/04 : premier scoring des douleurs
- Vendredi 18/04 : sélection du top 3 des douleurs à valider

### Phase 2 : Validation (20-22 avril 2026 — 48-72h)

- Landing pages pour les 3 douleurs candidates
- Posts dans les communautés
- Mesure des signups
- Décision GO/KILL sur chaque douleur

### Phase 3 : Build + Distribution (23 avril → mi-mai 2026)

- F code le MVP (2-3 semaines avec IA)
- R continue la distribution dans les communautés (volume plein)
- F reste actif dans les communautés (30% de son temps)
- Premiers users beta issus de la communauté
- Cold outreach monte en puissance : R à 20-30/jour

### Phase 4 : Scale ou Repeat (mi-mai 2026)

- Si MRR > 0 et croissance → SCALE (plus de volume, plus de canaux)
- Si MRR = 0 après 4 semaines de distribution active → analyse : produit, pricing, ou marché ?
- Si marché mort → REPEAT le loop sur une autre communauté/douleur

---

## 8. MÉTRIQUES

### Métriques d'infiltration (Phase 1)

| Métrique | Seuil minimum/semaine |
|----------|----------------------|
| Interactions dans les communautés (F+R) | 200+ |
| Réponses/commentaires reçus | 50+ |
| DMs reçus organiquement | 5+ |
| Douleurs identifiées et documentées | 10+ |

### Métriques de validation (Phase 2)

| Métrique | Seuil GO |
|----------|----------|
| Signups en 48h | ≥ 10 |
| DMs / questions reçues | ≥ 5 |
| "Combien ça coûte ?" spontané | ≥ 2 |

### Métriques de distribution (Phase 3+)

| Métrique | Seuil minimum/semaine |
|----------|----------------------|
| Cold outreach envoyés (F+R) | 150+ |
| Taux de réponse cold | > 5% |
| Signups | 20+/semaine |
| Trial → Paid | > 5% |
| Interactions communauté maintenues | 200+ |

### Décision KILL vs CONTINUE (à M1 du produit)

| Signal | Action |
|--------|--------|
| 0 signups après 2 semaines de distribution active | KILL le produit, pas la communauté |
| Signups mais 0 conversion payante après M1 | Revoir pricing/gating/valeur |
| > 5 clients payants à M1 | CONTINUE + augmenter le volume |
| MRR > 500€ à M2 | INVEST — les deux doublent le temps dessus |

---

## 9. CE QUI NE CHANGE PAS

- Stack technique : FastAPI + Next.js 14 + Supabase + Stripe + Claude API
- Modèle usine : 1 petit SaaS par mois (mais distribution-first maintenant)
- Budget : ≤ 200€/SaaS
- Modèle de monétisation préféré : Freemium + abonnement
- FoundryTwo reste un studio généraliste
- Le modèle usine reste un search algorithm — on cherche le winner

### Ce qui change

| Avant | Maintenant |
|-------|------------|
| Idée → Build → Chercher où vendre | Communauté → Douleur → Validation → Build → Distribution |
| Cible dev | Cible NON-dev |
| Side project (CDI + freelance) | Full-time |
| Volume cold : 1-2/jour | Volume cold : 30-50/jour (F+R) |
| Twitter build-in-public pour devs | Présence dans les communautés de la CIBLE |
| Documentation d'abord | Action d'abord, documentation minimale |

---

## 10. DÉCISIONS PRISES

| Date | Décision | Rationale |
|------|----------|-----------|
| 03/04/2026 | Pivot distribution-first | 3 semaines LD : 8 signups, 0€ MRR. L'approche build-first ne fonctionne pas sans distribution. |
| 03/04/2026 | Abandon cible dev | Les devs DIY tout. Pire marché pour bootstrap sans crédibilité technique établie. |
| 03/04/2026 | Volume × Constance = non-négociable | Le delta 10x entre plan et exécution sur LD prouve que sans volume, rien ne se valide. |
| 03/04/2026 | Full-time F + R | Chômage = runway limité mais temps illimité. Timer qui tourne = discipline forcée. |
| 03/04/2026 | Validation 48h avant tout build | Plus jamais 4 semaines de code sans preuve de demande du marché. |
