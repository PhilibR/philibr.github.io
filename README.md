# philibr.github.io

Site personnel académique de **F. Philibert Andriniriniaimalaza**, Docteur-Ingénieur,
chercheur postdoctoral à l'ISSTM (Institut Supérieur des Sciences et Technologies de
Mahajanga), Université de Mahajanga, Madagascar.

🔗 **Site en ligne :** [https://philibr.github.io](https://philibr.github.io)

## Aperçu

Site vitrine académique statique : parcours, encadrement doctoral/master, publications,
actualités, galerie photo et contact. Disponible en trois langues (EN / FR / MG).

## Stack technique

Un unique fichier `index.html` (HTML + CSS + JavaScript vanilla, aucune dépendance,
aucune étape de build). Hébergé gratuitement via **GitHub Pages**.

- Pas de framework, pas de bundler — le site s'ouvre et fonctionne tel quel
- Police : [Inter](https://fonts.google.com/specimen/Inter) via Google Fonts (seule ressource externe chargée)
- Multilingue par paramètre d'URL (`?lang=fr`, `?lang=mg`, par défaut `en`) — tout le texte
  est stocké dans un objet de traduction JS et injecté via `data-i18n`
- Recherche interne (filtre les sections de la page, aucune requête réseau)
- Galerie photo avec lightbox par albums (JS pur, sans librairie)
- Diaporama en boucle sur la page d'accueil (CSS + JS, rotation automatique)
- Formulaire de contact : ouvre le client mail de l'utilisateur avec le message pré-rempli
  (`mailto:`) — aucun backend, aucune donnée n'est envoyée à un serveur tiers

## Structure du dépôt

```
index.html                 Page unique (toutes langues, toutes sections)
assets/
  fp-logo-icon.svg          Icône du logo (header)
  icon-512.png               Icône PWA / favicon
  favicon.svg, favicon-16.png, favicon-32.png, apple-touch-icon.png
  banner/                    Photos du diaporama d'accueil (photo-1.jpg … photo-6.jpg)
  contact/                   QR code de contact (contact-qrcode.jpg)
  cv/                        CV téléchargeables (PDF, un par langue)
  gallery/                   Albums photo, un sous-dossier par événement
    isstm-22-et-23/
    coop-operation-smile/
    symposium-maintenance-2026/
    salon-etudiant-2025/
    isstm-2024/
    isstm-2025/
    icecer-2025/
```

## Mettre à jour le contenu

- **Textes** : chercher la clé correspondante (`data-i18n="..."`) dans le HTML, puis mettre
  à jour la même clé dans les trois blocs de traduction (`en`, `fr`, `mg`) en bas du fichier.
- **Photos de la galerie** : déposer les fichiers dans `assets/gallery/<album>/` en respectant
  la numérotation (`-01.jpg`, `-02.jpg`, ...), puis mettre à jour la liste `images: [...]`
  correspondante dans l'objet `albums` du JavaScript si le nombre de photos change.
- **Diaporama d'accueil** : remplacer les fichiers dans `assets/banner/` (mêmes noms,
  format paysage recommandé, ratio homogène entre les 6 photos).
- **Publications** : ajouter une entrée `<li>` dans la liste correspondante (Journal Articles
  ou Conference Papers) de la page Publications.

## Déploiement

Le site est servi directement par **GitHub Pages** depuis la branche principale — aucune
action de build n'est nécessaire. Tout changement poussé sur `main` est publié
automatiquement en 1 à 2 minutes.

```bash
git add .
git commit -m "Update content"
git push
```

## Licence

© 2020–2026 F. Philibert Andriniriniaimalaza. Tous droits réservés — contenu académique
et personnel, non destiné à la réutilisation sans autorisation.
