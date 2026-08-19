# 📊 Organigrama e Inventario de Analítica - Savia Salud EPS

Este repositorio contiene el código fuente para el despliegue del **Organigrama Interactivo de Savia Salud EPS**, enfocado en visibilizar el **Inventario de la Coordinación de Analítica y Ciencia del Dato**. 

El proyecto permite navegar por la estructura jerárquica de la entidad y conocer, al hacer clic en cada dependencia, la cantidad de activos de información (Informes de Conexiones, Normativos y Tableros BI) asociados a esa área específica.

🔗 **Enlace de Producción (Vercel):** [https://ti-six-gamma.vercel.app](https://ti-six-gamma.vercel.app)

---

## 🏢 Estructura Organizacional

De acuerdo con el modelo de la entidad, el organigrama abarca los diferentes niveles de gobernanza y operación:

### 1. Órganos de Gobierno y Alta Dirección
*   **Asamblea de Accionistas** y **Revisoría Fiscal**.
*   **Junta Directiva**.
*   **Agente Especial Interventor** (con seguimiento de la Contraloría Delegada).
*   **Gerencia General** (Raíz operativa del organigrama en la web).

### 2. Ramas y Dependencias Operativas
A partir de la Gerencia General, la aplicación desglosa las siguientes ramas en un formato de árbol vertical:

*   **Staff de Gerencia:** Secretaría General, Direcciones (Auditoría Interna, Calidad y Planeación), Jefaturas (Comunicaciones, Defensa Judicial, Contratación), Oficial de Cumplimiento y Coordinación Jurídica.
*   **Subgerencia de Salud:** Desglosa áreas vitales como la Dirección de Acceso a Servicios, Dirección de Riesgo en Salud, Jefatura de Autorizaciones, Centro Regulador, Cuentas Médicas, Atención al Usuario, Auditoría Concurrente, Apoyo a Regiones y diversas coordinaciones (Epidemiología, Salud Pública, Alto Costo, Programas Especiales).
*   **Subgerencia Financiera:** Dirección de Contabilidad y Presupuesto, Dirección de Tesorería y Cartera.
*   **Subgerencia Administrativa:** Jefaturas de Gestión Humana, Administrativa, Aseguramiento de Recursos/Operaciones, y la **Dirección de Tecnología e Información** (donde se aloja la Coordinación de Analítica y Ciencia del Dato, Soporte, e Infraestructura).

---

## 🚀 Características Principales

1. **Diseño en Árbol Vertical (Directorio):** Estructura jerárquica de arriba hacia abajo y con indentación lateral, optimizada para facilitar la lectura y el *scroll* en cualquier dispositivo, incluyendo teléfonos móviles.
2. **Interactividad (Modal Dinámico):** Al hacer clic en cualquier área/nodo del organigrama, se despliega una ventana emergente (modal) que detalla los activos de datos del área.
3. **Datos Pre-cargados (Estáticos):** La información de los inventarios (Informes, Normativos y Tableros de BI) ha sido inyectada estáticamente en los atributos HTML (`data-informes`, `data-normativos`, `data-bi`) provenientes del maestro en Excel (Hoja "SP"). Esto elimina tiempos de carga y latencia con APIs externas.
4. **Despliegue Rápido en Vercel:** Integración continua a través de GitHub, garantizando un despliegue sin configuraciones complejas de backend.

---

## 🛠️ Tecnologías Utilizadas

*   **HTML5:** Estructuración semántica de nodos y niveles organizacionales.
*   **CSS3:** Variables nativas (`:root`), Flexbox, y pseudo-elementos (`::before`, `::after`) para crear las líneas conectoras del árbol sin necesidad de librerías de gráficos (como D3.js o GoJS), haciéndolo muy liviano.
*   **Vanilla JavaScript (ES6):** Manejo del DOM para los eventos de clic y la apertura/cierre de los modales informativos. No requiere frameworks externos.

---

## 💻 Ejecución Local

Para visualizar este proyecto de manera local, no se requiere la instalación de dependencias o servidores Node.js complejos:

1. Clona este repositorio:
   ```bash
   git clone [https://github.com/TU_USUARIO/TU_REPOSITORIO.git](https://github.com/TU_USUARIO/TU_REPOSITORIO.git)
