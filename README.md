# Balad'Quest — Guide utilisateur

Documentation utilisateur de **Balad'Quest**, l'application web de balades urbaines à étapes.

Site publié : <https://morahk31.github.io/ai-project-parkours-docs/>

Public couvert : visiteurs, membres et contributeurs.

## Travailler en local

Prérequis : Python 3.10 ou plus.

```bash
python -m venv .venv
# Windows : .venv\Scripts\activate    macOS/Linux : source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve
```

Le site est servi sur <http://127.0.0.1:8000> et se recharge à chaque modification.

## Structure

```text
docs/
  index.md            Accueil
  balader/            Faire un parcours (visiteurs et membres)
  compte/             Compte, médailles, vie privée
  contribuer/         Studio contributeur
  faq.md, glossaire.md
  assets/captures/    Captures d'écran de l'application (données de démonstration)
mkdocs.yml            Configuration et menu de navigation
```

Pour ajouter une page : créer le fichier Markdown dans `docs/`, puis l'ajouter à la section `nav` de `mkdocs.yml`.

Les captures mobiles s'insèrent avec `![Texte](chemin.png){ .capture .mobile }`, les captures d'écran large avec `{ .capture .desktop }`.

## Publication

Chaque push sur `main` construit le site (`mkdocs build --strict`) et le publie sur GitHub Pages via GitHub Actions (`.github/workflows/pages.yml`). Les pull requests sont seulement construites, pour détecter les liens cassés.
