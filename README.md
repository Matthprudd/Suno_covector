# MEYDEN AUDIO CONVERTER

**Version :** v0.2.0, prototype du 6 novembre 2026  
**Site public :** https://meyden-audio-converter.vercel.app  
**Code :** https://github.com/Matthprudd/Suno_covector

Outil de production MEYDEN — Mouvement artistique du Québec.

## Fonctionnalités

1. Coller un lien Suno et ouvrir la page de la chanson pour un téléchargement officiel, si autorisé.
2. Coller un lien direct vers un fichier audio accessible publiquement : importation lorsque le serveur autorise CORS.
3. Importer un fichier audio (WAV, M4A, OGG, MP3, etc. selon le navigateur), convertir en MP3 (128/192/256/320 kb/s) localement, télécharger.
4. **Album des Inconnus** : tenir un registre local de 22 chansons avec lien Suno, artiste, titre, droits déclarés et statut « MP3 reçu ». Export CSV.
5. **Conversion par lots** de fichiers audio autorisés, avec lien de téléchargement pour chaque MP3.

## À savoir

- Un lien de partage Suno ne contient pas un fichier MP3 directement exportable. L'application ne contourne pas les limites de téléchargement, les protections d'accès ou les conditions d'utilisation de Suno.
- Les chansons générées sur un compte Suno gratuit n'ont normalement pas de licence commerciale. Les exporter ou convertir en MP3 n'accorde aucun droit de vente. Pour les chansons déjà créées sur un compte gratuit, obtenir une **permission écrite de Suno** avant de commercialiser un album.
- Même un abonnement pris plus tard ne garantit pas l'attribution rétroactive de droits commerciaux pour les chansons créées gratuitement.
- Les champs « titre » et « artiste » servent au nom des fichiers, pas aux tags ID3.
- Le débit de 320 kb/s n'améliore pas la qualité d'un fichier déjà compressé.
- Les fichiers sont traités localement. La bibliothèque de conversion lamejs est chargée à la demande à partir d'un CDN public.
- Les entrées de l'album sont sauvegardées dans le **stockage local du navigateur** : pas de synchronisation entre téléphones, pas de fichier audio mémorisé sur le serveur, pas de conservation après effacement du stockage navigateur.
- Pour les lots, téléchargez chaque résultat avant de quitter la page.
- Limite de sélection : 150 Mo par fichier; la mémoire disponible sur Android peut imposer des limites inférieures.

## Procédure recommandée pour L'Album des Inconnus

1. Ajouter le lien de chaque chanson au registre (jusqu'à 22).
2. Déclarer la provenance et faire vérifier les autorisations auprès de chaque contributeur.
3. Pour une chanson créée gratuitement sur Suno, contacter Suno à **support@suno.com** afin de solliciter une autorisation commerciale spécifique, ou produire une version originale avec les droits nécessaires.
4. Quand un fichier audio est disponible légalement, le sélectionner dans le convertisseur ou le module de conversion par lots.
5. Exporter le registre en CSV afin de conserver un historique hors du navigateur.
6. Ne pas mettre l'album en vente tant que les droits de toutes les chansons ne sont pas vérifiés.

## Déploiement

Application statique servie depuis `index.html` à la racine. Le dépôt GitHub est lié à Vercel, branche de production `main`. Aucun secret requis.

## État de validation

Déploiement Vercel et syntaxe JavaScript vérifiés. Conversion MP3 sur un vrai téléphone Android et compatibilité de tous les formats **non validées** à ce stade.
