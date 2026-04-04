# PRINCIPES ANTI-CONCURRENTS — Ce que nos concurrents font mal et qu'on ne fera JAMAIS

Dernière mise à jour : 04/04/2026
Source : 100+ reviews 1★ scrapées (Chargeflow, TrueProfit, Avada SEO, PageFly, AgencyAnalytics)

Ces principes s'appliquent à TOUS les 9 SaaS FoundryTwo. Ils sont non-négociables.

---

## 1. Jamais de modification sans consentement explicite

**Ce que les concurrents font :** Avada modifie le code du theme sans permission. PageFly injecte du code global même sur les pages non utilisées. Chargeflow auto-submit les disputes sans preuves complètes.

**Notre règle :** CHAQUE action qui modifie le store/les données/les campagnes du client nécessite un preview + une approbation explicite. Pas de "on fait ça pour vous en arrière-plan." Le client voit, comprend, et approuve.

**Implémentation :** Modal de confirmation avec diff visuel avant/après. Bouton "Approuver" / "Annuler." Log de toutes les modifications dans un historique accessible.

---

## 2. Zéro résidu à la désinstallation

**Ce que les concurrents font :** Avada laisse des snippets liquid, des sitemaps orphelins, et du JS mort. PageFly laisse du code qui "brique" le site. Les deux forcent le merchant à chercher manuellement les résidus.

**Notre règle :** Si le merchant désinstalle notre app, TOUT notre code est retiré proprement. Aucun résidu. Le store revient à son état pré-installation.

**Implémentation :** Script de cleanup automatique au uninstall. Vérification post-cleanup. Email de confirmation "Votre store a été nettoyé. Aucun résidu de [NomApp]."

---

## 3. Pricing transparent, sans piège

**Ce que les concurrents font :** Chargeflow facture $100 de "vérification" sans prévenir, double-charge $2805, 8% de frais d'annulation. TrueProfit augmente de 400% avec 1 semaine de préavis. Avada facture un plan annuel quand le merchant a sélectionné mensuel.

**Notre règle :** Prix affichés = prix payés. Pas de frais cachés. Pas de frais de vérification. Pas de frais d'annulation. Annulation en 1 clic, instantanée. Si le merchant approche de la limite de son plan → alerte AVANT la facture, pas après.

**Implémentation :** Page pricing claire. Bannière in-app "Vous êtes à X/Y de votre limite. Prochain plan : Z$/mois." Le merchant upgrade QUAND IL VEUT, pas quand on le force.

---

## 4. Données fiables dès le jour 1

**Ce que les concurrents font :** TrueProfit affiche des données fausses (ad spend incorrect, returns mal comptés, LTV incluant les non-acheteurs). AgencyAnalytics admet que "les chiffres ne matchent pas entre plateformes."

**Notre règle :** Au setup, on vérifie nos données vs les sources natives (Shopify, Stripe, Meta, Google). Si écart > 2% → on alerte et on explique le delta. Le merchant fait confiance aux chiffres dès le premier jour.

**Implémentation :** Data Integrity Check au setup. Réconciliation automatique quotidienne. Badge "Données vérifiées" visible dans le dashboard.

---

## 5. L'agent est PROACTIF, pas passif

**Ce que les concurrents font :** AgencyAnalytics montre des dashboards que le client doit interpréter. Chargeflow ne rappelle pas au merchant de soumettre des preuves. TrueProfit ne communique pas les bugs.

**Notre règle :** L'agent AGIT sans qu'on le lui demande. Il alerte, recommande, et propose des actions en 1 clic. Le merchant ne doit JAMAIS checker manuellement si tout va bien — l'agent le fait pour lui.

**Implémentation :** Notifications push (PWA), emails, alertes in-app. Chaque alerte = problème + diagnostic + action recommandée + bouton 1-clic.

---

## 6. Les optimisations appartiennent au merchant

**Ce que les concurrents font :** Avada REVERT toutes les optimisations quand le merchant désinstalle. "Work you do will be reverted upon cancelling — this is a scam."

**Notre règle :** Les optimisations sont pushées DANS la plateforme du merchant (Shopify, Meta, Google). Si le merchant nous quitte, il garde TOUT ce qu'on a fait. Zéro verrouillage.

**Implémentation :** Toute modification = API push vers la plateforme native. Pas de couche intermédiaire qui disparaît à la désinstallation.

---

## 7. Support technique direct

**Ce que les concurrents font :** Avada assigne des agents non-techniques qui "ne savent pas comment l'app fonctionne." PageFly a des agents qui "insultent" les merchants. Chargeflow harcèle les merchants pour qu'ils retirent leurs reviews négatives.

**Notre règle :** Le support répond en <2h. La personne qui répond COMPREND le produit. Pas de layer intermédiaire inutile. Jamais de harcèlement pour les reviews.

**Implémentation :** Support technique direct (pas de tier 1 non-technique). Templates de réponses techniques pré-validées. Escalade automatique si le ticket n'est pas résolu en 24h.

---

## APPLICATION PAR SAAS

| Principe | StoreMD | ListingLab | ChargebackShield | ProfitPilot | AdAudit | ClientPulse | CreatorSuite | LeadQuiz |
|----------|---------|-----------|-----------------|------------|--------|------------|-------------|---------|
| 1. Pas de modif sans consentement | App Risk Monitor, Safe Mode | Safe Mode, preview bulk | Merchant approuve avant soumission | — | — | — | — | — |
| 2. Zéro résidu | Cleanup auto | Cleanup auto | Cleanup auto | Cleanup auto | Cleanup auto | Cleanup auto | Cleanup auto | Cleanup auto |
| 3. Pricing transparent | ✅ | ✅ | Zéro frais cachés, pas de % commission | Alerte avant upgrade | Plan solo 49$ | ✅ | Free tier généreux | ✅ |
| 4. Données fiables | Bot Traffic Filter | — | — | Data Integrity Check | Attribution Cleaner | — | — | — |
| 5. Agent proactif | Alertes régressives, Weekly Report | New Product Watch | Proactive Evidence Reminder | Proactive Bug Alert | Weekly Audit Report | Signaux de churn | Performance Coach | Auto-Optimize |
| 6. Optimisations au merchant | — | Zero Lock-in, push API Shopify | — | — | — | — | — | — |
| 7. Support technique | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
