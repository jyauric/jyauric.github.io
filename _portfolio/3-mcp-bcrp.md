---
title: "Un servidor MCP que conecta a Claude con las series del BCRP"
collection: portfolio
imagen: mcp-grafico.jpg
imagen_alt: "Gráfico: con el servidor MCP, Claude acierta las 10 preguntas; de memoria responde que no sabe en las 10"
etiquetas: ["MCP", "FastMCP", "Claude Code", "Evaluación"]
pregunta: "¿Cuántas cifras oficiales entrega Claude sin el servidor y cuántas con él?"
cifra: "10 de 10"
cifra_texto: "aciertos con el servidor, cada uno con su fuente; sin él no respondió ninguna de las 10 preguntas."
enlaces:
  - { texto: "Código", url: "https://github.com/jyauric/mcp-bcrp" }
  - { texto: "Informe", url: "https://github.com/jyauric/mcp-bcrp/blob/main/informe.md" }
---

{{ page.pregunta }}

<p class="resultado-destacado"><strong>{{ page.cifra }}</strong> {{ page.cifra_texto }}</p>

![{{ page.imagen_alt }}](/images/{{ page.imagen }})

## Qué hice

Un servidor hecho con FastMCP que busca entre las 17,167 series oficiales del Banco Central de Reserva del Perú, las descarga y calcula variaciones. Cada respuesta cita el código de la serie, el periodo y la URL de la API.

## Evaluación

Modelo Haiku, 10 preguntas:

| Modo | Acierta | Se equivoca | No sabe | Segundos promedio |
|---|---|---|---|---|
| De memoria | 0 | 0 | 10 | 4.3 |
| Con el servidor | 10 | 0 | 0 | 7.7 |

<p class="botones">
  <a class="boton boton--principal" href="https://github.com/jyauric/mcp-bcrp">Ver el código</a>
  <a class="boton" href="https://github.com/jyauric/mcp-bcrp/blob/main/informe.md">Leer el informe</a>
</p>
