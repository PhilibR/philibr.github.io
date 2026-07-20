# philibr.github.io

Site personnel académique de **F. Philibert Andriniriniaimalaza**, Docteur-Ingénieur,
chercheur postdoctoral à l'ISSTM (Institut Supérieur des Sciences et Technologies de
Mahajanga), Université de Mahajanga, Madagascar.

🔗 **Site en ligne :** [https://philibr.github.io](https://philibr.github.io)

## Aperçu

Site vitrine académique statique : parcours, encadrement doctoral/master, publications,
actualités, galerie photo et contact. Disponible en trois langues (EN / FR / MG).

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
