# LLM Agent Architecture

Proyecto orientado al estudio y desarrollo de agentes autónomos basados en modelos de lenguaje (LLM), enfocado en problemas reales de producción, inferencia híbrida y razonamiento mediante herramientas externas.

Este trabajo nace a partir de una idea muy simple:

> ¿Y si el núcleo de un agente autónomo fuese únicamente un ciclo de decisión y ejecución?

A partir de esta premisa se desarrolló una arquitectura capaz de:
- analizar contexto
- decidir acciones dinámicamente
- utilizar herramientas externas
- iterar hasta alcanzar un objetivo

Todo ello utilizando lenguaje natural como núcleo operativo.

---

## Objetivo del proyecto

El objetivo principal del trabajo es explorar cómo integrar agentes LLM en entornos reales de producción, evaluando:
- inferencia local vs cloud
- latencia y concurrencia
- gestión de contexto
- arquitecturas híbridas
- especialización de modelos
- uso de herramientas deterministas

El proyecto no busca únicamente generar respuestas, sino estudiar cómo construir sistemas autónomos reutilizables capaces de operar sobre problemas reales.

---

## Idea principal

La principal conclusión obtenida durante el desarrollo fue comprobar que el comportamiento conceptual de un agente puede simplificarse enormemente:

```text
do
   decisión = LLM(contexto)
   resultado = ejecutar_herramienta(decisión)
   contexto = actualizar(resultado)
while objetivo_no_completado
```

Este enfoque desplaza parte de la lógica procedural tradicional hacia sistemas guiados mediante:
- contexto
- objetivos
- herramientas
- lenguaje natural

---

## Arquitectura híbrida

Durante las pruebas se evaluaron distintos entornos:
- OpenAI API
- Ollama
- Qwen 2.5
- vLLM
- CUDA
- Docker
- WSL

Las conclusiones obtenidas muestran que actualmente las arquitecturas híbridas representan la solución más viable para producción real:
- modelos cloud para procesos críticos en tiempo
- modelos locales para automatización asíncrona y desatendida

---

## Contenido del repositorio

- Paper completo del proyecto
- Diagramas conceptuales de arquitectura
- Ciclo iterativo del agente autónomo
- Bibliografía utilizada
- Material visual utilizado en presentación

---

## Paper

El documento completo puede encontrarse en:

`/paper`

---

## Autor

Roger Pujol  
Institut TIC de Barcelona (ITIC)
