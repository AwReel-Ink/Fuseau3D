# Fuseau — CAO légère pour tablette et PC

Fuseau est un modeleur 3D paramétrique léger dans l'esprit de Fusion 360 : esquisses contraintes et cotées, extrusions, congés, chanfreins, réseaux, vue en coupe, export 3MF / STL / STEP et reprise dans Fusion 360 ou FreeCAD.

L'application tient en un seul fichier `index.html`, sans serveur ni compte. Elle fonctionne hors ligne une fois ouverte.

## Mettre en ligne sur GitHub Pages

1. Sur GitHub, créez un nouveau dépôt public, par exemple `fuseau`.
2. Sur la page du dépôt, cliquez **Add file → Upload files**, puis glissez **tout le contenu** de ce dossier : `index.html`, `manifest.webmanifest`, `sw.js`, les icônes, `.nojekyll` et ce fichier. Validez avec **Commit changes**.
   - Le fichier `.nojekyll` est caché sur certains systèmes. S'il manque, ce n'est pas bloquant.
3. Ouvrez **Settings → Pages**. Sous *Build and deployment*, choisissez **Source : Deploy from a branch**, puis la branche **main** et le dossier **/ (root)**. Cliquez **Save**.
4. Au bout d'une à deux minutes, l'adresse s'affiche en haut de la page : `https://<votre-identifiant>.github.io/fuseau/`.

## Installer sur l'iPad

1. Ouvrez l'adresse dans **Safari**.
2. Touchez le bouton **Partager**, puis **Sur l'écran d'accueil**.
3. Fuseau s'ouvre alors en plein écran, comme une application, et fonctionne sans connexion.

Sur PC, Chrome et Edge proposent aussi l'installation, avec l'icône ⊕ dans la barre d'adresse.

## Mettre à jour

Déposez le nouveau `index.html` et le nouveau `sw.js` dans le dépôt, en remplaçant les anciens. La tablette télécharge la mise à jour en arrière-plan et l'utilise au lancement suivant ; fermez puis rouvrez l'application.

## Vos fichiers

- **Projet** : le travail en cours est gardé automatiquement dans l'appareil. Utilisez **Enregistrer** (fichier `.fuseau.json`) pour en garder une copie ou le transférer vers un autre appareil.
- **Impression 3D** : export **3MF** (Bambu Studio, PrusaSlicer, Orca, Cura) ou **STL**. Sur iPad, la feuille de partage permet d'enregistrer dans **Fichiers** ou d'envoyer directement au trancheur.
- **Reprise sur PC** :
  - **Fusion 360** : dans *Utilitaires → Scripts et compléments*, cliquez **+**, choisissez le script `.py` exporté, puis **Exécuter**. La pièce est reconstruite avec ses esquisses, ses cotes modifiables et sa timeline.
  - **FreeCAD** : *Macro → Macros…*, choisissez le fichier `.FCMacro`, puis **Exécuter**. Le résultat est un corps PartDesign avec ses esquisses cotées.

---
Leroy Aurélien - 2026 - Tous droits réservés.
