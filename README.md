# 📚 Proyecto_Biblioteca_TopDown_Testing_David_Aceros

<p align="center">
  <img src="https://www.python.org/static/community_logos/python-logo.png" width="300" alt="Python Logo"/>
</p>

This project implements and tests a **Library System** developed in **Python**, using a **Top Down Testing** approach with **stubs** for dependencies like database and authentication.  

---

## 🖥️ Language and Version
- 🐍 **Language:** Python  
- 📌 **Recommended version:** 3.10 or higher  

---

## ⚙️ Installation

1. Clone or download this repository.  
2. Install the required dependencies (only `pytest` is needed):  

```bash
pip install pytest

pytest test_top_down.py -v --tb=short
pytest test_top_down.py::test_prestamo_exitoso -v
pytest -s


proyecto_biblioteca/
│── biblioteca_sistema.py     # Sistema principal
│── test_top_down.py          # Pruebas unitarias con Pytest
└── stubs/                    # Carpeta de stubs
    │── __init__.py           # Hace la carpeta un paquete
    │── database_stub.py      # Stub de base de datos
    └── auth_stub.py          # Stub de autenticación



test_top_down.py::test_prestamo_exitoso PASSED
test_top_down.py::test_usuario_no_autorizado PASSED
test_top_down.py::test_libro_no_disponible PASSED


📝 Fixes and Improvements

🔧 Added __init__.py to stubs/ to make it a package.

🔧 Corrected imports in test_top_down.py.

🔧 Ensured class name is BibliotecaSistema.

🧪 Added missing test for "libro no disponible".

🏃 Executed tests using python -m pytest to avoid import errors.


| Command                      | Description                                |
| ---------------------------- | ------------------------------------------ |
| `pytest`                     | Run all tests                              |
| `pytest -v`                  | Verbose mode (show each test)              |
| `pytest -s`                  | Show `print()` output                      |
| `pytest -x`                  | Stop on first error                        |
| `pytest archivo::funcion -v` | Run a specific test                        |
| `pytest --durations=5`       | Show 5 slowest tests                       |
| `pytest --html=report.html`  | Generate HTML report (needs `pytest-html`) |

