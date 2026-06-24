# QA Testing Project - First Repository

Bienvenido a mi primer proyecto de QA Testing en GitHub. Este repositorio contiene casos de prueba, scripts de automatización y documentación para testing de aplicaciones web y APIs.

## 📋 Contenido del Repositorio

- **test-cases/**: Casos de prueba manuales y documentación
- **scripts/**: Scripts de automatización de pruebas
- **api-testing/**: Pruebas para APIs
- **web-testing/**: Pruebas para aplicaciones web
- **reports/**: Reportes de pruebas y resultados

## 🎯 Propósito

Este proyecto es para:
- 📚 Aprender y practicar QA Testing
- 🤖 Automatizar pruebas con scripts
- 📝 Documentar casos de prueba
- 🐛 Rastrear bugs y defectos
- 📊 Generar reportes de testing

## 🚀 Cómo Empezar

### Requisitos
- Python 3.8+
- pip (gestor de paquetes de Python)
- Git

### Instalación

```bash
# Clonar el repositorio
git clone https://github.com/SantiagoCanese6/first.git
cd first

# Crear un entorno virtual (opcional pero recomendado)
python -m venv venv
source venv/bin/activate  # En Windows: venv\\Scripts\\activate

# Instalar dependencias
pip install -r requirements.txt
```

### Ejecutar Pruebas

```bash
# Ejecutar todos los tests
python -m pytest

# Ejecutar tests con reportes detallados
python -m pytest -v --html=report.html
```

## 📁 Estructura del Proyecto

```
first/
├── README.md                          # Este archivo
├── requirements.txt                   # Dependencias de Python
├── .gitignore                         # Archivos a ignorar en Git
│
├── test-cases/
│   ├── README.md                      # Guía de casos de prueba
│   ├── web-testing-cases.md           # Casos para sitios web
│   └── api-testing-cases.md           # Casos para APIs
│
├── web-testing/
│   ├── test_login.py                  # Ejemplo: pruebas de login
│   ├── test_navigation.py             # Ejemplo: pruebas de navegación
│   └── conftest.py                    # Configuración de pytest
│
├── api-testing/
│   ├── test_api_endpoints.py          # Ejemplo: pruebas de API
│   └── test_api_auth.py               # Ejemplo: pruebas de autenticación
│
├── scripts/
│   ├── run_tests.py                   # Script para ejecutar todas las pruebas
│   └── generate_report.py             # Script para generar reportes
│
└── reports/
    └── test-results.txt               # Reportes de ejecución
```

## 🧪 Tipos de Testing en este Proyecto

### 1. **Manual Testing** (test-cases/)
- Casos de prueba documentados paso a paso
- Checklist de funcionalidades
- Pasos esperados vs. resultados reales

### 2. **Web Testing** (web-testing/)
- Pruebas de interfaz de usuario
- Login y autenticación
- Navegación y flujos de usuario
- Validación de formularios

### 3. **API Testing** (api-testing/)
- Pruebas de endpoints REST
- Validación de respuestas
- Pruebas de autenticación
- Manejo de errores

## 📚 Recursos Útiles

- [GitHub Issues](https://github.com/SantiagoCanese6/first/issues) - Rastrear bugs encontrados
- [GitHub Projects](https://github.com/SantiagoCanese6/first/projects) - Organizar tareas de testing
- [Pytest Docs](https://docs.pytest.org/) - Framework de testing
- [Selenium Docs](https://www.selenium.dev/) - Testing de navegadores

## 🐛 Reportar Bugs

Si encuentras un bug durante testing:

1. Ve a [Issues](https://github.com/SantiagoCanese6/first/issues)
2. Haz clic en "New Issue"
3. Completa:
   - **Título**: Resumen del bug
   - **Descripción**: Pasos para reproducir, resultado esperado, resultado actual
   - **Labels**: Selecciona "bug"

## 📖 Convenciones

- Commits: `git commit -m "test: descripción del cambio"`
- Branches: `git checkout -b feature/nombre-feature`
- Pull Requests: Describe qué pruebas agregaste o mejoraste

## 📞 Contacto

Santiago Canese
GitHub: [@SantiagoCanese6](https://github.com/SantiagoCanese6)

---

¡Happy Testing! 🎉