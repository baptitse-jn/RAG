Décompresser l'archive :
Trouvez le fichier mon-agent-rag-web_final_pure.zip sur votre ordinateur.
Faites un clic droit dessus et choisissez "Extraire tout..." ou utilisez un outil de décompression pour extraire le contenu dans un dossier de votre choix. Vous obtiendrez un dossier nommé mon-agent-rag-web.
Vérifier l'installation de Python :
Ouvrez un terminal (ou Invite de commandes/PowerShell sur Windows).
Tapez python --version ou python3 --version et appuyez sur Entrée.
Assurez-vous d'avoir une version de Python 3.9 ou supérieure installée. Si ce n'est pas le cas, téléchargez et installez la dernière version depuis python.org .
Ouvrir un terminal dans le dossier du projet :
Naviguez jusqu'au dossier mon-agent-rag-web que vous venez de décompresser en utilisant la commande cd dans votre terminal. Par exemple :
bash
cd chemin/vers/votre/dossier/mon-agent-rag-web
Créer un environnement virtuel :
Dans le terminal, toujours dans le dossier mon-agent-rag-web, exécutez la commande suivante pour créer un environnement virtuel nommé venv :
bash
python -m venv venv 
# ou python3 -m venv venv si 'python' pointe vers Python 2
Activer l'environnement virtuel :
Sur Windows (Invite de commandes/PowerShell) :
bash
.\venv\Scripts\activate
Sur macOS ou Linux (bash/zsh) :
bash
source venv/bin/activate
Une fois activé, vous devriez voir (venv) au début de l'invite de votre terminal.
Installer les dépendances :
Toujours dans le terminal avec l'environnement virtuel activé, installez les bibliothèques Python nécessaires en utilisant le fichier requirements.txt :
bash
pip install -r requirements.txt
Configurer votre clé API Mistral :
Dans le dossier mon-agent-rag-web, créez un nouveau fichier texte nommé exactement .env (attention au point au début).
Ouvrez ce fichier .env avec un éditeur de texte (comme le Bloc-notes, VS Code, Cursor, etc.).
Ajoutez la ligne suivante dans le fichier, en remplaçant VOTRE_CLE_API_MISTRAL_ICI par votre véritable clé API obtenue sur le site de Mistral AI :
MISTRAL_API_KEY=VOTRE_CLE_API_MISTRAL_ICI
Enregistrez et fermez le fichier .env.
Lancer l'application web Flask :
Dans le terminal, toujours avec l'environnement virtuel activé et dans le dossier mon-agent-rag-web, exécutez :
bash
python src/main.py
Vous devriez voir des messages indiquant que le serveur Flask démarre, y compris des lignes comme * Running on http://127.0.0.1:5000.
Accéder à l'application :
Ouvrez votre navigateur web (Chrome, Firefox, etc.) .
Allez à l'adresse : http://127.0.0.1:5000
Vous devriez voir l'interface web de l'agent.
Arrêter l'application :
Pour arrêter le serveur local, retournez dans le terminal où il s'exécute et appuyez sur Ctrl + C.
