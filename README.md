
<p align="center">
  <img src="https://github.com/user-attachments/assets/365f38e1-f243-4216-940a-1e977ce332e2" alt="Banner QA" width="100%">
</p>



#  ¡Hola, soy Samir! 👋

Soy **QA Tester** en formación con experiencia práctica en pruebas funcionales, **validación de APIs** y evaluación de interfaces web. Me enfoco en asegurar productos confiables mediante un análisis detallado, el uso de herramientas modernas como **Postman y JIRA**, y la aplicación de buenas prácticas usando **metodologías ágiles**.

## 🚀 Sobre mí
- 🎓 Formación empirica en **Logistica**.
- 📚 Actualmente estoy cursando el **bootcamp de Quality Assurance Engineering** de Tripleten LaTam.
- 💡 Estoy emprendiendo un nuevo camino, dejando atrás la logística para adentrarme en el mundo TI, impulsado por mi pasión por la tecnología.
- 🧩 Fortaleciendo mis habilidades en **lenguajes Java y Python**,**mobile testing**, **pruebas API** y **pruebas en bases de datos**.


## 🛠️ Habilidades y herramientas

- **Pruebas de Software:** Pruebas manuales, clases de equivalencia, pruebas de regresión, Valores limite y diseño de pruebas.
- **API Testing:** Postman, Scripts, JIRA.
- **UI Testing:** Pruebas multiplataforma, DevTools, Diseño web responsive .  
- **Metodologías:** Discord y documentación de pruebas.

## 🚀 Proyectos Destacados

### 🔹 Urban Routes *(Aplicación web para reserva de taxis)*
📌 **Contexto:** Este proyecto consiste en evaluar la funcionalidad de **“Compartir un automóvil”** dentro del aplicativo de taxis Urban Routes. El objetivo es asegurar que el usuario pueda compartir un viaje correctamente y que la interfaz responda de manera adecuada en distintos **navegadores y resoluciones.**
  
🛠 **Analisis:**

**✔️ 1. Diseño del formulario de reserva (UI) – 2 entornos**

Se ejecutaron **40 pruebas** por entorno **(Chrome 800×600 y Firefox 1920×1080)**, sumando 80 pruebas:
**23 APROBADAS, 13 NO APROBADAS y 4 OMITIDAS.**
Los fallos se repitieron en ambos navegadores, indicando problemas generales del diseño y no del entorno.

**✔️ 2. Ventanas “Agregar Tarjeta” y “Método de Pago” – Funcionalidad**

En un solo entorno se corrieron **41 pruebas:
19 APROBADAS y 21 NO APROBADAS.**
El alto número de fallos evidencia errores importantes en validaciones y comportamiento del flujo de pago.

**✔️ 3. Funcionalidad del botón “Reservar”**

Se evaluaron **5 pruebas:
1 APROBADA y 4 NO APROBADAS.**
La lógica del botón presenta fallos en habilitación y funcionamiento bajo diferentes condiciones.

**✔️ 4. Funciones de Reserva – Lógica**

Se ejecutaron **5 pruebas:**
**1 APROBADA, 3 NO APROBADAS y 1 OMITIDA.**
Se identificaron inconsistencias en pasos clave del flujo de reserva, afectando la acción principal del sistema. 

🔍 **Conclusiones:**  

Las pruebas evidencian que **Urban Routes no está lista para un lanzamiento en su estado actual**. Se identificaron fallos críticos que afectan directamente la experiencia del usuario y la capacidad de completar una reserva.

Entre los problemas más relevantes destacan:

❌ Fallos en el flujo principal de reserva, como el mal funcionamiento del **botón Cancelar en la ventana de “Automóvil Compartido”**, lo que bloquea al usuario en un punto clave del proceso.

❌ Validaciones deficientes en **métodos de pago**, permitiendo ingresar tarjetas inválidas que comprometen la integridad del cobro.

❌ Errores de interfaz, especialmente en la selección del automóvil, generando confusión y riesgo de reservas incorrectas.

Además, el sistema solo permite **pagar con tarjeta** en el servicio “Automóvil Compartido”, lo que limita a usuarios que utilizan otros medios de pago. **Se recomienda habilitar opciones como efectivo o billeteras digitales**, ampliamente utilizadas en países como Perú, **para evitar que usuarios potenciales abandonen la app o migren a la competencia.**

En conjunto, estos problemas tienen un impacto directo en la usabilidad, accesibilidad y confiabilidad del producto. No se recomienda el lanzamiento hasta corregir los errores identificados y ampliar las opciones de pago para mejorar la experiencia del usuario y fortalecer la competitividad de la aplicación  

🔗 **[Repositorio](https://docs.google.com/spreadsheets/d/1RfMwd0oTuZMptLQmKaavlMsr3Y_mB5hV/edit?usp=sharing&ouid=117698356908026899234&rtpof=true&sd=true)**

---

### 🔹 Urban Grocers *(Plataforma web y API entrega de comestibles)*

📌 **Descripción:** Urban Grocers es una plataforma de entrega de comestibles que acaba de enviar nuevas actualizaciones sobre cómo maneja los kits y los servicios de entrega. Se requiere probar las funciones especificas de como **agregar productos a un kit** y la **disponibilidad del sercicio de entrega Order and Go**. Analizar los requisitos del backend y el apidocs para asegurarte de que la API los admita correctamente.


🛠 **Analisis:**

**🥣 Requisito 1: Agregar productos a un kit**

Se ejecutaron **33 casos de prueba**, orientados a validar reglas funcionales, restricciones y comportamientos esperados al agregar productos a un kit.

✅ **14 pruebas aprobadas**

❌ **19 pruebas desaprobadas**

**El porcentaje de fallas supera el 55%**, lo cual evidencia problemas relevantes en la lógica de negocio del armado de kits.

**🚚 Requisito 2: Disponibilidad del servicio de entrega “Order & Go”**

Se evaluaron **43 casos de prueba**, enfocados en validar disponibilidad, reglas de activación y respuesta de la API relacionada al servicio.

**✅ 23 pruebas aprobadas**

**❌ 20 pruebas desaprobadas**

Aunque la cantidad de pruebas aprobadas es ligeramente mayor, el número de fallas continúa siendo significativo. Los errores se relacionan con condiciones incorrectas para habilitar el servicio, respuestas inconsistentes del endpoint y validaciones que no coinciden con los requisitos del backend.


🔍 **Conclusiones:**  

**🥣 Requisito 1: Agregar productos a un kit**

El comportamiento del endpoint no cumple con una de las reglas más importantes del negocio:
**el sistema debería impedir agregar más de 30 productos únicos por kit**, pero la API permite enviar valores fuera del límite esperado.
Lo que evidencia:

**❌ Falta de validación de límites en el backend**

**❌ Riesgo de generar kits inválidos, incompletos o con datos corruptos**

Este error afecta directamente la lógica de creación de kits y puede comprometer la integridad de los productos ofrecidos al cliente.

**🚚 Requisito 2: Disponibilidad del servicio “Order & Go”**

**Las pruebas demuestran que el endpoint no valida correctamente los valores de entrada.**
Incluso al enviar valores numéricos inválidos (negativos, decimales o fuera del rango permitido), el sistema devuelve:

**Código 200 OK**

**Disponibilidad True** del servicio Order & Go

Esto indica que el backend:

❌ No filtra parámetros incorrectos

❌ No valida tipos de datos según los requisitos

❌ Retorna respuestas engañosas que podrían habilitar el servicio cuando no corresponde

**El impacto para el usuario final sería grave: se mostraría un servicio disponible en zonas o condiciones donde no debería estarlo.**



**🛑 Recomendación General**

Con base en los resultados obtenidos, **no se recomienda** implementar estas funcionalidades en producción hasta corregir:

Validaciones de límites y reglas de negocio en ambos endpoints.

Manejo adecuado de errores y respuestas cuando se reciben valores inválidos.

Coherencia entre los requisitos documentados y el comportamiento real de la API.

La solución requiere una revisión completa del backend y sus validaciones, así como una actualización de los casos de prueba una vez implementadas las correcciones.

🔗 **[Repositorio](https://docs.google.com/spreadsheets/d/15fx3K5L_CvDCVqkwxzmoaoWlS0XJhwGXYulZhvu__jg/edit?usp=sharing)**



<!-- ===========================
     GitHub Stats — Métricas por Proyecto (Urban Routes / Urban Grocers)
     =========================== -->

<div align="center">

  <h2>📊 GitHub Stats — Métricas por Proyecto</h2>

  <!-- =====================
       URBAN ROUTES
       ===================== -->
  <h3>🚕 Urban Routes — Función: Compartir Automóvil</h3>

  <!-- Badges resumen UR -->
  <p>
    <img alt="Total UR Tests" src="https://img.shields.io/badge/Total_UrbanRoutes-131-blue?style=flat-square" />
    <img alt="UR Approved" src="https://img.shields.io/badge/Aprobadas-44-brightgreen?style=flat-square" />
    <img alt="UR Failed" src="https://img.shields.io/badge/No_Aprobadas-41-red?style=flat-square" />
    <img alt="UR Omitted" src="https://img.shields.io/badge/Omitidas-5-lightgrey?style=flat-square" />
  </p>

  <!-- Tabla UR por seccion -->
  <table align="center" style="margin-top:10px; margin-bottom:18px; border-collapse: collapse;">
    <tr>
      <td style="padding:8px 14px; background:#0b1220; color:#fff; font-weight:600;">Sección</td>
      <td style="padding:8px 14px; background:#0b1220; color:#fff; font-weight:600;">Pruebas</td>
      <td style="padding:8px 14px; background:#0b1220; color:#fff; font-weight:600;">Aprobadas</td>
      <td style="padding:8px 14px; background:#0b1220; color:#fff; font-weight:600;">No aprobadas</td>
      <td style="padding:8px 14px; background:#0b1220; color:#fff; font-weight:600;">Omitidas</td>
    </tr>
    <tr>
      <td style="padding:8px 14px;">Diseño formulario de reserva (UI) — 2 entornos</td>
      <td style="padding:8px 14px;">40</td>
      <td style="padding:8px 14px;">23</td>
      <td style="padding:8px 14px;">13</td>
      <td style="padding:8px 14px;">4</td>
    </tr>
    <tr>
      <td style="padding:8px 14px;">Agregar Tarjeta / Método de Pago</td>
      <td style="padding:8px 14px;">41</td>
      <td style="padding:8px 14px;">19</td>
      <td style="padding:8px 14px;">21</td>
      <td style="padding:8px 14px;">0</td>
    </tr>
    <tr>
      <td style="padding:8px 14px;">Lógica botón "Reservar"</td>
      <td style="padding:8px 14px;">5</td>
      <td style="padding:8px 14px;">1</td>
      <td style="padding:8px 14px;">4</td>
      <td style="padding:8px 14px;">0</td>
    </tr>
    <tr>
      <td style="padding:8px 14px;">Funciones de Reserva — Lógica</td>
      <td style="padding:8px 14px;">5</td>
      <td style="padding:8px 14px;">1</td>
      <td style="padding:8px 14px;">3</td>
      <td style="padding:8px 14px;">1</td>
    </tr>
    <tr>
      <td style="padding:8px 14px; font-weight:700;">Total (UR)</td>
      <td style="padding:8px 14px; font-weight:700;">91</td>
      <td style="padding:8px 14px; font-weight:700;">44</td>
      <td style="padding:8px 14px; font-weight:700;">41</td>
      <td style="padding:8px 14px; font-weight:700;">5</td>
    </tr>
  </table>

  <!-- =====================
       URBAN GROCERS
       ===================== -->
  <h3>🛒 Urban Grocers — Kits y Servicio "Order & Go"</h3>

  <!-- Badges resumen UG -->
  <p>
    <img alt="Total UG Tests" src="https://img.shields.io/badge/Total_UrbanGrocers-76-blue?style=flat-square" />
    <img alt="UG Approved" src="https://img.shields.io/badge/Aprobadas-37-brightgreen?style=flat-square" />
    <img alt="UG Failed" src="https://img.shields.io/badge/Desaprobadas-39-red?style=flat-square" />
    <img alt="UG Endpoints" src="https://img.shields.io/badge/Endpoints_Probados-2-orange?style=flat-square" />
  </p>

  <!-- Tabla UG por seccion -->
  <table align="center" style="margin-top:10px; margin-bottom:18px; border-collapse: collapse;">
    <tr>
      <td style="padding:8px 14px; background:#0b1220; color:#fff; font-weight:600;">Sección</td>
      <td style="padding:8px 14px; background:#0b1220; color:#fff; font-weight:600;">Pruebas</td>
      <td style="padding:8px 14px; background:#0b1220; color:#fff; font-weight:600;">Aprobadas</td>
      <td style="padding:8px 14px; background:#0b1220; color:#fff; font-weight:600;">Desaprobadas</td>
    </tr>
    <tr>
      <td style="padding:8px 14px;">Req. 1 — Agregar productos a un kit</td>
      <td style="padding:8px 14px;">33</td>
      <td style="padding:8px 14px;">14</td>
      <td style="padding:8px 14px;">19</td>
    </tr>
    <tr>
      <td style="padding:8px 14px;">Req. 2 — Disponibilidad Order & Go</td>
      <td style="padding:8px 14px;">43</td>
      <td style="padding:8px 14px;">23</td>
      <td style="padding:8px 14px;">20</td>
    </tr>
    <tr>
      <td style="padding:8px 14px; font-weight:700;">Total (UG)</td>
      <td style="padding:8px 14px; font-weight:700;">76</td>
      <td style="padding:8px 14px; font-weight:700;">37</td>
      <td style="padding:8px 14px; font-weight:700;">39</td>
    </tr>
  </table>

  <!-- =====================
       Resumen General (ambos proyectos)
       ===================== -->
  <h3>📌 Resumen General</h3>
  <p>
    <img alt="Total Combined" src="https://img.shields.io/badge/Pruebas_Totales-207-blue?style=for-the-badge" />
    <img alt="Aprobadas Combined" src="https://img.shields.io/badge/Aprobadas-81-brightgreen?style=for-the-badge" />
    <img alt="Fallidas Combined" src="https://img.shields.io/badge/Desaprobadas-80-red?style=for-the-badge" />
    <img alt="Endpoints Combined" src="https://img.shields.io/badge/Endpoints_Probados-4-orange?style=for-the-badge" />
  </p>

  <p style="font-size:12px; color:#6b7280; margin-top:8px;">
    <em>Nota: los subtotales se basan en los datos de prueba proporcionados. Si detectas alguna inconsistencia en los conteos (p. ej. pruebas faltantes en un ítem), puedo ajustar los números exactamente según tus registros.</em>
  </p>

  <!-- Links a evidencia -->
  <p>
    🔗 <a href="https://docs.google.com/spreadsheets/d/1RfMwd0oTuZMptLQmKaavlMsr3Y_mB5hV/edit?usp=sharing" target="_blank">Evidencias — Urban Routes</a>
    &nbsp;•&nbsp;
    🔗 <a href="https://docs.google.com/spreadsheets/d/15fx3K5L_CvDCVqkwxzmoaoWlS0XJhwGXYulZhvu__jg/edit?usp=sharing" target="_blank">Evidencias — Urban Grocers</a>
  </p>

</div>





## ✉️ Contact

<!-- [![Portfolio Badge](https://img.shields.io/badge/-Portifolio-blueviolet?style=flat-square&logo=Portfolio&logoColor=white)](https://pepyn0.github.io/)&nbsp; -->
  [![LinkedIn Badge](https://img.shields.io/badge/-Samir_Palomino-blue?style=flat-square&logo=Linkedin&logoColor=white&link=www.linkedin.com/in/samirpalominoqa)](www.linkedin.com/in/samirpalominoqa)&nbsp;
  [![Gmail Badge](https://img.shields.io/badge/-szavaleta.qacontact@gmail.com-red?style=flat-square&logo=Gmail&logoColor=white)](mailto:szavaleta.qacontact)&nbsp;
  

</div>


<!-- ![Snake animation](https://github.com/Pepyn0/Pepyn0/blob/output/github-contribution-grid-snake.svg) -->

