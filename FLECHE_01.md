# FLÈCHE 1 — SaaS EXISTANTS → Adaptation aux verticals non-dev

**Date :** 03 avril 2026
**Objectif :** Mapper les 5 SaaS planifiés sur les douleurs découvertes dans les 3 verticals non-dev
**Verdict rapide :** 2 sur 5 sont adaptables immédiatement. 1 est parfait tel quel. 2 sont à abandonner ou à reporter.

---

## VUE D'ENSEMBLE

| SaaS | Cible originale | Adaptable ? | Nouvelle cible | Effort | Priorité |
|------|----------------|-------------|---------------|--------|----------|
| **Leak Detector** | Devs / SaaS founders | ✅ OUI — pivot fort | Agences marketing + e-commerce | Moyen (repakaging + ajustements) | 🟢 P1 |
| **FicheProduitAI** | E-commerce | ✅ DÉJÀ ALIGNÉ | E-commerce sellers (Shopify/Amazon) | Faible (context.md déjà prêt) | 🟢 P1 |
| **QuizForge** | Education / Formation | ⚠️ PIVOT POSSIBLE | Content creators / coaches | Moyen | 🟡 P2 |
| **PayloadDiff** | DevOps / monitoring | ❌ NON — trop dev | — | — | 🔴 ABANDON |
| **DevToolsAPI** | Développeurs | ❌ NON — trop dev | — | — | 🔴 ABANDON |

---

## 1. LEAK DETECTOR → "STORE AUDIT" (Pivot vers e-com + agences)

### Ce qui existe déjà

Leak Detector scanne une URL et audite 8 catégories de conversion (Headline, CTA, Social Proof, Forms, Visual Hierarchy, Trust, Mobile, Speed) en 60 secondes avec un score /100 et des recommandations actionnables. Le core engine est fonctionnel : Playwright scrape, Claude API analyse, scoring automatique.

### Pourquoi le pivot marche

Le produit fait EXACTEMENT ce dont les e-commerçants et les agences ont besoin — mais il est positionné pour des devs/SaaS founders qui peuvent le faire eux-mêmes. Le même outil, repackagé pour des non-devs, change tout.

### Ce qui change

| Aspect | Avant (dev-focused) | Après (non-dev) |
|--------|---------------------|-----------------|
| **Nom** | Leak Detector | StoreScan / ShopAudit / ConvertCheck (à valider) |
| **Cible** | Indie hackers, SaaS founders | Shopify store owners, marketing freelancers, agences |
| **Message** | "Find what makes visitors leave your landing page" | "Your Shopify store is leaking money — find out where in 60 seconds" |
| **Canaux** | Twitter dev, r/SaaS, IndieHackers | r/shopify, r/ecommerce, Shopify FB Groups, r/digital_marketing |
| **Langue** | Technique (CRO jargon) | Simple ("Your buy button is hard to find", "Customers don't trust your page") |
| **Pricing** | Free 3 audits → Pro 29€ → Agency 99€ | Identique — le pricing est déjà bon |

### Ce qui change techniquement

| Modification | Effort | Impact |
|-------------|--------|--------|
| Ajuster les prompts Claude pour langage non-tech dans les rapports | 2-3 jours | HAUT — les recommandations doivent être "do this" pas "optimize your above-the-fold CTA placement" |
| Ajouter des checks spécifiques Shopify (checkout flow, product page, collection page) | 1 semaine | HAUT — les Shopify stores ont des patterns différents des landing pages SaaS |
| Nouveau landing page + messaging | 2-3 jours | HAUT |
| Intégration Shopify App Store (optionnel V2) | 2-3 semaines | MOYEN — canal de distribution massif mais review process long |

### Double usage : outil de prospection pour agences

L'insight clé : un freelancer marketing peut utiliser cet outil pour **prospecter**. Il scanne le site d'un prospect potentiel → obtient un rapport avec des problèmes concrets → approche le prospect avec "j'ai analysé votre site, voici 5 choses qui vous font perdre des clients" → le prospect est impressionné → le freelancer close le deal.

C'est le modèle que vous avez déjà testé avec le cold outreach Twitter (score + top leaks → reply). Le même modèle, mais pour la cible AGENCES et FREELANCERS au lieu de devs.

### Plan d'action

1. **Semaine 1-2 (pendant le warming)** : Ajuster les prompts pour du langage non-tech. Tester sur 20 Shopify stores.
2. **Semaine 3** : Nouveau landing page + messaging e-com/agence. Proposer des audits gratuits dans les communautés.
3. **Semaine 4** : Validation — 10+ signups en 48h depuis r/shopify ou FB groups → GO scale.

**Time-to-pivot : 2-3 semaines** (le core engine existe, c'est du repackaging).

---

## 2. FICHEPRODUITAI → Parfait tel quel pour l'e-commerce

### Ce qui est planifié

FicheProduitAI analyse et optimise les fiches produit e-commerce avec l'IA : scoring de la qualité du listing, réécriture optimisée SEO, benchmark concurrence, suggestions d'amélioration.

### Pourquoi c'est aligné

La douleur #1 dans les communautés e-commerce est exactement ça. Les merchants Shopify ont des centaines de produits avec des descriptions pauvres, génériques, ou inexistantes. Ils perdent des ventes à cause de listings faibles.

### Paysage concurrentiel analysé

| Outil | Prix | Ce qu'il fait | Ce qu'il ne fait PAS |
|-------|------|---------------|---------------------|
| GoWise | Free + payant | Bulk génération descriptions + SEO | Pas d'analyse/scoring de l'existant |
| SEO On (Avada) | Free + payant | Bulk génération + meta tags | Pas de benchmark concurrence |
| Tako (Hypotenuse) | Payant | Brand voice + auto-pull | Cher, pas de scoring |
| Shopify Magic | Gratuit (inclus) | Descriptions basiques | Très basique, pas de SEO, pas de scoring |
| PageFly | Free + payant | Page builder + descriptions | C'est un page builder, pas un optimiseur |

### Le gap que FicheProduitAI comble

**AUCUN outil ne fait : analyse de l'existant → score → diagnostic des faiblesses → réécriture ciblée → benchmark vs concurrents → suivi dans le temps.**

Tous les outils existants font de la GÉNÉRATION (créer du nouveau). FicheProduitAI fait de l'OPTIMISATION (améliorer l'existant). C'est la différence.

### Plan d'action

1. **Semaine 2-3 du warming** : F commence le build (context.md déjà prêt)
2. **Semaine 3** : Offrir des "free listing audits" dans r/shopify et FB Groups pendant que F code
3. **Semaine 4-5** : MVP live, premiers users beta issus des communautés
4. **Time-to-market : 3-4 semaines**

---

## 3. QUIZFORGE → Pivot possible vers Content Creators / Coaches

### Ce qui est planifié

QuizForge génère des quiz IA + export SCORM pour la formation professionnelle.

### Pivot possible

Les content creators et coaches utilisent des quiz pour :
- **Lead generation** ("Take this quiz to find your [skin type / learning style / business stage]")
- **Engagement audience** (quiz interactifs dans les newsletters/réseaux)
- **Validation de connaissances** dans les cours en ligne

### Verdict

⚠️ **BACKLOG.** Le marché des quiz est compétitif (Typeform, Interact, Outgrow) et le pricing est faible. La vertical content creators a déjà un problème de willingness-to-pay. À revisiter si les 2 premiers produits (Leak Detector pivoté + FicheProduitAI) ne prennent pas.

---

## 4. PAYLOADDIFF et DEVTOOLSAPI → ABANDON pour la stratégie distribution-first

### Pourquoi

- **PayloadDiff** (webhook monitoring) : cible purement dev, niche technique, pas de communauté non-dev active
- **DevToolsAPI** (unified dev API) : idem, B2D avec croissance lente

Ces deux produits violent la règle fondamentale du pivot : **la cible ne doit pas savoir coder.** Les garder dans le pipeline dilue l'énergie. KILL ou DEEP BACKLOG.

---

## SYNTHÈSE — Produits existants adaptés

| Produit | Action | Timeline | Revenue potentiel M6 |
|---------|--------|----------|---------------------|
| **Leak Detector → StoreScan** | Pivot messaging + prompts non-tech + landing page | 2-3 semaines | 2-5K€ MRR |
| **FicheProduitAI** | Build tel que planifié, distribution via communautés e-com | 3-4 semaines | 3-8K€ MRR |
| QuizForge | BACKLOG — revisiter si P1 et P2 ne prennent pas | — | — |
| PayloadDiff | KILL / deep backlog | — | — |
| DevToolsAPI | KILL / deep backlog | — | — |
