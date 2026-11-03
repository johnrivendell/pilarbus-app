# 🚌 PilarBus - Ecosistema Móvil de Transporte Público

Proyecto desarrollado para la asignatura *Fundamentos del desarrollo del software y metodologías ágiles* - **Universidad Nacional de Pilar (UNP) 2026**.

## 📌 Control de Versiones y Flujo de Trabajo (Git Flow)
Para mantener la estabilidad de la aplicación móvil y la plataforma web, el equipo utiliza el siguiente esquema de ramas:
* **`main`**: Rama principal con el código estable desplegado en producción.
* **`develop`**: Rama de integración donde se agrupan las funcionalidades terminadas.
* **`feature/...`**: Ramas de características individuales creadas por cada integrante para cada tarjeta de Trello (ej. `feature/gps-tracking`, `feature/sube-integration`).

### Uso de Pull Requests (PR)
Ningún código sube de forma directa a producción:
* Se abre un **Pull Request (PR)** desde la rama `feature` hacia `develop` o `main`.
* Requiere revisión de código (*Code Review*) obligatoria por parte de otro compañero del equipo.

## 🔄 Integración y Entrega Continua (CI/CD)
El repositorio cuenta con automatización mediante **GitHub Actions** (`.github/workflows/ci-cd.yml`):
1. **Build y Test Automático:** Ante cada Pull Request, el sistema compila la app y ejecuta pruebas unitarias para validar que no haya errores.
2. **Despliegue Continuo (Deploy):** Al hacer *merge* a la rama `main`, la plataforma se actualiza automáticamente en la nube sin interrumpir el servicio para los pasajeros.
