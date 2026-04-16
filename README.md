Entendido. Estás diseñando la **arquitectura de la información** y las reglas del juego. Tu objetivo aquí es crear un estándar que permita a cualquier equipo documentar su aplicativo en 2 días y a cualquier desarrollador nuevo (sin idea de cómo funciona Santander) empezar a trabajar sin bloqueos.

Aquí tienes la propuesta estructurada, dividida entre el nivel general (el SharePoint completo) y el nivel específico (la plantilla de cada aplicativo y sus carpetas).

### Orquestador Prompt
A clean vector illustration diagram showing data flow. On the left side, there are three dark-blue-outlined icons vertically stacked: a bank (classical building), a credit card, and a smartphone, each within a dark circle. Leading from each of these left icons are dark blue solid lines flowing to the center. Positioned on these lines are three stylized folder icons with a subtle blue-to-teal gradient. These lines all converge into a central large circular processor with a dark outline, containing a detailed blue-gradient tree-like circuit board pattern. From the right side of the central processor, two dark blue solid lines flow to the right. The top line leads to a modern building with a list of items and four small circles above it. A single 3D open-box vector wireframe cube is on this line. The bottom line leads to a simple warehouse or factory building with a large door. A cluster of three small open-box wireframe cubes is on this line. The background is clean white.

### Gestor de estatus
Genera la siguiente imagen para el gestor de estatus

Composición y Escala: Una ilustración técnica y plana (flat design) en un estilo vectorial limpio, que representa una arquitectura de tubería de datos (data pipeline). La imagen es limpia, sobre un fondo blanco puro.

Elementos de Entrada (Izquierda): Tres flujos de datos horizontales alineados verticalmente. Cada uno consta de un icono circular y un transportador lineal de datos.



Superior: Un icono de edificio bancario azul oscuro (tipo Partenón). El transportador tiene una caja cúbica verde que se mueve hacia la derecha con una flecha verde.

Medio: Un icono de tarjeta de crédito azul oscuro con banda magnética. El transportador tiene una caja cúbica amarilla que se mueve con una flecha amarilla.

Inferior: Un icono de teléfono inteligente azul oscuro. El transportador tiene una caja cúbica roja que se mueve con una flecha roja.

Los transportadores tienen pequeños rodillos punteados.

Procesador Central (Centro): Un gran contenedor cilíndrico central de color azul oscuro, que sirve como núcleo de procesamiento y almacenamiento.



Está dividido internamente en dos secciones principales.

Sección Superior (Procesamiento): Contiene un icono de base de datos apilada azul oscuro en el centro. A su izquierda, hay una caja cúbica verde con puntos suspensivos que la conectan con la base de datos. A su derecha, hay una caja cúbica amarilla conectada de forma similar. Pequeñas líneas de flujo indican el movimiento entre ellas.

Sección Inferior (Validación/Clasificación): Tres columnas alineadas horizontalmente.

Izquierda (Aprobado): Una pila vertical de tres cajas cúbicas verdes con un icono de marca de verificación verde arriba.

Centro (Pendiente): Una pila vertical de tres cajas cúbicas amarillas con un icono de reloj de arena amarillo arriba.

Derecha (Error): Una pila vertical de tres cajas cúbicas rojas con un icono de signo de exclamación rojo arriba.

La base del cilindro es un pedestal con un panel de control de tres puntos.

Elementos de Salida (Derecha): Dos flujos de datos horizontales alineados verticalmente, que salen del cilindro central hacia nuevos edificios.



Superior: Un transportador de salida que lleva una sola caja cúbica verde. Se dirige hacia un edificio de centro de datos azul oscuro y detallado (con filas de racks de servidores).

Inferior: Un transportador de salida que lleva un pequeño grupo de tres cajas cúbicas rojas. Se dirige hacia un edificio corporativo o de almacén azul oscuro con una gran puerta.

Estilo y Color:

Estilo: Diseño vectorial plano, limpio y de alta precisión. Líneas nítidas y uniformes.

Paleta de colores: Azul marino/oscuro como color principal para los edificios, el cilindro y los transportadores. Unidades de datos codificadas por colores: verde (bueno/procesado/aprobado), amarillo (medio/pendiente/intermedio) y rojo (entrada final/congelado/error).

Las flechas y los iconos de validación (palomilla, reloj, exclamación) utilizan el mismo código de colores que sus respectivas unidades de datos.

Todos los elementos están dispuestos con simetría y lógica visual para mostrar el flujo de izquierda a derecha.

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
