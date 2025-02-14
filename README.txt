##Prise en main
Pour commencer, il vous suffit de compléter le fichier settings.txt avec vos informations.
Voici les paramètres à renseigner :

DISCORD_URL :
L’URL de votre webhook Discord.
Procédure : Serveur > Intégrations > Webhooks > Nouveau Webhook > Choisissez le salon > Sauvegardez > Copiez l’URL et remplacez-la dans DISCORD_URL.

LOGS_FOLDER :
Le chemin complet vers le dossier contenant vos logs arcdps.

MAIN_FOLDER :
Le chemin complet vers le dossier principal (souvent nommé raid) qui contiendra les rapports, les records et d’autres fichiers générés par le script.

TARGET_DATE :
La date ciblée pour l’analyse, au format "YYYY-MM-DD" pour une date précise ou "now" pour la date actuelle.

DISPLAY_RECORDS :
"true" si vous souhaitez que les records individuels des boss s’affichent dans le rapport, sinon "false".

DISPLAY_RESURRECT_TIMERS :
"true" si vous souhaitez afficher les temps totaux de résurrection par joueur, sinon "false".

DISPLAY_TIMERS :
"true" pour afficher les différents temps (temps sur boss, temps sur échecs, etc.), sinon "false".

DISPLAY_CC :
"true" si vous voulez afficher le total de CC infligé par chaque joueur, sinon "false".

SEND_GRAPH_IMAGE :
"true" si vous souhaitez que le graphique (contenant le temps de la soirée par date) soit envoyé dans l’embed Discord, sinon "false".

ATTENTION:
Il est important de respecter la syntaxe avec les guillemets (") dans le fichier de configuration.
Ne les ajoutez pas ou ne les retirez pas si ce n’est pas indiqué.

##Utilisation
- Modifiez le fichier settings.txt pour qu’il corresponde à votre environnement et à vos préférences.
- Exécutez le fichier start script.exe pour lancer le script principal.

Structure du répertoire
La structure de votre dossier principal (par exemple raid/) est la suivante :

graphql
Copier
raid/
├── rapport/         # Contient les rapports générés (fichiers texte)
├── record/          # Stocke les records et données historiques
├── save/            # Dossier temporaire pour sauvegarder les données intermédiaires
├── data/            # Contient le fichier JSON des temps de soirée et le graphique généré
├── settings.txt     # Fichier de configuration
├── start script.exe # Fichier exécutable pour lancer le script
├── __pycache__/     # Dossier contenant les fichiers bytecode Python (générés automatiquement)
1. rapport/
Ce dossier contient des rapports générés par le script. Ces rapports incluent des informations sur les performances du raid, les temps sur boss, les échecs, les transitions, etc.

2. record/
Ce dossier stocke les meilleurs records par boss et par aile (W1 à W8).
Note : Le record pour l'aile W8 est désormais affiché dans l’embed.

3. save/
Ce dossier est utilisé pour sauvegarder temporairement les fichiers JSON générés à partir des logs. Ces fichiers sont ensuite supprimés une fois le rapport envoyé.

4. data/
Contient le fichier evening_times.json qui enregistre, pour chaque semaine (maximum 52 semaines), le temps total de la soirée en secondes.
Contient également le graphique généré (evening_times.png) qui affiche, sur l'axe des x, les dates présentes dans le JSON (au format "jj/mm/aa") et, sur l'axe des y, le temps de la soirée (entre 1h30 et 4h, par incréments de 15 minutes).
5. settings.txt
Fichier de configuration contenant tous les paramètres (voir la section Prise en main).

6. start script.exe
Fichier exécutable pour lancer le script principal.
Assurez-vous que l'environnement nécessaire (Python, modules, etc.) est correctement configuré.

7. __pycache__/
Ce dossier contient les fichiers bytecode Python générés automatiquement pour accélérer le chargement des scripts.

Licence
Ce projet est propriétaire et ne peut être distribué sans autorisation.
