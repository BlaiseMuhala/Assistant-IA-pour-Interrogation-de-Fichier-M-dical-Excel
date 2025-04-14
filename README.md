# Assistant-IA-pour-Interrogation-de-Fichier-M-dical-Excel

Un assistant interactif conçu pour répondre à des questions médicales en langage naturel à partir d’un fichier Excel structuré.
🧑‍💻 Auteur : Blaise MUHALA

🎯 Objectif
Ce projet démontre comment utiliser l’API GPT-4 d’OpenAI pour interagir avec des données médicales contenues dans un fichier Excel. L’utilisateur peut poser une question (ex : Quels sont les traitements du paludisme ?) et obtenir une réponse intelligente directement extraite des données.

🛠️ Technologies utilisées
Python 3.8+

Bibliothèques :

openai

pandas

openpyxl

API utilisée : OpenAI GPT-4

🚀 Fonctionnement du script
Génère automatiquement un fichier data.xlsx contenant un tableau médical fictif.

Lit ce fichier et le convertit en texte.

Envoie une question de l’utilisateur + les données au modèle GPT.

Affiche une réponse claire basée uniquement sur les données du fichier Excel.

📁 Structure du projet
bash
Copier
Modifier
/medbot/
├── main.py          # Script principal
├── data.xlsx        # Fichier généré automatiquement (maladies, symptômes, traitements)
└── README.md        # Fichier d’explication
▶️ Exemple de question
text
Copier
Modifier
Quels sont les symptômes du paludisme ?
Réponse attendue de l’IA :

Les symptômes du paludisme sont : fièvre, frissons.

🧪 Lancer le script
Ouvre ton terminal

Exécute le script :

bash
Copier
Modifier
python main.py
Saisis une question comme :

text
Copier
Modifier
Quels sont les traitements pour la grippe ?
L’IA te répond en analysant le fichier data.xlsx.

📦 Installation des dépendances
Avant de lancer, installe les bibliothèques nécessaires :

bash
Copier
Modifier
pip install openai pandas openpyxl
🔒 Attention à la clé API
N’oublie pas de remplacer ta clé API personnelle dans le fichier main.py :

python
Copier
Modifier
client = openai.OpenAI(api_key="ta-clé-api-ici")
💡 Améliorations futures (TODO)
Ajouter une interface graphique (ex : avec Flask ou Tkinter)

Permettre l’upload de fichiers Excel personnalisés

Ajouter un historique des questions

Ajouter la traduction multilingue

Intégration avec des données médicales réelles (avec contrôle qualité)

🗃️ Historique
v1.0 – Version console fonctionnelle avec données fictives

À venir – Version web ou API REST

🖋️ Rédigé par Blaise MUHALA – Libre à l’usage et à l’amélioration
