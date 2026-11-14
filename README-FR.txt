NOVA AI — moteur local GGUF (prototype d'intégration)
=====================================================

CONTENU
- index.html : interface de test du moteur local
- manifest.webmanifest : métadonnées PWA
- sw.js : cache de l'interface

UTILISATION
1. Héberger ces fichiers sur un site HTTPS (par exemple GitHub Pages).
2. Ouvrir l'URL dans Safari.
3. Choisir un fichier .gguf via le bouton d'import.
4. Commencer avec un modèle Q4 très léger (idéalement < 500 Mo), contexte 512/1024.
5. Charger le modèle, puis discuter.

IMPORTANT
- Le moteur utilisé est @wllama/wllama 3.13.0, chargé depuis esm.sh, avec les fichiers WebAssembly servis via le mécanisme CDN du projet.
- La première initialisation nécessite une connexion Internet. L'interface est mise en cache, mais le moteur/WASM et les modèles ne sont PAS garantis hors ligne par ce prototype.
- Le fichier modèle est chargé en mémoire à partir du sélecteur de fichiers; il n'est pas conservé durablement après fermeture/rechargement.
- Ce n'est pas encore le moteur intégré au projet NOVA AI complet : c'est une page autonome de validation.
- Compatibilité iOS/Safari et performance non garanties. L'iPhone SE 2020 (3 Go RAM) peut fermer la page ou échouer avec certains modèles. Ne pas supposer qu'un modèle de 500 Mo consommera seulement 500 Mo de RAM : le runtime, le cache KV et le contexte ajoutent de la mémoire.
- Pour une application hors ligne complète, il faudra embarquer les fichiers WASM, gérer le stockage persistant des modèles (IndexedDB/OPFS selon compatibilité) et tester sur l'appareil.
- Aucun modèle n'est inclus dans ce ZIP.
