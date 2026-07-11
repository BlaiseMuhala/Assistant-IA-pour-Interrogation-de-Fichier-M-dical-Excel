# Assistant IA pour interroger un fichier médical Excel

Petit projet perso pour poser des questions en langage naturel sur un fichier Excel médical, et obtenir une réponse basée uniquement sur ces données.

Auteur : Blaise MUHALA

## L’idée

On a un tableau Excel (maladies, symptômes, traitements). Au lieu de chercher à la main, on pose une question comme « Quels sont les traitements du paludisme ? » et GPT-4 répond à partir du contenu du fichier.

Rien de plus : pas d’invention hors tableau, juste une lecture intelligente des données.

## Stack

- Python 3.8+
- `openai`, `pandas`, `openpyxl`
- API OpenAI (GPT-4)

## Comment ça marche

1. Le script crée un `data.xlsx` avec quelques lignes d’exemple.
2. Il lit le fichier et le transforme en texte.
3. Il envoie ta question + ces données à GPT-4.
4. Tu reçois une réponse claire, calée sur le tableau.

## Structure

```
/medbot/
├── main.py      # script principal
├── data.xlsx    # généré au lancement (maladies, symptômes, traitements)
└── README.md
```

## Exemple

Question :

```
Quels sont les symptômes du paludisme ?
```

Réponse typique :

```
Les symptômes du paludisme sont : fièvre, frissons.
```

## Installation

```bash
pip install openai pandas openpyxl
```

## Lancer

```bash
python main.py
```

Ensuite, tape ta question, par exemple :

```
Quels sont les traitements pour la grippe ?
```

L’IA répond en s’appuyant sur `data.xlsx`.

## Clé API

Dans `main.py`, remplace la clé par la tienne :

```python
client = openai.OpenAI(api_key="ta-clé-api-ici")
```

Sans ça, rien ne tourne.

## Idées pour la suite

- Une vraie interface (Flask ou Tkinter)
- Pouvoir uploader son propre Excel
- Garder un historique des questions
- Support multilingue
- Brancher des données médicales réelles (avec un vrai contrôle qualité)

## Versions

- **v1.0** — console, données fictives, ça marche
- À venir — version web ou API REST

---

Blaise MUHALA — libre d’usage et d’amélioration.
