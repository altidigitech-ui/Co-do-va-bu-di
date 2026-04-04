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
| Auto-Evidence Builder | Chargeback reçu → l'agent compile le dossier automatiquement (tracking, emails, screenshots, communication client) dans le format Visa/Mastercard. PDF de 10-20 pages en 1 clic. RÈGLE ABSOLUE : le merchant VOIT et APPROUVE le dossier avant soumission. Jamais d'auto-submit aveugle. Notification "Dossier prêt — 12 pages de preuves — approuver ?" | Thread 230 upvotes : "j'ai passé 4h à assembler les preuves. 10+ pages de preuves, et les banques ne les lisent même pas" + Reviews Chargeflow (3+) : "auto submit without key evidence", "submitted before evidence window closed", "they just submit a prompt from ChatGPT and call it a day." |
| Email "menace polie" auto | Dès qu'un chargeback est détecté → email au client : "Nous constatons une opposition... probablement une erreur... les banques facturent des frais pour les oppositions non valides... nous soumettons parfois aux recouvrements." | Thread 230 upvotes : commentaire à 6 upvotes avec template exact validé par la communauté |
| Intégration recouvrement TSI/Rocket | Bouton "Envoyer en recouvrement" en 1 clic. PDF pré-rempli avec toutes les preuves. | Thread 230 upvotes : "on envoie CHAQUE chargeback perdu en recouvrement. TSI récupère chaque centime. Certains paient immédiatement." |
| Plainte IC3 FBI pré-remplie | Formulaire IC3 pré-rempli avec les données de la commande. | Thread 230 upvotes (35 upvotes sur ce commentaire) : "la plupart voudront arranger ça avant qu'une plainte pénale ne soit déposée" |
| Ratio Monitor temps réel | Surveille le ratio en temps réel. Alerte AVANT le seuil 0.9% (Visa) ou 1.0% (Mastercard). | Thread processeurs (81 upvotes) : merchant banni pour 6 chargebacks. "Dépasser 0.9% = amendes 25K-100K$/mois" |
| Blacklist partagée cross-merchants | Base de données partagée des fraudeurs récidivistes (tokenisé). | Thread 230 upvotes (96 upvotes sur ce commentaire) : "une blacklist des rétrofacturations, c'est une super idée" — un dev Shopify a créé une app gratuite pour ça |
| Friendly Fraud Detector | Identifie les patterns : livraison confirmée + aucun contact support + chargeback = friendly fraud. | Thread 230 upvotes : "ils reçoivent le produit, ne contactent JAMAIS le support, et font un chargeback" |
| Billing Descriptor Code | Vérifie que le nom affiché sur le relevé bancaire du client est clair. | Thread chargebacks : certains clients font opposition parce qu'ils ne reconnaissent pas le nom sur leur relevé |
| Payment Processor Health Dashboard | Compare les taux de chargeback par processeur. Suggère un processeur backup. | Thread processeurs : "Stripe est le pire. Amex encore pire. Mastercard/Discover les meilleurs." |
| Revenue Dashboard | Combien sauvé : chargebacks évités + gagnés. ROI visible. Inclut le win rate AVANT vs APRÈS installation. "Avant ChargebackShield : 30% win rate. Après : 72%." | Thread 230 upvotes : "Ce mois : 4800$ sauvés, 1200$ récupérés. ROI abonnement : 60x." + Reviews Chargeflow (4+) : "we lost ALL chargebacks since implementing", "win rate over 6 months still at 0%." |
| Proactive Evidence Reminder | L'agent rappelle au merchant de soumettre des preuves supplémentaires AVANT la deadline. "Deadline dans 48h. Vous avez le tracking mais pas la preuve de communication client — l'ajouter augmenterait vos chances de 35%." | Reviews Chargeflow (3+) : "they don't reach out to remind you to submit additional info", "submitted before evidence window closed so my proof was never included" |
| Business Model Adapter | À l'onboarding, le merchant choisit son type (digital, physique, dropship, abonnement). L'agent adapte sa stratégie de contestation, ses templates de preuves, et ses signaux de risque. | Review Chargeflow : "We have a business model that Chargeflow may not be familiar with" |
| AMEX Risk Alert | Si le client paie avec AMEX → le Pre-Ship Score ajoute un facteur de risque. Notification : "Commande AMEX — risque chargeback élevé historiquement. Recommandation : exiger signature à la livraison." | Thread Reddit 53 upvotes (3 commentaires distincts) : "On ne prend plus AMEX." "Client a admis avoir commandé, admis avoir reçu. AMEX a maintenu le chargeback." "J'ai perdu tous les bénéfices du mois à cause d'un seul chargeback AMEX." |
| Freight Forwarder Detection | Détecte si l'adresse de livraison est un transitaire/réexpéditeur connu. Score risque +30 points. Alerte : "Adresse identifiée comme transitaire. Risque élevé de chargeback 'non reçu'." | Thread Reddit $4200 (125 upvotes) : "On n'envoie plus aux commissionnaires de transport. La plupart du temps, ce sont des arnaques." "Un client canadien a utilisé un centre de réexpédition US pour un article à $4200 puis a fait un chargeback 'non reçu'." |
| Refund vs Contest Calculator | Pour chaque chargeback, l'agent calcule si contester ou rembourser est plus rentable. "Cette commande de 47$ coûterait 85$ à contester (temps + risque de perte). Recommandation : rembourser et blacklister le client." | Thread Reddit 53 upvotes (14 upvotes sur commentaire) : "Si quelqu'un n'est pas content, même s'il est fou, on lui donne une étiquette retour. Ça limite les chargebacks et le gaspillage d'énergie." |
| 3DS Recommender | Pour les commandes à haut risque, recommande d'activer 3D Secure. "3DS transfère la responsabilité du chargeback vers la banque du client. Recommandé pour les commandes > 500$." | Thread Reddit $4200 (1 commentaire) : "Une fois 3DS activé, la responsabilité passe de nous à l'utilisateur si le paiement passe avec 3DS." |

**Pricing :** Free (50 commandes/mois) → 49$/mois (500) → 99$/mois (2000) → 199$/mois (illimité)

### Données marché (sources : Mastercard 2025, Market Clarity, Reddit)

- **TAM global chargebacks :** 33.78 milliards $ drainés des retailers en 2025 (Mastercard)
- **Volume disputes :** 324 millions/an d'ici 2028 (+24% vs 2025)
- **Friendly fraud :** 71% des pertes ne sont PAS de la vraie fraude (Mastercard)
- **Perte moyenne par store :** $800/mois en chargebacks
- **Win rate actuel :** 20%. Potentiel avec IA : 60%
- **Coût réel par chargeback :** 2.6-4.61x le montant de la transaction (produit + shipping + fees + temps)
- **Seuil critique :** 0.65% dispute rate → programme de monitoring Visa. 0.9% → amendes 25-100K$/mois
- **AMEX :** processeur le plus risqué — merchants arrêtent de l'accepter (3+ témoignages Reddit)
- **Transitaires :** risque maximum — "la plupart sont des arnaques" (thread $4200, 125 upvotes)
- **Recouvrement post-chargeback :** "10 clients sur X nous ont rappelés gênés pour payer" (thread 53 upvotes)
- **Un seul chargeback de $4200 peut tuer un small business overnight** (thread 125 upvotes)

Market Clarity recommande un pricing de $99-299/mois pour ce type de produit. Notre pricing ($49-199/mois) est volontairement plus accessible pour capturer les petits merchants.

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
| Data Integrity Check | Au setup, compare les données ProfitPilot vs Shopify vs Stripe. Si écart > 2% → alerte avec explication du delta. Le merchant voit que les chiffres sont fiables dès le jour 1. | Reviews TrueProfit (3+) : "data was all wrong", "wrongly counts ad spend, returns", "their customer metric includes all records regardless of purchase" |
| Proactive Bug Alert | Si l'app a un problème technique → email proactif au merchant AVANT qu'il ne le découvre. "Nous avons un souci avec le sync Meta Ads. Vos données des dernières 4h sont en attente. Résolution estimée : 2h." | Reviews TrueProfit (2+) : "cannot login since few days, no support response", "app has errors all the time" |
| LTV propre | LTV calculée sur les vrais acheteurs uniquement (1+ achats). Filtre explicite clients acheteurs vs tous contacts Shopify. | Review TrueProfit (Yellow Tail Wines) : "their customer metric includes all records regardless of whether that person has made a purchase. Makes LTV reporting unusable." |
| Multi-Fulfillment Sync | Combine automatiquement les coûts de shipping de ShipStation + ShipBob + Shopify Fulfillment quand une commande est splittée entre plusieurs sources. | Reviews Lifetimely (1 review KEUTEK, +4 ans) : "when a shipment is split between ShipStation and ShipBob, the app does not combine shipping costs" |
| Post-Purchase Upsell Tracker | Tracking correct des upsells post-achat. Revenue attribué au produit original + upsell séparément. | Reviews Lifetimely (1 review Koss Design, +1 an) : "not working properly when using a post purchase upsell. Numbers are not relevant at all." |

### Positionnement vs Lifetimely/AMP (concurrent principal Shopify)

Lifetimely (racheté par AMP) = 4.8★ sur Shopify, 468 reviews, mais en chute libre. L'acquisition AMP a dégradé le produit et créé une fenêtre d'opportunité massive.

| Gap Lifetimely/AMP | Ce que ProfitPilot fait mieux |
|-------------------|-----------------------------|
| Données devenues inexactes post-acquisition ("you can disregard all previous positive reviews") | Data Integrity Check au setup + réconciliation quotidienne. Les chiffres sont vérifiés vs Shopify/Stripe. |
| COGS incorrect avec fulfillment multi-source ("shipment split between ShipStation and ShipBob, app does not combine shipping costs") | Support natif multi-fulfillment : ShipStation + ShipBob + Shopify Fulfillment combinés automatiquement. |
| Post-purchase upsells cassent les chiffres ("not working properly with post purchase upsell") | Tracking correct des upsells post-achat. Revenue attribué correctement au produit original + upsell. |
| Focus AMP sur les upsells, plus sur la compta ("focus is more on upsells and additional apps") | ProfitPilot = 100% comptabilité e-com. Pas de feature bloat. Pas de cross-sell d'apps tierces. |
| Plan gratuit mensonger ("says FREE up to 50 orders but you cannot do anything without paying") | Free tier réellement fonctionnel : 50 commandes/mois avec TOUTES les features de base. |
| Support lent ("if I pay 150€/month I expect direct live support") | Support < 2h. Live chat pendant le trial = critique pour la conversion. |
| Pricing en hausse post-acquisition ("new prices are extremely high compared to old ones") | Pricing stable. Garantie 12 mois de prix identique pour les early adopters. |

Le positionnement est clair : Lifetimely a été "enshittified" par AMP. ProfitPilot = l'alternative indie, founder-led, centrée merchant.

**Pricing :** 29$/mois (1 store) → 79$/mois (multi-stores + fiscal) → 149$/mois (prédictions + advisory IA)

### Données marché (sources : Market Clarity, Reddit)

- **Bookkeeping e-com :** 20h/mois de travail DIY = $800/mois de coût d'opportunité
- **Comptable externe :** $500-1,000/mois
- **Déductions manquées :** $5,000/an en moyenne
- **Urgences fiscales :** $3,000 en moyenne
- **Coût annuel total du problème :** $20,000+ par merchant
- **La comptabilité est la frustration #6** sur Reddit/Shopify Community (Market Clarity)
- **Market size :** 2 millions de stores Shopify. TAM estimé à $49/mois × 2M = $98M/an.

Market Clarity recommande un pricing de $49/mois (undercut tout le monde). Notre pricing ($29-149/mois) est aligné avec un entry point encore plus bas.

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
| Integration Health Monitor | Monitoring automatique de chaque connexion API (Meta, Google, etc.). Si une intégration se déconnecte ou retourne des erreurs → alerte proactive : "Votre connexion Meta Ads est cassée depuis 2h. Reconnexion en 1 clic." | Reviews Whatagraph (4+) : "entering month 3 where they are 'working on it', reports unusable", "cannot connect Facebook to any client accounts" |
| Self-Serve Onboarding | L'agent détecte les comptes connectés et configure automatiquement les dashboards/rapports pertinents. En 15 min, pas en 2 mois. | Reviews Whatagraph (2+) : "lead on my team spent 2 months explaining what we needed", "disconnect between sales and implementation team" |

### Positionnement vs AgencyAnalytics (concurrent principal)

AgencyAnalytics = 4.7★ sur G2, 432 reviews, dominant du marché. Mais c'est un OUTIL de dashboards, pas un AGENT. Voici les gaps qu'on exploite :

| Gap AgencyAnalytics | Ce que AdAudit fait mieux |
|--------------------|-----------------------|
| Dashboards PASSIFS — le freelancer doit interpréter les données lui-même | AdAudit DIT quoi faire : "Vous gaspillez 2340$/mois sur 3 audiences. Fusionnez-les." |
| Pas de détection proactive de gaspillage | Waste Detector + Creative Fatigue Alert = l'agent alerte AVANT que le budget ne soit brûlé |
| Chiffres qui ne matchent pas entre plateformes ("hard to explain to customers why numbers differ") | Attribution Cleaner réconcilie Meta vs Google vs CRM |
| Minimum 5 clients obligatoire ($79/mois plan Freelancer) | AdAudit : 1 compte dès 49$/mois. Le freelancer solo ne paie que pour ce qu'il utilise |
| Pas de résumé automatique en langage simple | L'agent génère les insights en phrases, pas en graphiques. "Ce mois : 847$ gaspillés sur 23 termes informationnels." |
| Pas d'alertes proactives | Weekly Audit Report envoyé automatiquement avec les 3 actions prioritaires |

Le positionnement est clair : AgencyAnalytics = "montrez vos données." AdAudit = "sachez quoi faire."

### Positionnement vs Whatagraph (concurrent reporting)

Whatagraph = 4.3★ sur G2, ~278 reviews. Plus faible que AgencyAnalytics, et avec des failles exploitables plus graves.

| Gap Whatagraph | Ce que AdAudit fait mieux |
|--------------|-------------------------|
| Intégrations qui cassent ("entering month 3, they are 'working on it', reports absolutely unusable, cannot connect Facebook") | Monitoring automatique des connexions API. Si une intégration se déconnecte → alerte proactive + reconnexion assistée en 1 clic. |
| Contrats annuels rigides ("switched from quarterly to yearly only, completely inflexible") | Plans mensuels flexibles. Downgrade en 1 clic. Pas de lock-in annuel obligatoire. |
| UI buggée / auth instable ("constant authentication bugs, every interaction requires a refresh") | Interface stable. Pas de re-auth intempestive. Sessions longues. |
| Onboarding catastrophique ("lead on my team spent 2 months explaining what we needed") | Self-service onboarding en 15 min. L'agent configure les dashboards automatiquement basé sur les comptes connectés. |
| Données incomplètes ("not able to fetch purchases, adds to cart") | Toutes les métriques e-com clés dès le launch : purchases, add to cart, ROAS, CPL, CPA. |
| Promesses sales non tenues ("promised functionality that was not there") | Pas de sales team. Self-serve. Ce que tu vois dans le free tier = ce que tu obtiens en payant, en plus grand. |

### Positionnement vs Databox (concurrent dashboards)

Databox = 4.4★ sur G2, 193 reviews. Le plus faible des 3 concurrents reporting (AgencyAnalytics 4.7★, Whatagraph 4.3★, Databox 4.4★).

| Gap Databox | Ce que AdAudit fait mieux |
|------------|-------------------------|
| Templates et métriques qui cassent constamment ("templates always break, individual metrics always break") | Monitoring proactif : si une métrique se déconnecte → alerte + reconnexion automatique. Pas de dashboard cassé silencieux. |
| Bait-and-switch pricing ("bulk of features in top service tiers", "hidden restrictions") | Toutes les features essentielles dans le plan de base. Pas de features cachées. Ce que tu vois dans le free = ce que tu obtiens en payant, en plus grand. |
| Support lent et défensif ("rarely same-DAY service", "always play the victim, can take months to fix a critical issue") | Support < 2h. Ownership des problèmes. Si un bug est signalé → investigation immédiate, pas de blame-shifting. |
| Personnalisation limitée ("not a lot of granular control, metrics come as they are") | Filtres avancés, custom queries, drag-and-drop flexible. L'agent adapte le dashboard au type de campagne. |

**Récap concurrents AdAudit — 3 concurrents scrapés :**
- AgencyAnalytics (4.7★, dominant) : dashboards passifs, pas d'insights, cher pour solo
- Whatagraph (4.3★) : intégrations cassées, contrats rigides, UI buggée
- Databox (4.4★) : templates cassés, bait-and-switch, support défensif

Aucun des 3 ne fait ce qu'AdAudit fait : DIRE quoi faire, pas juste montrer les données.

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
| Export Fiable | Export vidéo/audio garanti fonctionnel. Progress bar honnête. Si erreur → retry automatique + notification. Pas de "0 minutes remaining" qui finit en erreur. | Reviews Descript (3+) : "have NOT ONCE been able to export my video", "downloads take hours on 2GB+ internet", "parts of exported video is blank" + Review Opus Clip : "says 0 minutes left and turns out to be an error" |
| Projets Toujours Accessibles | Les créations du creator lui appartiennent. Échec de paiement → 7 jours de grâce. Projets accessibles en lecture même après expiration du plan. | Reviews Descript (1 review 0★) : "they suspend your access with all your projects after payment failure" |
| Clip Context Guard | L'IA de découpe vérifie que chaque clip contient une idée COMPLÈTE avant de couper. Pas de coupure mid-sentence ou mid-concept. | Reviews Opus Clip (2) : "clips cutting into shorter versions — sometimes context would be cut", "clips get cut off before the idea is finished" |
| Cloud Processing Rapide | Traitement vidéo/audio parallèle cloud-based. Clips extraits en <2 min pour une vidéo de 15 min. Progress bar honnête avec ETA précise. | Reviews Riverside.fm (5+) : "1 minute clip took 20 minutes to export", "2 hour show expected 24 hours to export" + Review Opus Clip : "says 0 minutes left and turns out to be an error" |

**Pricing :** Free (2 vidéos/mois, repurpose basique) → 9$/mois (10 vidéos) → 29$/mois (illimité) → 59$/mois (teams)
**Note :** Pricing volontairement BAS par rapport aux autres SaaS car WTP faible confirmée par le terrain.
**Positionnement prix vs marché :** Les creators utilisent des outils gratuits (CapCut, Canva, etc.). AgencyAnalytics facture $79+/mois. Notre pricing (9-59$) est calibré sur la WTP réelle observée dans les communautés. Le free tier DOIT être généreux pour créer l'habitude.
**Moat :** Faible (outils gratuits nombreux). Différenciateur = l'intégration tout-en-un + l'agent qui optimise en continu.

### Positionnement vs Descript (concurrent principal editing/transcription)

Descript = 4.6★ sur G2, 863 reviews, mais 41 reviews négatives révèlent un produit en dégradation. La fenêtre est ouverte.

| Gap Descript | Ce que CreatorSuite fait mieux |
|------------|------------------------------|
| Bugs chroniques ("so buggy, won't open", "littered with bugs", "treat customers like beta testers" — 15+ reviews) | Stabilité = priorité #1. "It just works." Pas de shipping de features buggées. QA rigoureuse. |
| Transcription qui se dégrade ("used to be 90-95% accurate, now it's worse" — 8+ reviews) | Whisper/Deepgram = qualité constante. Pas de régression. Si la qualité baisse → on switche de provider, pas on ignore. |
| Exports qui échouent ("have NOT ONCE been able to export my video", "downloads take hours" — 3+ reviews) | Export fiable à 100%. C'est le moment de vérité — si l'export plante, tout le workflow est perdu. |
| UI qui change constamment ("over-developed", "constantly change the UI, keystrokes", "step backwards" — 5+ reviews) | UX simple et STABLE. Les changements d'UI sont progressifs. Les workflows existants ne cassent jamais. |
| Pricing confus ("deceptive pricing, charging you twice", "no credit for unused subscriptions" — 5+ reviews) | Pricing simple. Crédits inutilisés reportés au mois suivant. Pro-rata automatique en cas d'upgrade. |
| Support inexistant ("just an AI bot", "suspend access after payment failure" — 5+ reviews) | Support humain accessible. Jamais bloquer l'accès aux projets du user. Les créations du creator lui appartiennent. |
| Projets inaccessibles après problème de paiement | Si le paiement échoue → 7 jours de grâce pour régulariser. Les projets restent accessibles en lecture. |

Le positionnement est clair : Descript essaie de tout faire (editing, transcription, screen recording, podcasting) et fait tout mal. CreatorSuite fait le REPURPOSING et le fait parfaitement.

### Positionnement vs Riverside.fm (concurrent recording/transcription)

Riverside.fm = 4.8★ sur G2, 1676 reviews, mais 26 reviews ≤3★ révèlent des failles critiques.

| Gap Riverside.fm | Ce que CreatorSuite fait mieux |
|-----------------|------------------------------|
| Enregistrements perdus — "alarming 30% chance you won't get the entirety of an interview" (10 reviews) | CreatorSuite ne fait PAS de recording live (pas notre scope). Mais pour le processing post-upload : fiabilité 100%. Backup automatique de chaque fichier uploadé avant traitement. |
| Support IA chatbot frustrant — "impossible to find a human through their AI chatbot", "AI bot support they pretend are real people" (8 reviews) | Support humain réel. Pas de chatbot en première ligne. |
| Exports ultra-lents — "1 minute clip took 20 minutes to export", "2 hour show expected to take 24 hours" (5 reviews) | Processing parallèle cloud-based. Clips extraits en <2 min pour une vidéo de 15 min. |
| Free plan inutile — "free account is completely useless" (5 reviews) | Free tier généreux : 2 vidéos/mois avec repurpose basique. Le creator voit la valeur AVANT de payer. |
| UX confuse — "hard to find stuff I'm working on", "very little guidance on setup" (4 reviews) | Dashboard de projets clair. Onboarding guidé step-by-step. |

**Récap concurrents CreatorSuite — 4 concurrents scrapés :**
- Descript (4.6★, 863 reviews) : bugs chroniques, transcription dégradée, exports cassés, pricing confus
- Riverside.fm (4.8★, 1676 reviews) : enregistrements perdus, support IA, exports lents
- Opus Clip (4.6★, 4 reviews) : clips hors contexte
- Repurpose.io (4.4★, 46 reviews) : 0 reviews négatives — concurrent bien-aimé

La différenciation CreatorSuite = tout-en-un REPURPOSING (pas recording, pas editing lourd). Stable, rapide, et l'agent optimise en continu.

### 6. LEADQUIZ — Voir MUTATIONS.md

**Positionnement vs Octane AI (concurrent Shopify) :** Octane AI = 4.8★, 192 reviews, mais 4 reviews 1★ révèlent : pricing qui explose sans prévenir ($9 → $191/mois), support déficient, setup trop long. LeadQuiz se positionne sur : quiz en 2 min (pas en heures), pricing stable et transparent, multi-langue natif (gap RevenueHunt).

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
| StoreMD (Bot Traffic Filter) | ChargebackShield | "StoreMD bloque les bots et le card testing AVANT. ChargebackShield gère les chargebacks qui passent quand même. Les deux ensemble = protection complète." |

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

---

## DONNÉES REVIEWS CONCURRENTS — Résumé du scraping Shopify App Store + G2

| Concurrent | SaaS cible | Reviews analysées | Patterns clés exploitables |
|-----------|-----------|------------------|--------------------------|
| Chargeflow | ChargebackShield | 20+ × 1★ Shopify | Auto-submit aveugle, frais cachés ($100 vérification, 8% cancellation), win rate PIRE après installation, support zombie, pas d'adaptation par type de business |
| TrueProfit | ProfitPilot | 7 × 1★ Shopify | Données fausses, pricing explosif (+400% sans prévenir), bugs login non communiqués, LTV inclut les non-acheteurs |
| Avada SEO | StoreMD + ListingLab | 40+ × 1★ Shopify | App détruit le store (SEO, collections, images), ralentit au lieu d'accélérer, résidus code après désinstall, images cassées irréversibles, pixel Meta bloqué, lock-in (revert à la désinstall), support non-technique |
| PageFly | StoreMD | 20+ × 1★ Shopify | Code injecté sans permission, pages cassées après updates, résidus massifs après désinstall, duplication de 3000+ pages, demande d'accès données clients, homepage cassée 3x en 1 an |
| AgencyAnalytics | AdAudit | 432 reviews G2 (4.7★) | Dashboard passif (pas d'insights actionnables), intégrations limitées en profondeur, chiffres qui ne matchent pas entre plateformes, cher pour solo (min 5 clients), pas d'alertes proactives, pas de détection de gaspillage |
| NoFraud | ChargebackShield | Pas disponible | — |
| BeProfit | ProfitPilot | Pas disponible | — |
| GoWise | ListingLab | Pas disponible | — |
| Descript | CreatorSuite | 41 reviews ≤3★ G2 | Bugs chroniques (15+), transcription dégradée (8+), pricing confus (5+), support inexistant (5+), exports défaillants (3+), UI instable (5+) |
| Whatagraph | AdAudit | 15 reviews ≤3★ G2 | Intégrations cassées (Facebook, HubSpot), contrats rigides annuels, UI buggée/auth instable, onboarding 2 mois, données incomplètes |
| Lifetimely/AMP | ProfitPilot | 11 reviews 1-2★ Shopify | Données inexactes post-acquisition AMP, COGS multi-fulfillment cassé, support lent, pricing trompeur, dégradation qualité |
| Octane AI | LeadQuiz | 4 reviews 1-2★ Shopify | Pricing explosif ($9→$191 sans prévenir), support déficient, setup complexe |
| Plug In Speed | StoreMD | 2 reviews 1★ Shopify | Casse les sites (modifie fichiers d'autres apps), app non fonctionnelle pendant le trial |
| Opus Clip | CreatorSuite | 1 review G2 | Clips coupés hors contexte (idée incomplète) |
| vidIQ | CreatorSuite | 1 review G2 | Support défaillant, valeur seulement au tier le plus cher |
| Repurpose.io | CreatorSuite | 0 reviews négatives G2 | Concurrent bien-aimé — différenciation par features IA, pas par faiblesses |
| Privy | StoreMD + LeadQuiz | 262 reviews 1-2★ Shopify | Prix abusifs (80+), facturation fantôme post-désinstall (40+), support lent (45+), emails pas envoyés (25+), harcèlement reviews (20+), site ralenti (10+) |
| Shogun | StoreMD | 57 reviews 1-2★ Shopify | Vendor lock-in + prix +300-500% (15), code résiduel impossible à retirer (12), ralentissement site/SEO (10), bugs/instabilité (10) |
| Databox | AdAudit | 11 reviews ≤3★ G2 | Templates/métriques qui cassent (3), bait-and-switch pricing (3), support lent et défensif (3) |
| DashThis | AdAudit | 2 reviews ≤3★ G2 | Données inconsistantes, pricing élevé |
| Riverside.fm | CreatorSuite | 26 reviews ≤3★ G2 | Enregistrements perdus 30% chance (10), support IA chatbot (8), exports ultra-lents (5), free plan inutile (5) |

---

## DONNÉES REDDIT — Threads majeurs scrapés

| Thread | Upvotes | Commentaires | SaaS concerné | Insight clé |
|--------|---------|-------------|---------------|-------------|
| "Comment les chargebacks sont-ils légaux ?" | 53 | 69 | ChargebackShield | Banks incitées à favoriser le client. AMEX pire processeur. Recouvrement fonctionne. Rembourser > contester pour petits montants. |
| "$4,200 chargeback" | 125 | 78 | ChargebackShield | Transitaires = risque max. Données GPS UPS comme preuve. Billing descriptor comme vérification. badbuyerlist.com existe. 3DS shift responsabilité. |
| "Paniers abandonnés BIZARRES et GROS" | 44 | 70 | StoreMD | asdfasdf@asdf.com attaque des centaines de stores. Paniers $700-$100K. Bots sabotent données marketing. Blacklistent domaines email. |
| "Centaines de commandes bots, milliers de faux comptes" | 40 | 48 | StoreMD + ChargebackShield | Card testing massif. Store fermé 2 ans. $25K+ en frais potentiels. Cloudflare + capture manuelle comme défense. |
| "Du trafic mais pas de conversions" | 7 | 45 | StoreMD + LeadQuiz | Mauvais ciblage, site pas optimisé, confiance manquante. Le diagnostic 3 couches de StoreMD résout ça. |

### TOTAL CUMULÉ SCRAPING

| Source | Volume | Concurrents/SaaS |
|--------|--------|-----------------|
| Reddit terrain (sessions précédentes) | 50+ threads, 5000+ commentaires | 8 SaaS validés |
| Reddit threads Market Clarity | 5 threads, 310 commentaires | ChargebackShield, StoreMD, LeadQuiz |
| Reviews Shopify App Store | 400+ reviews 1-2★ | Chargeflow, TrueProfit, Avada, PageFly, Privy, Shogun, Octane AI, Lifetimely, Plug In Speed |
| Reviews G2 | 130+ reviews ≤3★ | AgencyAnalytics, Whatagraph, Databox, DashThis, Descript, Riverside.fm, Opus Clip, vidIQ, Dubsado, HoneyBook |
| Méta-analyses | Market Clarity (milliers de plaintes) + Mastercard 2025 + APPWRK 2026 | Données marché globales |
| **TOTAL** | **55+ threads Reddit + 530+ reviews + données marché** | **18 concurrents analysés** |
