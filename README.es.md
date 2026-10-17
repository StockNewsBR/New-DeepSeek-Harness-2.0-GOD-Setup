<p align="center">🌐 <strong>Documentación:</strong><br><a href="README.md">🇺🇸 English</a> · <a href="README.pt-BR.md">🇧🇷 Português (Brasil)</a> · <strong>🇪🇸 Español</strong></p>

<div align="center">

# ⚡ DEEPSEEK HARNESS 2.0
## 👑 GOD SETUP — CENTRO DE CONTROL DE INGENIERÍA DE SOFTWARE CON IA

**UN SOLO ESCRITORIO · MEMORIA PERSISTENTE · INTELIGENCIA DE CÓDIGO · ENRUTAMIENTO DE MODELOS · AUTONOMÍA CONTROLADA**

**PENSAR → RECORDAR → COMPRENDER → CONSTRUIR → REVISAR → VERIFICAR → ENTREGAR**

Una alternativa personalizable a las herramientas independientes de programación con IA.

</div>

---

## 🔥 La gran idea

Los asistentes de programación pueden perder contexto entre conversaciones, volver a inspeccionar el mismo repositorio y fragmentar planificación, ejecución, revisión y entrega entre varias herramientas. **DeepSeek Harness 2.0 — GOD SETUP** propone una plataforma integrada: interfaz de escritorio, memoria duradera, selección explícita del entorno de trabajo, grafos del código, revisión especializada, inferencia configurable y operaciones Git auditables.

Su objetivo es **sustituir el flujo de trabajo de diversas herramientas**, no afirmar que supera automáticamente a todos los modelos propietarios. Las ventajas de velocidad, memoria útil y coste deben demostrarse mediante pruebas.

## 🧬 Diagrama completo de arquitectura

\`\`\`mermaid
flowchart TB
    U["👤 Desarrollador"] --> D["🖥️ Harness 2.0 Desktop"]
    D --> R["🧭 Enrutador de proyecto e intención"]
    R --> P["🔐 Permisos y aislamiento"]
    P --> F["♾️ LETTA_ALWAYS_FIRST: memoria antes de inferencia"]
    F <--> L[("Letta: memoria persistente")]
    L <--> N["Memoria global y por entorno"]
    F --> A["Director / Orquestador"]
    A <--> O["OmniRoute: gateway local"]
    O <--> M["DeepSeek: identificador verificado"]
    A <--> G["Graphify: relaciones y dependencias"]
    G <--> S[("Código fuente local")]
    A --> T["Terminal, archivos, Git y pruebas"]
    T <--> S
    A <--> W["Búsqueda web opcional"]
    T --> V["Ponytail: revisión"]
    V --> Q["Pruebas, compilación, lint y seguridad"]
    Q --> C{"¿Verificación correcta?"}
    C -->|"No"| A
    C -->|"Sí"| H{"¿Requiere permiso?"}
    H -->|"Sí"| Z["Autorización humana"]
    Z --> GH["GitHub: commit / push / PR"]
    H -->|"No; operación autorizada"| E["Informe de evidencias"]
    GH --> E
    E --> L
    E --> D
\`\`\`

## 🧩 Diez pilares

| Componente | Función | Beneficio esperado |
|---|---|---|
| Harness Desktop | Control de misiones | Planificar, ejecutar y supervisar |
| Enrutador de contexto | Identificar y aislar entornos | Evitar mezclas entre repositorios |
| Letta | Memoria persistente | Continuidad entre sesiones |
| LETTA_ALWAYS_FIRST | Recuperación previa | Contexto correcto antes del modelo |
| DeepSeek | Razonamiento y código | Planificación, implementación y diagnóstico |
| OmniRoute | Gateway de IA | Enrutamiento configurable |
| Graphify | Grafo del código | Dependencias y análisis de impacto |
| Ponytail | Revisión especializada | Detectar errores y complejidad |
| Herramientas locales | Archivos, shell y pruebas | Cambios verificables |
| GitHub + CI | Versionado y auditoría | Entrega autorizada |

## 🥊 Frente a Claude Code, Cursor y Codex

La propuesta es integrar en un mismo sistema **memoria controlada por el usuario, continuidad entre conversaciones, estructura del código, selección de modelos y costes más transparentes**. No equivale necesariamente a disponer de una ventana de contexto superior ni a ser más rápido que cada competidor.

La comparación debe emplear las mismas tareas y versiones: éxito, latencias medianas y p95, tokens, coste por tarea exitosa, precisión del recuerdo, fallos y necesidad de intervención humana. No presentar superioridad sin resultados medidos.

## ♾️ Memoria antes de la inferencia

Identificar entorno → validar permisos → consultar memoria Letta en el ámbito correcto **antes** del modelo → incluir procedencia y fecha → razonar → verificar archivos/Git actuales → ejecutar y probar → guardar únicamente aprendizajes comprobados.

Memorias recomendadas: **global**, **por entorno** y **temporales por sesión**. Una memoria previa no sustituye la comprobación del código actual. Si falla la recuperación, no seleccionar otra memoria de forma silenciosa.

## 🕸️ Graphify y 🪶 Ponytail

**Graphify** indexa símbolos, importaciones, dependencias y relaciones para analizar el impacto de las modificaciones. Comprueba que el grafo corresponda al HEAD actual: instalado no significa sincronizado.

**Ponytail** puede cuestionar abstracciones innecesarias y revisar errores, seguridad y compatibilidad. Una integración cargada no demuestra que haya revisado un cambio real.

## 🔀 OmniRoute y DeepSeek

El gateway desacopla el escritorio de los proveedores de inferencia. Sus posibilidades de enrutamiento, control de costes y fallback dependen de la instalación concreta. Valida el **ID real del modelo**, las tarifas, los límites, el timeout y el soporte de herramientas.

Configuración **ilustrativa**:

\`\`\`dotenv
AI_BASE_URL=http://127.0.0.1:20128/v1
AI_MODEL=<identificador-verificado>
LETTA_BASE_URL=http://127.0.0.1:<puerto-configurado>
GITHUB_WRITE_REQUIRES_APPROVAL=true
\`\`\`

No publiques contraseñas, tokens, rutas privadas ni exportaciones de memoria.

## 🔁 Ciclo de una misión

1. Identificar el objetivo y el entorno.
2. Recuperar memoria Letta del ámbito correcto.
3. Comprobar la rama, el HEAD, Git status y archivos.
4. Consultar Graphify y las dependencias pertinentes.
5. Planificar un cambio mínimo con criterios de aceptación.
6. Ejecutar herramientas dentro de los permisos aprobados.
7. Revisar el diff con Ponytail, cuando corresponda.
8. Ejecutar pruebas, build, lint y análisis de seguridad.
9. Registrar evidencias; escribir en GitHub solo con autorización.
10. Guardar aprendizajes confirmados en la memoria correcta.

## 📥 Descargas y recursos oficiales

| Herramienta | Enlace |
|---|---|
| Windows + WSL2 | [Microsoft WSL](https://learn.microsoft.com/windows/wsl/install) |
| Git | [git-scm.com](https://git-scm.com/downloads) |
| GitHub CLI | [cli.github.com](https://cli.github.com/) |
| VS Code | [code.visualstudio.com](https://code.visualstudio.com/) |
| Docker | [Docker Desktop](https://docs.docker.com/desktop/) |
| DeepSeek | [Documentación API](https://api-docs.deepseek.com/) |
| Letta | [Docs](https://docs.letta.com/) · [GitHub](https://github.com/letta-ai/letta) |
| NVIDIA NIM opcional | [build.nvidia.com](https://build.nvidia.com/) |
| Graphify | [Buscar repositorios](https://github.com/search?q=graphify&type=repositories) — origen exacto pendiente de verificar |
| Ponytail | [Buscar repositorios](https://github.com/search?q=ponytail&type=repositories) — origen exacto pendiente de verificar |
| OmniRoute | [Buscar repositorios](https://github.com/search?q=omniroute&type=repositories) — origen exacto pendiente de verificar |
| Python | [python.org](https://www.python.org/downloads/) |
| Node.js | [nodejs.org](https://nodejs.org/) |
| pytest | [docs.pytest.org](https://docs.pytest.org/) |
| Playwright | [playwright.dev](https://playwright.dev/) |
| Semgrep | [semgrep.dev](https://semgrep.dev/) |
| Gitleaks | [GitHub](https://github.com/gitleaks/gitleaks) |
| GitHub Actions | [Documentación](https://docs.github.com/en/actions) |
| OpenTelemetry | [opentelemetry.io](https://opentelemetry.io/) |

**Aviso:** este repositorio es una guía de arquitectura; no proporciona un instalador público del Harness homologado.

## 🛠️ Guía de instalación

1. Instalar Windows y WSL2 siguiendo Microsoft.
2. En Linux: \`sudo apt update && sudo apt install -y git curl ca-certificates python3 python3-venv python3-pip\`.
3. Crear directorios de trabajo aislados y proteger los archivos de configuración.
4. Configurar una implementación verificada de OmniRoute y probar el modelo.
5. Instalar Letta y demostrar recuperación tras reiniciar y abrir una conversación nueva.
6. Integrar Graphify y verificar que el índice corresponda al HEAD actual.
7. Integrar Ponytail y comprobar una revisión real de diff.
8. Configurar GitHub con permisos mínimos y aprobación de operaciones de escritura.
9. Ejecutar pruebas completas en un repositorio temporal.
10. Guardar versiones, evidencias y procedimiento de recuperación.

## 🚀 Hoja de ruta GOD-tier

| Prioridad | Mejora | Validación |
|---|---|---|
| P0 | Enrutador seguro de entornos | Pruebas contra contaminación de contexto |
| P0 | Garantizar LETTA_ALWAYS_FIRST | Trazas antes de cada inferencia |
| P0 | Motor de permisos | Rechazos y aprobaciones auditadas |
| P0 | Modelos y timeouts verificados | ID real, latencias p50/p95 |
| P1 | Índice incremental Graphify | Grafo actualizado al HEAD |
| P1 | Revisión Ponytail | Hallazgos en cambios reales |
| P1 | Caché de recuperación | Menos búsquedas y tokens |
| P1 | Búsqueda web documentada | Fuentes, límites y coste |
| P1 | CI y análisis de secretos | Pruebas positivas y negativas |
| P1 | Backups y recuperación | Reinicio y restore comprobados |
| P2 | Especialistas en paralelo | Rendimiento sin conflictos |
| P2 | Observabilidad | Métricas, tokens y trazas |
| P2 | Informes de PR | Evidencias reproducibles |
| P2 | Instalación reproducible | Prueba desde una máquina limpia |
| P2 | Benchmark público | Metodología y resultados verificables |

## ✅ Criterios de aceptación

Para declarar **GOD SETUP homologado** se necesita evidencia de: escritorio tras reiniciar; aislamiento entre entornos; Letta antes del modelo; memoria entre nuevas conversaciones; identidad del modelo; Graphify actualizado y utilizado; Ponytail revisando cambios; build, lint y pruebas; push autorizado a una rama de prueba; búsqueda opcional comprobada; recuperación tras fallos; informes con SHAs, riesgos y resultados.

**Estado:** arquitectura descrita; no existe certificación independiente completa de extremo a extremo en este repositorio.

## 🛡️ Seguridad

No realizar push, merge, deploy, gastos, envíos externos o acciones destructivas sin los permisos correspondientes. Aplicar privilegio mínimo, protección contra inyección de instrucciones y auditoría sin exponer secretos. Pasar pruebas no constituye permiso para desplegar en producción.

---

<div align="center">

### 👑 DEEPSEEK HARNESS 2.0 — GOD SETUP

**Controla el trabajo. Conserva la memoria. Entiende el código. Verifica cada paso. Entrega con permiso.**

Guía de arquitectura · No es un instalador listo · Sin afiliación con proveedores mencionados

### 🤝 Patrocinio / Sponsored by

<a href="https://iamarketmaster.com"><img src="https://raw.githubusercontent.com/StockNewsBR/New-DeepSeek-Harness-2.0-GOD-Setup/main/assets/unnamed.png" alt="Patrocinio AI Market Master y StockNewsBR" width="850"></a>

[AI Market Master](https://iamarketmaster.com) · [StockNewsBR](https://stocknewsbr.com)

</div>
