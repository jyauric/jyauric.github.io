---
title: "Tres skills de Claude Code que limpian, grafican y mapean la ENAHO 2024"
collection: portfolio
imagen: enaho-mapa.jpg
imagen_alt: "Mapa de la pobreza monetaria por departamento, Perú 2024"
etiquetas: ["Claude Code", "Skills", "ENAHO", "Mapas"]
pregunta: "¿Puede un agente limpiar la ENAHO y replicar la pobreza oficial?"
cifra: "27.53 %"
cifra_texto: "de pobreza monetaria, frente al 27.6 % oficial del INEI, con 108,664 residentes habituales."
enlaces:
  - { texto: "Código", url: "https://github.com/jyauric/enaho-skills" }
  - { texto: "Evaluación", url: "https://github.com/jyauric/enaho-skills/blob/main/evaluacion.md" }
---

{{ page.pregunta }}

<p class="resultado-destacado"><strong>{{ page.cifra }}</strong> {{ page.cifra_texto }}</p>

![{{ page.imagen_alt }}](/images/{{ page.imagen }})

## Qué hice

Tres skills que se usan en cadena: basta pedirle a Claude «un mapa de la pobreza por departamento» para que limpie la base, la valide y genere el mapa.

| Skill | Qué hace |
|---|---|
| `limpiando-enaho` | Une los módulos 34 y 02 y valida la base |
| `graficando-enaho` | Grafica la pobreza por área, sexo o edad |
| `mapeando-enaho` | Mapea la pobreza por departamento |

## Validación

| Chequeo | Resultado | Oficial INEI |
|---|---|---|
| Pobreza monetaria | 27.53 % | 27.6 % |
| Pobreza extrema | 5.50 % | 5.5 % |

También comparé tres pedidos con y sin skills. Sin ellas, Claude llegó a cifras parecidas, pero con figuras menos cuidadas: por ejemplo, un mapa cuya escala no empezaba en 0.

<p class="botones">
  <a class="boton boton--principal" href="https://github.com/jyauric/enaho-skills">Ver el código</a>
  <a class="boton" href="https://github.com/jyauric/enaho-skills/blob/main/evaluacion.md">Leer la evaluación</a>
</p>
