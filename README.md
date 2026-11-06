# MEYDEN AUDIO CONVERTER

Application officielle de prototypage pour MEYDEN — Mouvement artistique du Québec.

**Site :** https://meyden-audio-converter.vercel.app  
**Dépôt :** https://github.com/Matthprudd/Suno_covector  
**Version :** 0.1.0 (prototype, 2026-11-06)

## Fonctionnalités

- Interface responsive en français (Android et ordinateur).
- Importation d'un fichier audio local (WAV, M4A, OGG, AAC, MP3 et autres formats reconnus par le navigateur).
- Conversion locale en MP3 à 128, 192, 256 ou 320 kb/s via lamejs.
- Préservation d'un MP3 importé, sans réencodage.
- Téléchargement du résultat avec nom de fichier personnalisable.
- Reconnaissance d'un lien de partage Suno et indication de la procédure d'export officielle.
- Importation possible depuis un lien direct vers un fichier audio lorsque le serveur autorise l'accès CORS.

## Limites

Un lien de partage Suno ne constitue pas un fichier MP3 direct. L'application ne contourne ni protections d'accès, ni abonnements, ni quotas, ni droits d'auteur.

Les fichiers choisis sont traités localement par le navigateur; la bibliothèque d'encodage est chargée à la demande depuis un CDN public. La connexion Internet est donc nécessaire pour encoder un fichier non-MP3.

Les champs titre et artiste affectent le nom de sortie, pas les métadonnées ID3. Le 320 kb/s ne rétablit pas la qualité absente du fichier source. Le décodage des formats et les performances varient selon le navigateur et l'appareil; limite de sélection 150 Mo.

## Déploiement

Le projet est un site statique mono-fichier (`index.html` à la racine). Vercel déploie automatiquement les mises à jour de la branche `main`. Aucun secret ou serveur n'est requis.

## Test manuel conseillé

1. Importer un WAV court dont vous disposez des droits.
2. Sélectionner 192 kb/s puis lancer la conversion.
3. Vérifier que le MP3 téléchargé est lisible et que le nom est correct.
4. Tester le même parcours sur Android.
5. Coller un lien de partage Suno, vérifier que le lien ouvre Suno sans prétendre télécharger un MP3 protégé.

**Statut :** prototype à valider sur appareils réels.
