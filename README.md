
![tester(1)](https://github.com/user-attachments/assets/368d3250-3a36-4de1-8143-04dffa1e5779)


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
📌 **Contexto:** Este proyecto consiste en evaluar la funcionalidad de “Compartir automóvil” dentro del aplicativo de taxis Urban Routes. El objetivo es asegurar que el usuario pueda compartir un viaje correctamente y que la interfaz responda de manera adecuada en distintos navegadores y resoluciones.
  
🛠 **Analisis:**

✔️ 1. Diseño del formulario de reserva (UI) – 2 entornos

Se ejecutaron 40 pruebas por entorno (Chrome 800×600 y Firefox 1920×1080), sumando 80 pruebas:
23 APROBADAS, 13 NO APROBADAS y 4 OMITIDAS.
Los fallos se repitieron en ambos navegadores, indicando problemas generales del diseño y no del entorno.

✔️ 2. Ventanas “Agregar Tarjeta” y “Método de Pago” – Funcionalidad

En un solo entorno se corrieron 41 pruebas:
19 APROBADAS y 21 NO APROBADAS.
El alto número de fallos evidencia errores importantes en validaciones y comportamiento del flujo de pago.

✔️ 3. Funcionalidad del botón “Reservar”

Se evaluaron 5 pruebas:
1 APROBADA y 4 NO APROBADAS.
La lógica del botón presenta fallos en habilitación y funcionamiento bajo diferentes condiciones.

✔️ 4. Funciones de Reserva – Lógica

Se ejecutaron 5 pruebas:
1 APROBADA, 3 NO APROBADAS y 1 OMITIDA.
Se identificaron inconsistencias en pasos clave del flujo de reserva, afectando la acción principal del sistema. 

🔍 **Conclusiones:**  

Las pruebas evidencian que Urban Routes no está lista para un lanzamiento en su estado actual. Se identificaron fallos críticos que afectan directamente la experiencia del usuario y la capacidad de completar una reserva.

Entre los problemas más relevantes destacan:

❌ Fallos en el flujo principal de reserva, como el mal funcionamiento del botón Cancelar en la ventana de “Automóvil Compartido”, lo que bloquea al usuario en un punto clave del proceso.

❌ Validaciones deficientes en métodos de pago, permitiendo ingresar tarjetas inválidas que comprometen la integridad del cobro.

❌ Errores de interfaz, especialmente en la selección del automóvil, generando confusión y riesgo de reservas incorrectas.

Además, el sistema solo permite pagar con tarjeta en el servicio “Automóvil Compartido”, lo que limita a usuarios que utilizan otros medios de pago. Se recomienda habilitar opciones como efectivo o billeteras digitales, ampliamente utilizadas en países como Perú, para evitar que usuarios potenciales abandonen la app o migren a la competencia.

En conjunto, estos problemas tienen un impacto directo en la usabilidad, accesibilidad y confiabilidad del producto. No se recomienda el lanzamiento hasta corregir los errores identificados y ampliar las opciones de pago para mejorar la experiencia del usuario y fortalecer la competitividad de la aplicación  

🔗 **[Repositorio](https://docs.google.com/spreadsheets/d/1RfMwd0oTuZMptLQmKaavlMsr3Y_mB5hV/edit?usp=sharing&ouid=117698356908026899234&rtpof=true&sd=true)**

---

### 🔹 Urban Grocers *(Plataforma web y API entrega de comestibles)*
📌 **Descripción:** Urban Grocers es una plataforma de entrega de comestibles que acaba de enviar nuevas actualizaciones sobre cómo maneja los kits y los servicios de entrega. Se requiere probar las funciones especificas de como **agregar productos a un kit** y la **disponibilidad del sercicio de entrega Order and Go**. Analizar los requisitos del backend y el apidocs para asegurarte de que la API los admita correctamente.


🛠 **Analisis:**

🥣 Requisito 1: Agregar productos a un kit

Se ejecutaron 33 casos de prueba, orientados a validar reglas funcionales, restricciones y comportamientos esperados al agregar productos a un kit.

✅ 14 pruebas aprobadas

❌ 19 pruebas desaprobadas

El porcentaje de fallas supera el 55%, lo cual evidencia problemas relevantes en la lógica de negocio del armado de kits.

🚚 Requisito 2: Disponibilidad del servicio de entrega “Order & Go”

Se evaluaron 43 casos de prueba, enfocados en validar disponibilidad, reglas de activación y respuesta de la API relacionada al servicio.

✅ 23 pruebas aprobadas

❌ 20 pruebas desaprobadas

Aunque la cantidad de pruebas aprobadas es ligeramente mayor, el número de fallas continúa siendo significativo. Los errores se relacionan con condiciones incorrectas para habilitar el servicio, respuestas inconsistentes del endpoint y validaciones que no coinciden con los requisitos del backend.


🔍 **Conclusiones:**  

🥣 Requisito 1: Agregar productos a un kit

El comportamiento del endpoint no cumple con una de las reglas más importantes del negocio:
el sistema debería impedir agregar más de 30 productos únicos por kit, pero la API permite enviar valores fuera del límite esperado.
Lo que evidencia:

❌ Falta de validación de límites en el backend

❌ Inconsistencia entre los requisitos funcionales y la implementación real

❌ Riesgo de generar kits inválidos, incompletos o con datos corruptos

Este error afecta directamente la lógica de creación de kits y puede comprometer la integridad de los productos ofrecidos al cliente.

🚚 Requisito 2: Disponibilidad del servicio “Order & Go”

Las pruebas demuestran que el endpoint no valida correctamente los valores de entrada.
Incluso al enviar valores numéricos inválidos (negativos, decimales o fuera del rango permitido), el sistema devuelve:

Código 200 OK

Disponibilidad afirmativa del servicio Order & Go

Esto indica que el backend:

❌ No filtra parámetros incorrectos

❌ No valida tipos de datos según los requisitos

❌ Retorna respuestas engañosas que podrían habilitar el servicio cuando no corresponde

El impacto para el usuario final sería grave: se mostraría un servicio disponible en zonas o condiciones donde no debería estarlo.


🛑 Recomendación General

Con base en los resultados obtenidos, no se recomienda implementar estas funcionalidades en producción hasta corregir:

Validaciones de límites y reglas de negocio en ambos endpoints.

Manejo adecuado de errores y respuestas cuando se reciben valores inválidos.

Coherencia entre los requisitos documentados y el comportamiento real de la API.

La solución requiere una revisión completa del backend y sus validaciones, así como una actualización de los casos de prueba una vez implementadas las correcciones.

🔗 **[Repositorio](https://docs.google.com/spreadsheets/d/15fx3K5L_CvDCVqkwxzmoaoWlS0XJhwGXYulZhvu__jg/edit?usp=sharing)**



## 📊 GitHub Stats
[![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=ArturoLopMan)](https://github.com/anuraghazra/github-readme-stats)<br/>

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=ArturoLopMan)](https://github.com/anuraghazra/github-readme-stats)

¡Gracias por visitar mi perfil! 😊
<!--
**ArturoLopMan/ArturoLopMan** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

## ✉️ Contact

<!-- [![Portfolio Badge](https://img.shields.io/badge/-Portifolio-blueviolet?style=flat-square&logo=Portfolio&logoColor=white)](https://pepyn0.github.io/)&nbsp; -->
  [![LinkedIn Badge](https://img.shields.io/badge/-Samir_Palomino-blue?style=flat-square&logo=Linkedin&logoColor=white&link=www.linkedin.com/in/samirpalominoqa)](www.linkedin.com/in/samirpalominoqa)&nbsp;
  [![Gmail Badge](https://img.shields.io/badge/-szavaleta.qacontact@gmail.com-red?style=flat-square&logo=Gmail&logoColor=white)](mailto:szavaleta.qacontact)&nbsp;
  

</div>


<!-- ![Snake animation](https://github.com/Pepyn0/Pepyn0/blob/output/github-contribution-grid-snake.svg) -->

