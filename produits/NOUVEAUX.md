# NOUVEAUX SaaS — Créés from scratch

Dernière mise à jour : 04/04/2026
Même architecture commune que MUTATIONS.md (Agent 4 couches + PWA).
Source : 50+ threads Reddit (5000+ commentaires) + recherche web

---

## MOIS 1 — E-COMMERCE

### 1. CHARGEBACKSHIELD — Bouclier anti-fraude prédictif (Score 35/41)

**Cible :** E-commerce Shopify | **Problème :** 10K$/an (800$/mois chargebacks)
**Validation terrain :** 7+ threads, 1000+ commentaires — LE sujet le plus douloureux de l'e-com

Un merchant passe 4 HEURES PAR JOUR sur les chargebacks. 200-1000 commandes/jour, 2-4 chargebacks quotidiens, tous infondés. "J'ai passé 4h aujourd'hui juste à gérer les rétrofacturations. C'est du temps que je devrais utiliser pour développer mon business." Un autre a perdu son business de 15 ans à cause des chargebacks. Un merchant à 25K€/mois s'est fait bannir par Stripe pour 6 chargebacks. Stat Mastercard : 75% des chargebacks sont de la "fraude amicale."

| Feature | Ce que l'agent fait | Validation terrain |
|---------|-------------------|--------------------|
| Pre-Ship Score | Score risque 0-100 par commande AVANT expédition. Cross-order pattern detection (même adresse, même IP, mêmes produits sur plusieurs commandes). | Thread 230 upvotes : "les clients ne nous contactent même pas, ils appuient sur le bouton 'contestation' de leur appli bancaire" |
| Smart Hold | Commandes >75% risque → attente auto. Commandes safe → passent sans friction. | Thread 230 upvotes : "les commandes à faible risque de Shopify passent mais on a quand même des chargebacks" |
| Auto-Evidence Builder | Chargeback reçu → l'agent compile le dossier automatiquement (tracking, emails, screenshots, communication client) dans le format Visa/Mastercard. PDF de 10-20 pages en 1 clic. | Thread 230 upvotes : "j'ai passé 4h à assembler les preuves. 10+ pages de preuves, et les banques ne les lisent même pas" |
| Email "menace polie" auto | Dès qu'un chargeback est détecté → email au client : "Nous constatons une opposition... probablement une erreur... les banques facturent des frais pour les oppositions non valides... nous soumettons parfois aux recouvrements." | Thread 230 upvotes : commentaire à 6 upvotes avec template exact validé par la communauté |
| Intégration recouvrement TSI/Rocket | Bouton "Envoyer en recouvrement" en 1 clic. PDF pré-rempli avec toutes les preuves. | Thread 230 upvotes : "on envoie CHAQUE chargeback perdu en recouvrement. TSI récupère chaque centime. Certains paient immédiatement." |
| Plainte IC3 FBI pré-remplie | Formulaire IC3 pré-rempli avec les données de la commande. | Thread 230 upvotes (35 upvotes sur ce commentaire) : "la plupart voudront arranger ça avant qu'une plainte pénale ne soit déposée" |
| Ratio Monitor temps réel | Surveille le ratio en temps réel. Alerte AVANT le seuil 0.9% (Visa) ou 1.0% (Mastercard). | Thread processeurs (81 upvotes) : merchant banni pour 6 chargebacks. "Dépasser 0.9% = amendes 25K-100K$/mois" |
| Blacklist partagée cross-merchants | Base de données partagée des fraudeurs récidivistes (tokenisé). | Thread 230 upvotes (96 upvotes sur ce commentaire) : "une blacklist des rétrofacturations, c'est une super idée" — un dev Shopify a créé une app gratuite pour ça |
| Friendly Fraud Detector | Identifie les patterns : livraison confirmée + aucun contact support + chargeback = friendly fraud. | Thread 230 upvotes : "ils reçoivent le produit, ne contactent JAMAIS le support, et font un chargeback" |
| Billing Descriptor Code | Vérifie que le nom affiché sur le relevé bancaire du client est clair. | Thread chargebacks : certains clients font opposition parce qu'ils ne reconnaissent pas le nom sur leur relevé |
| Payment Processor Health Dashboard | Compare les taux de chargeback par processeur. Suggère un processeur backup. | Thread processeurs : "Stripe est le pire. Amex encore pire. Mastercard/Discover les meilleurs." |
| Revenue Dashboard | Combien sauvé : chargebacks évités + gagnés. ROI visible. | Thread 230 upvotes : "Ce mois : 4800$ sauvés, 1200$ récupérés. ROI abonnement : 60x." |

**Pricing :** Free (50 commandes/mois) → 49$/mois (500) → 99$/mois (2000) → 199$/mois (illimité)
**Moat :** Data ML + network effect (blacklist partagée) + intégration recouvrement unique

---

## MOIS 2 — AGENCES + E-COM RENFORCÉ

### 2. CLIENTPULSE — Le cerveau IA du freelancer (Score 36/41)

**Cible :** Agences/Freelancers marketing | **Problème :** 15-25K$/an (6 outils + 20h/sem non-productif)
**Validation terrain :** 6+ threads, 400+ commentaires (agences, reporting, workflow, finances freelance)

Un freelancer a construit TOUT le marketing d'une entreprise (0→2.2M$ en 18 mois) et a gagné 25K$ de profit. "J'ai construit un canal d'acquisition de plusieurs millions et j'ai gagné moins qu'un employé de McDonald's." La plainte #1 identifiée sur 527 threads tagués : "je ne peux pas prouver que ça fonctionne." Les freelancers jonglent entre 6-8 outils, passent 15-20h/semaine sur des tâches non-productives, et sont "6 mois de retard sur leurs comptes."

| Module | Ce que l'agent fait | Validation terrain |
|--------|-------------------|--------------------|
| PROSPECT | Scanne le site d'un prospect → mini-audit CRO/SEO 60 sec → message d'approche personnalisé. | Thread agence toiture (193 upvotes) : "j'ai regardé 1200 pubs vidéo de couvreurs pour trouver ce qui marche" |
| PROPOSE | Brief en 3 phrases → proposal complète en 2 min. Calcul ROI pour le client. Pricing recommandé basé sur les résultats. | Thread agence : le freelancer ne sait pas comment facturer — forfait, % du CA, % des profits ? |
| DELIVER | Kanban par client. Deadlines, livrables, suivi révisions, approbations. L'agent alerte : "Client X n'a pas répondu depuis 7 jours." | Thread quotidien (10 upvotes) : "je jongle entre les affaires des clients. La moitié du temps je me fais tirer dans des urgences" |
| REPORT | Connecte GA4 + Meta Ads + Google Ads → rapport mensuel 1 clic avec insights IA en phrases. White-label PDF. | Thread 527 fils tagués : "je ne peux pas prouver que ça fonctionne" est la plainte #1 |
| BILL | Factures auto-générées basées sur les livrables validés. Suivi paiements. Relances J+7, J+14, J+30 automatiques. | Thread finances freelance (27 upvotes) : "6 mois de retard sur mes comptes." "Le plus dur : garder mon argent organisé" |
| RETAIN | Détecte signaux de churn : client qui ouvre moins les rapports, résultats qui stagnent. Suggère upsells au bon moment. | Thread agence : "le goulot d'étranglement actuel est la conversion des ventes — 90.7% des devis non convertis" |

**Pricing :** Free (2 clients) → 29$/mois (5 clients) → 79$/mois (15 clients) → 149$/mois (illimité, white-label)
**Moat :** Data clients + historique + templates = switching cost massif après 6 mois

### 3. PROFITPILOT — Comptabilité e-com IA (Score 33/41)

**Cible :** E-commerce | **Problème :** 20K$/an (15-20h/mois compta + erreurs)
**Validation terrain :** 5+ threads, 200+ commentaires (marges, comptabilité, retours, attribution, tarifs)

"Bienvenue dans le e-commerce où tout le monde parle de revenus et personne ne parle de ce qu'il garde vraiment." Un merchant avec AOV de 85$ découvre 20$+ de coûts cachés par commande. Un autre dépense 9000$/mois en ads "mais aucune idée de quelle plateforme génère de vrais bénéfices après COGS." Un merchant a vu ses coûts augmenter de 7$/unité du jour au lendemain à cause des tarifs douaniers.

| Feature | Ce que l'agent fait | Validation terrain |
|---------|-------------------|--------------------|
| True Profit par produit | Profit RÉEL temps réel : revenue - COGS - shipping - ads - fees Shopify - returns. | Thread AOV (134 upvotes) : "j'ai 85$ d'AOV mais 20$+ de coûts avant le COGS" |
| App Cost Allocator | Répartit le coût de chaque app PAR COMMANDE, pas juste par mois. | Thread AOV : "4-5$/commande en abonnements apps — un tueur silencieux" |
| Daily P&L | Mis à jour quotidiennement. "Hier : 847$ revenue, 203$ profit réel (24% marge)." | Thread AOV : "la plupart des gens ne font pas ce calcul avant qu'il ne soit trop tard" |
| Margin Alerts | Alerte quand COGS augmente ou marge descend sous seuil. | Thread tarifs (37 upvotes) : "mon coût a augmenté de 7$/unité du jour au lendemain" |
| Ad Spend Tracker | Profit réel par source (Meta vs Google vs organique). | Thread attribution (36 upvotes) : "le ROAS ne dit pas le profit réel après COGS et shipping" |
| Return Cost Calculator | Coût RÉEL d'un retour : shipping retour + manutention + stock mort + temps. | Thread RTO (5 upvotes, 27 commentaires) : "l'impact des RTO est un casse-tête — bataille manuelle constante avec des CSV" |
| OPEX Categorizer | Catégorisation automatique des dépenses opérationnelles (apps, VA, shipping, ads). | Thread VA (111 upvotes) : "les dépenses du VA se mélangent avec les coûts généraux" |
| Tax Ready | Catégorisation auto. Rapport fiscal 1 clic. Détection déductions manquées. | Thread comptabilité (5 upvotes) : merchants utilisent Excel et "n'ont même pas besoin de QuickBooks" |
| Cashflow Forecast | Prédit le cashflow 30/60/90 jours. | Thread RTO : "les fondateurs D2C sont obsédés par le CAC et le ROAS mais ignorent la logistique inverse" |

**Pricing :** 29$/mois (1 store) → 79$/mois (multi-stores + fiscal) → 149$/mois (prédictions + advisory IA)
**Moat :** Data financières accumulées + intégrations Shopify/Stripe/Meta/Google = irremplaçable après 3 mois

### 4. ADAUDIT — Auditeur publicitaire IA (Score 30/41)

**Cible :** Agences marketing + merchants D2C | **Problème :** 12K$+/an budget ads gaspillé
**Validation terrain :** 5+ threads, 500+ commentaires (Google Ads CPL, SEO, outils IA marketing)

"Les mêmes campagnes, les mêmes mots-clés. Juste plus cher." Un client HVAC à 15K$/mois est passé de 180$ à 105$/lead en nettoyant les négatifs. Un dev a un cron job toutes les 20 min avec 11K négatifs. "C'est comme le jeu du whack-a-mole." Selon Gartner, l'industrie du marketing digital a un taux d'approbation de 20%.

| Feature | Ce que l'agent fait | Validation terrain |
|---------|-------------------|--------------------|
| Wasted Spend Detector | Identifie automatiquement le gaspillage : termes informationnels, bots, placements pourris, audiences chevauchées. | Thread Google Ads (141 upvotes) : "tu paies 40-80$ par clic pour des gens qui n'ont aucune intention de t'embaucher" |
| Negative Keyword Agent | Suggestions auto de négatifs basées sur les termes de recherche, mises à jour en continu. L'agent fait le whack-a-mole pour toi. | Thread Google Ads : un dev a un cron job avec 11K négatifs. "Il faut continuer chaque semaine" |
| True ROAS Calculator | Profit réel par plateforme après COGS/shipping/fees. (Cross-sell avec ProfitPilot.) | Thread attribution (36 upvotes) : "Facebook affiche un ROAS décent, Google un ROAS correct, mais ça ne dit pas le profit réel" |
| Agency Scorecard | Note les performances de ton agence/freelancer sur des métriques concrètes. | Thread SEO (214 upvotes) : "seulement 2 sur 50 experts pouvaient montrer de vrais classements" — les clients se font arnaquer |
| Creative Fatigue Alert | Détecte quand un ad perd en performance (CTR en baisse progressive). | Thread outils IA (92 upvotes) : "les outils qui essaient de remplacer la pensée humaine échouent" |
| Attribution Cleaner | Réconcilie les données cross-plateforme (Meta vs Google vs CRM). | Thread quotidien : "Facebook dit 40 conversions, Meta dit 52, mon CRM dit 90" |
| Weekly Audit Report | Rapport hebdomadaire auto : "Cette semaine, 847$ gaspillés sur 23 termes informationnels. 3 recommandations." | Thread quotidien : "je vérifie les performances des annonces en premier, je réalise qu'il y a quelque chose à corriger" |
| Multi-account | 10+ comptes publicitaires clients depuis un seul dashboard. | Thread agence toiture : le freelancer gère tout pour 1 client, imagine 5-10 |

**Pricing :** 49$/mois (1 compte) → 149$/mois (10 comptes) → 299$/mois (illimité)
**Moat :** Negative Keyword Agent s'améliore avec le temps + data cross-comptes

---

## MOIS 3 — CREATORS + CROSS-SELL

### 5. CREATORSUITE — Studio IA tout-en-un (Score 31/41)

**Cible :** Content Creators YouTube/TikTok/Podcast | **Problème :** 1.6K$/an outils + 15h/sem non-créatif
**Validation terrain :** 8+ threads, 2800+ upvotes (workflow, outils, burn-out, multi-plateforme)
**⚠️ ALERTE WTP :** La willingness-to-pay est basse. Les creators cherchent du GRATUIT. Pricing agressif ou freemium large obligatoire.

"Le burn-out sur YouTube, ce n'est pas un manque de discipline, c'est un workflow de merde." (2.3K upvotes). Les creators utilisent 5-10 outils séparés. "J'ai cramé deux fois et failli arrêter YouTube." Le repurposing prend 4-6h par épisode — la plupart ne le font pas et laissent 80% de la valeur de leur contenu sur la table.

| Module | Ce que l'agent fait | Validation terrain |
|--------|-------------------|--------------------|
| Auto-Transcribe | Vidéo/audio → transcription (Whisper/Deepgram). Timestamps, speakers, chapitres. | Thread outils (2.3K upvotes) : les creators utilisent Krisp pour la transcription |
| Repurpose Engine | Transcription → 5 tweets, 3 posts LinkedIn, 1 newsletter, 10 citations. Ton adapté par plateforme. 1 vidéo → 20+ contenus en 2 min. | Thread multi-plateforme (8 upvotes) : "c'est pas juste uploader, y'a les Shorts, les posts communauté, repurposer des extraits" |
| Clip Detector + Cutter | Identifie les 3-5 meilleurs moments pour Shorts/Reels. Extraction auto avec captions, format vertical. | Thread burn-out (175 upvotes) : "trouver des extraits c'est facile, c'est l'enfer du redimensionnement" |
| Audio Cleaner | Nettoyage audio auto (bruit, écho) en 1 clic avant publication. | Thread outils : "la qualité audio était nulle jusqu'à Auphonic. 2h gratuites/mois" |
| Thumbnail Manager | Upload + miniature custom en un seul workflow. Contourne la limitation YouTube (pas de custom thumbnail pour Shorts uploadés depuis PC). | Thread miniatures (25 upvotes, 61 commentaires) : "YouTube ne permet pas de choisir une miniature custom depuis le PC" |
| Title Optimizer | 5 variantes basées sur keywords YouTube + analyse des titres qui performent dans la niche. | Thread croissance (72 upvotes) : "des miniatures colorées = un CTR plus élevé" |
| Content Calendar | Deadlines, batch mode, rappels. | Thread multi-plateforme : "certaines semaines je fais du batch, d'autres semaines je poste quand je m'en souviens" |
| Performance Coach | "Cette semaine : meilleure vidéo, pourquoi, quoi reproduire." | Thread 1000 abonnés (79 upvotes) : creator ne sait pas quelle direction prendre |
| Content Theft Alert | Détecte si d'autres chaînes volent/re-uploadent tes vidéos. | Thread monétisation refusée : un musicien à 27K abonnés découvre que 3 chaînes volent ses shorts |
| Smart Schedule | Poste sur toutes les plateformes au meilleur horaire. | Thread multi-plateforme : "poster frénétiquement à 3h du matin" |

**Pricing :** Free (2 vidéos/mois, repurpose basique) → 9$/mois (10 vidéos) → 29$/mois (illimité) → 59$/mois (teams)
**Note :** Pricing volontairement BAS par rapport aux autres SaaS car WTP faible confirmée par le terrain.
**Moat :** Faible (outils gratuits nombreux). Différenciateur = l'intégration tout-en-un + l'agent qui optimise en continu.

### 6. LEADQUIZ — Voir MUTATIONS.md

### 7. [WILDCARD] — Issu des douleurs communautés (Mois 3)

Identifié pendant les mois 1-2 via douleurs-observees.md de R et F. Critères : problème observé 5+ fois, willingness-to-pay confirmée, aucune solution existante satisfaisante.

---

## CROSS-SELL MATRIX COMPLÈTE

| Si le client utilise | On propose | Pitch |
|---------------------|-----------|-------|
| StoreMD | ListingLab | "Store healthy mais listings faibles" |
| ListingLab | StoreMD | "Listings top mais store a des problèmes" |
| StoreMD + ListingLab | ChargebackShield | "Vous convertissez, protégez vos revenus" |
| ChargebackShield | ProfitPilot | "Vous bloquez la fraude, connaissez votre vrai profit" |
| ProfitPilot | AdAudit | "Vous connaissez votre profit, optimisez vos ads" |
| ClientPulse | AdAudit | "Vous gérez vos clients, optimisez leurs ads" |
| AdAudit | ClientPulse | "Vous auditez les ads, gérez tout le cycle" |
| CreatorSuite | LeadQuiz | "Vous repurposez, capturez des leads" |
| StoreMD (App Impact) | ProfitPilot (App Cost) | "StoreMD montre l'impact technique, ProfitPilot montre le coût financier de chaque app" |

**Bundle e-com :** StoreMD + ListingLab + ChargebackShield + ProfitPilot = 199$/mois (vs 316$)
**Bundle agence :** ClientPulse + AdAudit = 179$/mois (vs 228$)

---

## DONNÉES TERRAIN — Résumé du scraping

| SaaS | Threads scrapés | Upvotes total | Commentaires | Niveau de validation |
|------|----------------|---------------|-------------|---------------------|
| ChargebackShield | 7+ | 500+ | 1000+ | ✅✅✅ NUCLÉAIRE |
| StoreMD | 8+ | 300+ | 500+ | ✅✅✅ BÉTON |
| AdAudit | 5+ | 600+ | 500+ | ✅✅✅ BÉTON |
| ProfitPilot | 5+ | 250+ | 200+ | ✅✅ SOLIDE |
| ClientPulse | 6+ | 500+ | 400+ | ✅✅ SOLIDE |
| ListingLab | 4+ | 30+ | 100+ | ✅✅ SOLIDE |
| LeadQuiz | 1 | 9 | 20 | ✅ VALIDÉ |
| CreatorSuite | 8+ | 2800+ | 400+ | ✅✅ (mais WTP basse ⚠️) |

Les features marquées "Validation terrain" dans chaque tableau ont été confirmées par des vrais utilisateurs sur Reddit avec des douleurs chiffrées et des cas concrets.
