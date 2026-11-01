# order-platform

Plateforme de commandes : projet fil rouge pour construire, déployer et faire évoluer un backend Java de bout en bout (conception, qualité, CI/CD, cloud).

## Objectif

Permettre de gérer le cycle de vie d'une commande : catalogue produits, panier, passage de commande, paiement, suivi et notifications.

Le projet sert de terrain pour :

- structurer une application en architecture hexagonale
- appliquer le trunk-based development et une CI/CD complète
- documenter les choix d'architecture (ADR)
- déployer sur le cloud avec une infrastructure reproductible

## Stack

| Domaine | Choix |
|---|---|
| Langage | Java 21 |
| Framework | Spring Boot 3 |
| Build | Maven |
| Base de données | PostgreSQL |
| Conteneurs | Docker, Docker Compose |
| CI/CD | GitHub Actions |
| Cloud | AWS (à préciser dans un ADR) |

## Prérequis

- JDK 21
- Docker et Docker Compose
- Git

## Lancer le projet

Le code applicatif n'est pas encore initialisé. Cette section sera complétée au fil des itérations.

```bash
git clone https://github.com/<utilisateur>/order-platform.git
cd order-platform
```

Commandes cibles :

```bash
docker compose up -d
./mvnw spring-boot:run
./mvnw verify
```

## Organisation du travail

- Branche `main` protégée : pas de push direct, merge uniquement via pull request
- Trunk-based development : branches courtes (une journée au maximum), une idée par branche
- Nommage des branches : `feat/...`, `fix/...`, `docs/...`, `chore/...`
- Intégration continue obligatoire avant merge
- Historique linéaire (squash merge)

## Feuille de route

- [x] Initialisation du dépôt (licence, .gitignore, README)
- [ ] Protection de `main` et workflow de branches
- [ ] Squelette Spring Boot et premier endpoint
- [ ] Pipeline CI (build + tests)
- [ ] Modèle de domaine et architecture hexagonale
- [ ] Persistance PostgreSQL et migrations
- [ ] Tests automatisés (unitaires et intégration)
- [ ] Conteneurisation
- [ ] Déploiement cloud
- [ ] Observabilité (logs, métriques, traces)

## Décisions d'architecture (ADR)

Les décisions seront consignées dans [`docs/adr`](docs/adr) au fur et à mesure.

| ADR | Sujet | Statut |
|---|---|---|
| ADR-0001 | À venir | - |

## Licence

Distribué sous licence MIT. Voir le fichier [LICENSE](LICENSE).
