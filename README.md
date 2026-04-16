Entendido. Estás diseñando la **arquitectura de la información** y las reglas del juego. Tu objetivo aquí es crear un estándar que permita a cualquier equipo documentar su aplicativo en 2 días y a cualquier desarrollador nuevo (sin idea de cómo funciona Santander) empezar a trabajar sin bloqueos.

Aquí tienes la propuesta estructurada, dividida entre el nivel general (el SharePoint completo) y el nivel específico (la plantilla de cada aplicativo y sus carpetas).

### Orquestador Prompt
A clean vector illustration diagram showing data flow. On the left side, there are three dark-blue-outlined icons vertically stacked: a bank (classical building), a credit card, and a smartphone, each within a dark circle. Leading from each of these left icons are dark blue solid lines flowing to the center. Positioned on these lines are three stylized folder icons with a subtle blue-to-teal gradient. These lines all converge into a central large circular processor with a dark outline, containing a detailed blue-gradient tree-like circuit board pattern. From the right side of the central processor, two dark blue solid lines flow to the right. The top line leads to a modern building with a list of items and four small circles above it. A single 3D open-box vector wireframe cube is on this line. The bottom line leads to a simple warehouse or factory building with a large door. A cluster of three small open-box wireframe cubes is on this line. The background is clean white.

### Gestor de estatus
Genera la siguiente imagen para el gestor de estatus"Una ilustración vectorial de estilo plano e infográfico sobre un fondo blanco limpio, que muestra el flujo de procesamiento de documentos en una base de datos centralizada. La composición central es un gran servidor o base de datos cilíndrica de color azul oscuro, dividida internamente en dos secciones horizontales principales.

A la izquierda de la base de datos, hay tres flujos de entrada de cinta transportadora apilados verticalmente, cada uno con un icono de fuente y una flecha direccional.

Flujo superior: Un icono circular con un símbolo de banco/edificio, una cinta transportadora, un documento verde detallado y una flecha verde que entra en la base de datos.

Flujo central: Un icono circular con un símbolo de tarjeta de crédito/débito, una cinta transportadora, un documento amarillo-marrón detallado y una flecha amarilla-marrón que entra.

Flujo inferior: Un icono circular con un símbolo de teléfono inteligente, una cinta transportadora, un documento rojo detallado y una flecha roja que entra.

La sección superior del cilindro de la base de datos muestra la lógica de procesamiento interno:

A la izquierda, un icono de documento verde.

En el centro, una pila de servidor/CPU azul oscuro estilizada.

A la derecha, un icono de documento amarillo-marrón.

Líneas de conexión de color azul oscuro unen los documentos con el servidor, indicando el análisis o la vinculación.

La sección inferior del cilindro muestra los resultados categorizados en tres columnas distintas con iconos de estado claros arriba de pilas de documentos:

Columna izquierda: Un icono circular azul oscuro con una marca de verificación blanca (check-mark). Debajo hay dos pilas verticales idénticas de ocho iconos de documentos verdes cada una (total 16).

Columna central: Un icono circular azul oscuro con un símbolo de reloj blanco (temporizador). Debajo hay dos pilas verticales idénticas de ocho iconos de documentos amarillos-marrón cada una (total 16).

Columna derecha: Un icono circular azul oscuro con un símbolo de signo de exclamación blanco (!). Debajo hay dos pilas verticales idénticas de ocho iconos de documentos rojos cada una (total 16).

La base de la base de datos es sólida y cuenta con un panel frontal con tres pequeñas aberturas de conexión. El estilo es nítido, limpio y utiliza una paleta de colores coherente: azul oscuro para contornos y estructuras, y verde, amarillo-marrón y rojo para documentos y estados. La perspectiva es frontal y plana."

###
---

### Nivel 1: Estructura General del SharePoint (Página Principal / Home)

Esta es la página de aterrizaje (Landing Page) para todos los que entran al sitio. Debe contener el objetivo y el índice global.

1.  **Objetivo del Sitio (Hero Banner):**
    * *Texto sugerido:* "Bienvenido al Centro de Documentación de [Nombre del Área/Tribu]. Este sitio contiene la estructura, estándares y manuales necesarios para desarrollar, desplegar y mantener nuestros aplicativos dentro del ecosistema Santander. Si eres nuevo, comienza por la sección de Ecosistema y Herramientas."
2.  **Índice de Navegación (Quick Links / Menú Global):**
    * **1. Onboarding y Ecosistema:** (Contexto global, cómo pedir accesos, VPNs, herramientas PCR, reglas de CI/CD, SonarQube).
    * **2. Directorio de Aplicativos:** (Lista de todos los proyectos documentados).
    * **3. Plantillas y Estándares:** (Las plantillas vacías que los equipos deben usar para documentar).
3.  **Estado de Documentación:**
    * Un panel rápido o tabla mostrando el avance de homologación de los aplicativos (ej. App A: 100%, App B: En revisión).

---

### Nivel 2: Estructura de Carpetas (Biblioteca de Documentos)

Para que sea mantenible y escalable, la jerarquía de carpetas en SharePoint no debe ser profunda (máximo 3 niveles). Esto facilita la búsqueda y los permisos.

* 📂 `01_Plantillas_y_Estandares` *(Archivos base para que otros equipos los copien)*
* 📂 `02_Onboarding_Ecosistema` *(KeePass general, manuales PCR, manuales de SonarQube)*
* 📂 `03_Aplicativos`
    * 📂 `[Nombre_del_Aplicativo_A]`
        * 📄 `Readme_Proyecto.docx / .md` *(Documento general si aplica)*
        * 📂 `01_Manuales_Instalacion`
        * 📂 `02_Arquitectura_e_Insumos`
        * 📂 `03_Ambientes` *(Contiene configuraciones por ambiente)*
        * 📂 `04_Fases` *(Documentación evolutiva)*
            * 📂 `Fase_1`
            * 📂 `Fase_2`

---

### Nivel 3: Plantilla Genérica del Aplicativo (Página de SharePoint)

Esta es la plantilla que replicarás (tomando 2 días por app). Cada aplicativo tendrá una página basada en esta estructura.

**Encabezado del Aplicativo**
* Nombre del Aplicativo y Descripción corta de su función en el negocio.
* **Índice de Contenidos (Anclas):** Links rápidos a las secciones de abajo.

**1. Contexto y Arquitectura**
* Diagrama de Arquitectura de alto nivel.
* Stack tecnológico principal.

**2. Manual de Instalación (Enfoque: Cero Contexto Santander)**
*Este es el punto más crítico para los nuevos. Debe estar libre de jerga interna no explicada.*
* **A. Prerrequisitos:**
    * Accesos requeridos (Qué tickets/PCRs levantar y con qué roles).
    * Software a instalar (Versiones exactas de Java, Node, Docker, etc.).
    * Conexiones a red (VPN necesarias).
* **B. Entorno de Desarrollo Local:**
    * Acceso al Repositorio (URL, rama base).
    * Configuración de KeePass (Dónde descargar la bóveda, cómo obtener la llave maestra, cómo leer las variables).
    * Archivo de propiedades locales (`.env`, `application-local.yml`).
* **C. Ejecución de Pruebas y Compilación:**
    * Comandos para levantar el proyecto localmente (ej. `mvn spring-boot:run`).
    * Comandos para correr pruebas unitarias y de integración.
    * Instrucciones para correr el linter o SonarLint local antes del commit.

**3. Mapa de Ambientes (Desarrollo, QA, UAT, Producción)**
*Aquí se resuelve la necesidad de separar por entornos. Utiliza una tabla estructurada para que sea fácil de leer.*

| Ambiente | URL del Aplicativo | URL Base de Datos | Branch (Git) | KeePass de Configuración | Contacto Soporte |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **DEV** | `https://dev-app...` | `jdbc:oracle:.../dev` | `develop` | `[Link al archivo .kdbx]` | Nombre/Equipo |
| **QA** | `https://qa-app...` | `jdbc:oracle:.../qa` | `release/*` | `[Link al archivo .kdbx]` | Equipo QA |
| **PROD** | `https://app...` | `jdbc:oracle:.../prod` | `main` | *(Acceso Restringido)* | Equipo Ops |

**4. Ciclo de Vida CI/CD y Calidad**
* Link al Pipeline.
* Link al Dashboard de SonarQube.
* Reglas para hacer Pull Requests (Aprobadores mínimos, cobertura de código requerida).

**5. Historial y Entregables por Fases**
*Para manejar las Fases 2, 3, 4... usa un control de "Acordeón" (secciones colapsables) o una Lista de SharePoint embebida.*
* **Fase 1 [Completada]:** Descripción del release, enlace a los documentos de análisis de esa fase, endpoints liberados.
* **Fase 2 [En Desarrollo]:** Documento de requerimientos actuales, swagger actualizado.
* **Fase 3 [Backlog]:** Casos de uso futuros.

---

### Estrategia de Ejecución (Tu plan de acción)

Dado que tienes **2 semanas para diseñar y homologar**, y estimas **2 días por aplicativo**, te sugiero este flujo:

1.  **Día 1-2 (Diseño):** Crea la página "Home" en SharePoint y una página vacía que sirva como la "Plantilla Genérica". Configura las listas y tablas vacías.
2.  **Día 3-4 (Prueba Piloto):** Toma el aplicativo que mejor conozcas y llena la plantilla completa. Esto validará si tu estructura funciona o si le sobran/faltan campos.
3.  **Semana 1 y 2 (Auditoría e Implementación):** Empieza con los aplicativos. Al tomar 2 días por aplicativo, enfoca el **Día 1 en el mapeo y recolección** (revisar la documentación existente, identificar los faltantes críticos, entender los entornos). Enfoca el **Día 2 en el vaciado y formateo** dentro de la nueva estructura de SharePoint. Deja marcas claras (como "⚠️ PENDIENTE DE DOCUMENTAR POR EL EQUIPO") donde haya faltantes que tú no puedas llenar.
