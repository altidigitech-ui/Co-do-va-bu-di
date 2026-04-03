# Co-do-va-bu-di — Repo distribution-first FoundryTwo

Ce repo gère **uniquement la distribution** (infiltration communautés, contenu, cold outreach, vente).
Le build des SaaS se fait dans des projets Claude séparés. Voir `produits/STATUS.md` pour l'état de chaque produit.

## Structure

```
.
├── CLAUDE.md
├── README.md
├── .claude/commands/
│   ├── bilan-jour.md
│   ├── coach-fabrice.md
│   ├── coach-romain.md
│   └── scoring-idee.md
├── romain/
│   ├── CLAUDE.md
│   ├── plan-30-jours.md
│   ├── semaine-1/
│   │   └── jour-01-lun-06-04.md
│   └── tracking/
│       ├── comptes-groupes.md
│       ├── douleurs-observees.md
│       └── karma-reddit.md
├── fabrice/
│   ├── CLAUDE.md
│   ├── plan-30-jours.md
│   ├── semaine-1/
│   │   └── jour-01-lun-06-04.md
│   └── tracking/
│       ├── comptes-groupes.md
│       ├── douleurs-observees.md
│       └── karma-reddit.md
├── strategie/
│   ├── CONTEXT.md
│   ├── PLAYBOOK-DISTRIBUTION.md
│   ├── WARMING-FARMING.md
│   └── verticals/
│       ├── CONTENT-CREATORS.md
│       ├── ECOMMERCE.md
│       ├── MARKETING-FREELANCERS.md
│       └── RECHERCHE-SCORING.md
├── produits/
│   ├── STATUS.md
│   ├── MUTATIONS.md
│   └── NOUVEAUX.md
└── tracking/
    ├── dashboard-hebdo.md
    └── decisions-log.md
```

## Utilisation

Chaque matin :
- **Romain** : `/project:coach-romain`
- **Fabrice** : `/project:coach-fabrice`

## Slash commands

| Commande | Description |
|----------|-------------|
| `/project:coach-romain` | Plan heure par heure + commentaires prêts à poster (angle growth) |
| `/project:coach-fabrice` | Plan heure par heure + commentaires prêts à poster (angle technique) |
| `/project:bilan-jour` | Bilan du soir : tracking, prévu vs fait, ajustements |
| `/project:scoring-idee` | Évaluer une nouvelle idée SaaS (grille 7 critères + bonus distribution) |

## Build

Voir `produits/STATUS.md` pour le statut de chaque SaaS.
Le build se fait dans des projets Claude séparés (2-5 jours par produit).
