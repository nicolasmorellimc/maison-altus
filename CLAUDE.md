# Maison Altus — Site vitrine

## Vue d'ensemble
Site vitrine pour **Maison Altus**, studio de design d'intérieur spécialisé dans le style japandi et wabi-sabi.

## Stack technique
- HTML5 / CSS3 / JavaScript vanilla (pas de framework)
- Google Fonts : Cormorant Garamond + Inter
- Site statique, aucun build tool requis
- Compatible avec GitHub Pages, Netlify, Vercel

## Structure du projet
```
maison-altus/
├── index.html              # Page principale (responsive desktop + mobile)
├── site_mobile_version.html # Prototype mobile d'origine (référence)
├── assets/
│   ├── images/             # Toutes les photos de projets (JPG, WEBP, PNG)
│   ├── videos/             # Vidéos de présentation (MP4)
│   └── docs/               # Documents PDF (prestations, projets)
├── CLAUDE.md               # Ce fichier
├── .gitignore
└── README.md
```

## Sections du site
1. **Hero** — Accroche principale avec image en plein écran
2. **Réalisations** — Galerie filtrable (Projets / 3D / Moodboards) avec lightbox
3. **Services** — 4 prestations : Visite Conseil, Plans 2D/3D, Shopping List, Projet Complet
4. **À propos** — Philosophie de design + lien vers PDF prestations
5. **Contact** — Formulaire de prise de contact

## Palette de couleurs
```css
--beige:     #f5f1ed  /* Fond principal */
--vert:      #6b8e6f  /* Couleur accent (sauge) */
--text:      #2c2c2c  /* Texte principal */
--beige-dark:#e8dcc8  /* Beige soutenu */
```

## Conventions de développement
- Tout le CSS est inline dans `<style>` dans `index.html` (single-file)
- Les images sont référencées via `assets/images/nom-fichier.jpg`
- Les fallbacks `onerror` sur les `<img>` affichent un fond dégradé si l'image manque
- La galerie est rendue dynamiquement par JS depuis le tableau `images[]` en bas de page

## Ajouter des photos
Pour ajouter des images à la galerie, éditer le tableau `images` dans `index.html` :
```javascript
{ src: 'assets/images/NOM_FICHIER.jpg', title: 'Titre', desc: 'Description', cat: 'projets' }
// cat: 'projets' | '3d' | 'moodboard'
```

## Déploiement
- **GitHub Pages** : pousser sur `main`, activer Pages sur `/root`
- **Netlify / Vercel** : drag & drop du dossier ou connecter le repo Git
- **Custom domain** : ajouter un fichier `CNAME` à la racine

## TODO / Évolutions possibles
- [ ] Ajouter un vrai backend pour le formulaire de contact (Formspree, Netlify Forms…)
- [ ] Intégrer les vidéos dans une section dédiée
- [ ] Ajouter les métadonnées Open Graph pour le partage social
- [ ] Optimiser les images (WebP, lazy loading déjà en place)
- [ ] Ajouter Google Analytics ou Plausible
