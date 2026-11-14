NOVA AI — PACK PWA DE DÉPART

CONTENU
- index.html : interface NOVA, assistants personnalisables, mémoire par assistant, historique et éditeur HTML.
- manifest.webmanifest : identité de l’application installable.
- sw.js : cache hors ligne de l’interface.
- icon.svg : icône.

IMPORTANT
Cette version est un prototype PWA. Elle ne contient PAS de modèle d’intelligence artificielle. La réponse dans la conversation est une réponse de démonstration. Les données sont enregistrées dans le stockage local du navigateur : effacer les données du site ou changer de navigateur peut les faire perdre.
Le cache hors ligne fonctionne après le premier chargement réussi. L’installation PWA et le service worker nécessitent une adresse HTTPS (ou localhost). Un fichier ouvert directement depuis l’application Fichiers ne suffit pas.

INSTALLATION AVEC UN IPHONE SEUL (HÉBERGEMENT HTTPS REQUIS)
1. Crée un compte GitHub si tu n’en as pas.
2. Dans Safari, crée un nouveau dépôt public nommé nova-ai (github.com → + → New repository).
3. Dans le dépôt, utilise Add file → Upload files et ajoute les fichiers contenus dans ce dossier. Valide avec Commit changes.
4. Dans Settings → Pages, choisis Deploy from a branch, branche main, dossier /(root), puis Save.
5. Attends la publication. Ouvre l’adresse Pages indiquée par GitHub dans Safari.
6. Dans Safari : bouton Partager → Sur l’écran d’accueil → Ajouter.
7. Ouvre NOVA AI depuis sa nouvelle icône une première fois avec Internet pour que l’interface soit mise en cache.

LIMITES MATÉRIELLES
L’iPhone SE 2020 possède une mémoire vive limitée. Un modèle local de langage pourrait être lent, fortement contraint ou ne pas fonctionner dans Safari. Cette PWA ne prétend pas inclure ce moteur. Une vraie app iOS native signée nécessite normalement un environnement de compilation Apple et une signature appropriée.

SÉCURITÉ
N’importe quel code HTML importé peut contenir des scripts. L’aperçu utilise une iframe sandboxée, mais n’importe pas de fichiers inconnus ou non fiables.
