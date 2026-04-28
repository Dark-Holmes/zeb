# 🚚 ZEB Platform — Site Web Front-End

> Version HTML/CSS/JS pure — Aucun serveur requis  
> Ouvrir directement dans un navigateur ou via WampServer

---

## 📁 Structure du projet

```
zeb-front/
├── index.html                    ← Page d'accueil publique
├── css/
│   └── style.css                 ← Charte graphique complète ZEB
├── js/
│   └── main.js                   ← JavaScript principal (navbar, chat, filtres...)
└── pages/
    ├── login.html                ← Connexion (avec comptes démo)
    ├── register.html             ← Inscription multi-rôles
    ├── client-dashboard.html     ← Tableau de bord Client
    ├── client-loads.html         ← Liste des demandes client
    ├── client-create-load.html   ← Formulaire nouvelle demande
    ├── client-load-detail.html   ← Détail demande + offres
    ├── transporter-dashboard.html← Tableau de bord Transporteur
    ├── transporter-browse.html   ← Parcourir et filtrer les demandes
    ├── chargeur-dashboard.html   ← Tableau de bord Chargeur
    ├── chargeur-jobs.html        ← Missions de manutention disponibles
    ├── messages.html             ← Messagerie chat temps réel (simulée)
    ├── tracking.html             ← Suivi GPS carte Leaflet (OpenStreetMap)
    ├── admin-dashboard.html      ← Administration (utilisateurs, stats)
    ├── profile.html              ← Profil public + évaluations
    └── 404.html                  ← Page d'erreur
```

---

## 🚀 Comment ouvrir le site

### Option 1 — Directement dans le navigateur (sans serveur)
1. Double-cliquez sur `index.html`
2. Tout fonctionne immédiatement

### Option 2 — Via WampServer (recommandé)
1. Copiez le dossier `zeb-front/` dans `C:\wamp64\www\`
2. Ouvrez `http://localhost/zeb-front/`

### Option 3 — VS Code Live Server
1. Installez l'extension **Live Server** dans VS Code
2. Clic droit sur `index.html` → **Open with Live Server**

---

## 🔐 Comptes de démonstration

Sur la page de connexion, cliquez sur un bouton de démo :

| Rôle | Email | Mot de passe | Redirige vers |
|------|-------|--------------|---------------|
| Client | client@zeb.cm | Demo@1234 | client-dashboard.html |
| Transporteur | transport@zeb.cm | Demo@1234 | transporter-dashboard.html |
| Chargeur | chargeur@zeb.cm | Demo@1234 | chargeur-dashboard.html |
| Admin | admin@zeb.cm | Demo@1234 | admin-dashboard.html |

---

## 🗺️ Plan de navigation complet

```
index.html (Accueil)
  ├── pages/login.html
  │     └── [démo client]     → client-dashboard.html
  │     └── [démo transport]  → transporter-dashboard.html
  │     └── [démo chargeur]   → chargeur-dashboard.html
  │     └── [démo admin]      → admin-dashboard.html
  │
  ├── pages/register.html     → [redirige selon rôle]
  │
  ├── [Espace Client]
  │     ├── client-dashboard.html
  │     ├── client-loads.html
  │     ├── client-create-load.html
  │     └── client-load-detail.html → tracking.html
  │
  ├── [Espace Transporteur]
  │     ├── transporter-dashboard.html
  │     └── transporter-browse.html (filtres + modal offre)
  │
  ├── [Espace Chargeur]
  │     ├── chargeur-dashboard.html
  │     └── chargeur-jobs.html
  │
  ├── messages.html           (chat multi-conversations)
  ├── tracking.html           (carte Leaflet GPS)
  ├── admin-dashboard.html    (onglets : users / demandes / stats)
  ├── profile.html            (profil public + notation)
  └── 404.html
```

---

## 🎨 Charte graphique ZEB

| Couleur | Hex | Usage |
|---------|-----|-------|
| Bleu principal | `#0056A6` | Boutons, logo, titres |
| Orange énergie | `#F47B20` | CTA secondaires, prix, accents |
| Vert confiance | `#4CAF50` | Succès, validation, GPS |
| Fond | `#F9F9F9` | Arrière-plan général |
| Texte | `#333333` | Corps de texte |

**Polices** : Montserrat (titres) + Open Sans (texte)  
**Icônes** : Font Awesome 6.5  
**Carte** : Leaflet.js + OpenStreetMap (gratuit, sans clé API)

---

## ✅ Fonctionnalités interactives

- **Navbar** : responsive, menu burger mobile, dropdown utilisateur, ombre au scroll
- **Connexion** : simulation de login avec redirection par rôle
- **Inscription** : sélecteur de rôle dynamique, indicateur force MDP, panneau latéral animé
- **Filtres** : recherche en temps réel sur les demandes (origine, destination, marchandise, prix)
- **Tri** : tri des demandes (date, prix croissant/décroissant)
- **Chat** : messagerie simulée avec réponses automatiques, emoji, indicateur "en train d'écrire"
- **GPS** : carte Leaflet avec marqueur camion animé, tracé du trajet, simulation de déplacement
- **Offres** : acceptation/refus interactif avec mise à jour visuelle
- **Admin** : onglets, validation/rejet de comptes, recherche utilisateurs
- **Profil** : notation avec étoiles interactives
- **Chargeur** : candidature sur missions avec confirmation
- **Toast notifications** : messages de feedback colorés
- **Animations** : cartes flottantes hero, timeline, transitions

---

## 📱 Responsive

Le site s'adapte à toutes les tailles d'écran :
- **Desktop** (> 960px) : layout multi-colonnes complet
- **Tablette** (640–960px) : layout simplifié, sidebar masquée
- **Mobile** (< 640px) : menu burger, colonnes empilées, touch-friendly

---

*ZEB Platform Frontend v1.0 — HTML / CSS / JavaScript*
