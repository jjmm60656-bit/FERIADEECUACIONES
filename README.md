# FERIA DE ECUACIONES
# ⚗️ Simulador Hidráulico — Ecuaciones Diferenciales

Aplicación web interactiva para la simulación de sistemas hidráulicos basados en ecuaciones diferenciales ordinarias de primer orden, desarrollada para la **Feria Facultativa FICCT 1/2026** de la Universidad Autónoma Gabriel René Moreno.

> **Área:** Matemáticas Aplicadas  
> **Categoría:** Nivel Intermedio  
> **Asignatura:** Ecuaciones Diferenciales

---

## 📋 ¿Qué hace esta aplicación?

El simulador permite modelar el comportamiento del nivel de líquido en tanques con diferentes configuraciones:

- **Tanque simple** — Vaciado por gravedad (Ley de Torricelli).
- **Con bomba** — Entrada constante de caudal.
- **Doble tanque** — Dos tanques en serie.
- **Interconexión** — Flujo bidireccional entre tanques.

### Funcionalidades principales

- Resolución numérica mediante **Runge‑Kutta de 4° orden (RK4)**.
- Solución analítica para el caso de tanque simple.
- Visualización en tiempo real del sistema hidráulico (canvas interactivo).
- Gráficas dinámicas de **altura h(t)**, **caudal Q(t)**, **potencia P(t)** y **energía E(t)**.
- Tabla de resultados numéricos.
- Generación de **reportes en PDF** con carátula institucional, ecuaciones, gráficas y conclusiones.
- Exportación del código **LaTeX** del reporte.
- Modo **animación** para observar la evolución temporal.
- Soporte para **tema oscuro/claro**.

---

## 🗂️ Estructura del proyecto
Simulador_Hidraulico/
├── index.html ← Aplicación completa (HTML + CSS + JavaScript)
├── escudo.png ← Logo de la FICCT (opcional)
└── README.md ← Este archivo

> **Nota:** Todo el código está contenido en un único archivo `index.html`. No requiere instalación de dependencias adicionales (se cargan desde CDN: Chart.js, MathJax, jsPDF, html2canvas).

---

## ▶️ Cómo ejecutar la aplicación

1. Descarga el archivo `index.html` y el logo `escudo.png` (opcional).
2. Abre el archivo `index.html` en tu navegador web (Chrome, Firefox, Edge, etc.).
3. La aplicación cargará automáticamente los datos de prueba y estará lista para usar.

> No se necesita servidor web ni instalación de paquetes.

---

## 🔧 Tecnologías utilizadas

| Tecnología     | Versión | Función |
|----------------|---------|---------|
| HTML5          | 5       | Estructura de la interfaz |
| CSS3           | 3       | Estilos con modo oscuro/claro |
| JavaScript     | ES6     | Lógica de simulación y animación |
| Chart.js       | 4.4     | Visualización de gráficas |
| MathJax        | 3.2     | Renderizado de ecuaciones LaTeX |
| jsPDF + html2canvas | 2.5 / 1.4 | Generación de reportes PDF |

---

## 🧮 Notas técnicas

- El método numérico implementado es **Runge‑Kutta de 4° orden** con paso ajustable `Δt`.
- La ecuación diferencial general es:
  \[
  A \frac{dh}{dt} = Q_{in} - k \sqrt{h}
  \]
- Para el tanque simple se obtiene la solución analítica:
  \[
  h(t) = \left( \sqrt{h_0} - \frac{k}{2A} t \right)^2
  \]
- Los datos de prueba iniciales simulan un tanque con \(A = 2\,\text{m}^2\), \(k = 0.5\,\text{m}^2/\text{s}\), \(h_0 = 5\,\text{m}\).

---

## 👥 Integrantes del proyecto

| NOMBRE                              | ORCID                    | CARRERA            |
|-------------------------------------|--------------------------|--------------------|
| Azurduy Zambrana Ángel Moisés       | 0009-0003-4458-9355      | Ing. Sistemas      |
| Molina Sejas Josue Martin           | 0009-0007-2807-1950      | Ing. Sistemas      |
| Torrico Maquera Gustavo Gilmer      | 0009-0008-5094-6288      | Ing. Sistemas      |
| Martinez Teologides Sebastian       | 0009-0002-2408-5400      | Ing. Informática   |
| Romero Villarroel Pedro Matias      | 0009-0005-7990-7565      | Ing. Redes y T.    |

**Docente:** Ing. Eudal Avendaño Gonzales

---

## 📄 Reporte y documentación

El simulador genera automáticamente un **reporte en PDF** que incluye:

- Carátula institucional con borde doble (estilo FICCT).
- Parámetros del sistema.
- Ecuación diferencial con valores sustituidos.
- Solución analítica paso a paso.
- Tabla de resultados numéricos (RK4).
- Gráficas de \(h(t)\) y \(Q(t)\).
- Conclusiones y recomendaciones.

También puedes copiar el código **LaTeX** completo del reporte para compilarlo independientemente.

---

## 🚀 Mejoras futuras

- Extender a geometrías variables \(A(h)\) (tanques cónicos o esféricos).
- Incorporar fricción en tuberías (Darcy‑Weisbach).
- Implementar control PID para regular el nivel.
- Validación con datos experimentales de laboratorio.
**Santa Cruz de la Sierra — Bolivia, 2026**
