# Politique de confidentialité de Pli

Dernière mise à jour : 24 octobre 2026. Version de l'application examinée : 0.1.0.

## Éditeur et objet

Pli est édité par Nazim Ahres. Cette application Windows permet de réduire la taille d'un PDF, d'examiner l'original et le résultat, puis d'enregistrer une copie. Elle fonctionne sans compte et hors ligne, dès le premier lancement.

## Vos documents

Pli lit uniquement le PDF que vous choisissez ou déposez dans sa fenêtre. Il en crée une copie de travail locale, analyse sa structure, son texte et ses images, puis prépare des rendus d'aperçu et des essais de compression. Le contenu et les métadonnées du PDF peuvent donc être présents dans ces copies temporaires. Pli n'indexe pas vos autres documents et ne recherche pas de fichiers en arrière-plan.

Le PDF d'origine reste intact. L'enregistrement publie une nouvelle copie à l'emplacement choisi par vous. Un fichier existant n'est pas remplacé : Pli utilise un autre nom disponible. Les métadonnées présentes dans le document ne sont pas anonymisées ; vérifiez-les vous-même avant de partager le résultat.

## Données conservées

Pli conserve le thème d'apparence et le niveau de qualité courant dans le fichier `preferences.json` du dossier local de données Pli. Le niveau Équilibré est présélectionné à chaque nouvelle fenêtre. Pli n'enregistre pas d'historique durable des documents, de compte, de coordonnées ou d'identifiant publicitaire.

En version portable, le dossier de données est `%LOCALAPPDATA%\Pli`. Avec l'identité MSIX, Windows peut rediriger ce dossier dans le profil privé du package, sous `%LOCALAPPDATA%\Packages\NazimAhres.Pli_7a846rrbd9ypg\LocalCache\Local\Pli`. Le chemin effectivement retourné par Windows fait foi. Aucun document ni préférence n'est écrit dans le dossier d'installation.

## Fichiers temporaires et durée

Les sessions sont créées dans le sous-dossier `Sessions` du dossier de données Pli. Elles contiennent la copie de travail, les essais, les aperçus PNG et des fichiers JSON de coordination : chemins locaux, réglages, progression, tailles, durées et résultats des vérifications. Ces données restent sur le PC.

Pli supprime sa session lors d'une fermeture normale. Les résultats qui n'ont pas été enregistrés sont alors perdus. Après un arrêt brutal, une coupure ou un blocage, une session peut rester sur le disque ; Pli tente de supprimer les sessions abandonnées et non verrouillées à son prochain lancement. Une erreur de droits ou un verrou peut retarder ce nettoyage. Fermez toutes les fenêtres de Pli avant de supprimer manuellement le dossier de données.

Pendant un export, un fichier de préparation nommé `.pli-export-….tmp` est créé dans le dossier de destination. Il est supprimé après publication ou après un échec géré ; un journal local permet aussi de tenter son nettoyage au prochain lancement après interruption. Les copies que vous enregistrez sont conservées jusqu'à ce que vous les supprimiez vous-même. La suppression effectuée par Pli n'est pas un effacement sécurisé.

## Réseau, collecte et services

Le code applicatif livré n'envoie pas les documents, leurs extraits ou les réglages à Nazim Ahres ou à un service en ligne. Il n'intègre ni publicité, ni mesure d'audience, ni télémétrie, ni rapport de panne distant, ni vérification de mise à jour. Les modules utilisés pour le traitement et l'aperçu sont exécutés localement. Les pages de confidentialité et de mentions dans Pli n'ouvrent pas de contenu distant.

Cette description concerne Pli et les fonctions de ses bibliothèques qu'il utilise. Windows et Microsoft Store peuvent assurer leurs propres services de diagnostic, d'installation ou de mise à jour selon vos paramètres. Les dialogues Windows et les applications externes peuvent conserver leur propre historique. Si vous choisissez un fichier ou un dossier sur un partage réseau ou synchronisé, Windows et votre logiciel de synchronisation peuvent en transférer le contenu. Les actions « Ouvrir le fichier » et « Afficher dans le dossier » confient la copie enregistrée au lecteur PDF ou à l'Explorateur Windows de votre choix.

## Composants tiers

Pli utilise notamment Python, Qt / PySide6 / Shiboken6 pour son interface, pikepdf / qpdf pour la réécriture des PDF, PDFium / pypdfium2 pour l'aperçu et le contrôle du texte, et Pillow pour les images. Leurs licences, versions et sources redistribuées sont décrites dans les mentions légales livrées avec Pli. Aucun de ces composants n'est téléchargé à l'exécution par Pli.

## Vos moyens de contrôle

Vous choisissez le document, le niveau de compression et le dossier d'export. Vous pouvez annuler un traitement, fermer Pli, supprimer vos copies enregistrées ou supprimer les préférences et sessions locales après fermeture. Vous pouvez utiliser Pli sans connexion Internet. Pli n'a pas de compte utilisateur à fermer et aucun document n'est envoyé à l'éditeur par son fonctionnement normal.
