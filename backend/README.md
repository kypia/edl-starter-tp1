# TaskFlow — Backend

API FastAPI de gestion de tâches. Les tâches sont stockées en mémoire (TP 1 et 2), puis dans PostgreSQL (TP 3).

## Lancer

```bash
uv sync
uv run uvicorn src.app:app --reload
```

- API : <http://localhost:8000>
- Documentation interactive : <http://localhost:8000/docs>

⚠️ Les tâches sont en mémoire : elles disparaissent à chaque redémarrage du serveur.

## Tester

```bash
uv run pytest -v          # tous les tests (avec la couverture)
uv run pytest -k delete   # seulement les tests dont le nom contient « delete »
```

Le rapport de couverture HTML est généré dans `htmlcov/index.html`.

## Fichiers

| Fichier | Contenu |
|---------|---------|
| `src/app.py` | L'API : modèles, stockage, endpoints |
| `tests/conftest.py` | Les fixtures pytest (`client`, nettoyage des tâches) |
| `tests/test_api.py` | Les tests |
| `pyproject.toml` | Dépendances et configuration de pytest |

Les consignes sont dans les TP : `docs/TP-1.md`, `docs/TP-2.md`, `docs/TP-3.md`.
# Test PR
