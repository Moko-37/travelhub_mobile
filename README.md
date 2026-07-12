# TravelHub — Application Mobile Voyageur

Application mobile destinée aux **voyageurs** pour rechercher, réserver et suivre leurs voyages sur la plateforme TravelHub.

> Projet de portfolio — Douala, Cameroun

## À propos

TravelHub permet aux voyageurs camerounais de comparer les offres de plusieurs agences, réserver directement, et suivre leur voyage de bout en bout grâce à un carnet de voyage numérique intégré.

## Stack technique

| Composant | Technologie |
|---|---|
| Framework | React Native |
| Navigation | Expo Router |
| Gestion d'état | Redux Toolkit |
| Authentification | OpenID Connect (Keycloak) |

## Fonctionnalités

- **Recherche d'offres** — par destination, dates, budget
- **Réservation directe** — réservation d'une offre publiée par une agence/branche
- **Carnet de voyage** — suivi des étapes, documents liés (billets, vouchers), statut de la réservation
- **Historique des voyages** — réservations passées et en cours
- **Avis** — notation des agences après un voyage

## Prérequis

- Node.js 18+
- Expo CLI (`npx expo`)
- Expo Go (dernière version SDK) pour tester sur mobile, ou un simulateur/émulateur

## Installation

```bash
git clone https://github.com/TON_USERNAME/travelhub-mobile.git
cd travelhub-mobile
npm install
```

## Configuration

Crée un fichier `.env` à la racine :

```env
EXPO_PUBLIC_API_URL=http://localhost:8080
EXPO_PUBLIC_OIDC_AUTHORITY=http://localhost:8180/realms/travelhub
EXPO_PUBLIC_OIDC_CLIENT_ID=travelhub-mobile
```

## Lancer le projet en développement

```bash
npx expo start
```

Scanne le QR code avec l'app **Expo Go**, ou lance sur un émulateur :

```bash
npx expo start --android
npx expo start --ios
```

## Structure du projet

```
app/                # Routes (Expo Router — structure basée sur les fichiers)
├── (auth)/          # Écrans d'authentification
├── (tabs)/          # Navigation principale (recherche, réservations, profil)
components/          # Composants réutilisables
store/               # Redux Toolkit — slices et store
services/             # Appels API vers le backend
```

## Périmètre (MVP)

- Authentification voyageur
- Recherche et réservation d'offres
- Carnet de voyage (étapes, documents, statut)
- Historique des voyages

**Hors périmètre (V2)** : paiement en ligne intégré (Mobile Money), messagerie temps réel, notifications push avancées.

## Auteur

Yvan — Douala, Cameroun