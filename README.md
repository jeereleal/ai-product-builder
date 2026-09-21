# AI-Product-Builder Roadmap and resources

Index:
* [Diccionario](#diccionario)
* [Agentes](#agentes)
* [Recursos](#recursos)

------
## <a name="diccionario"></a> Diccionario

### Software en general

- Versionado
- CD/CI
- Deploy

### AI

- LLM:
  - **role**: el campo que identifica el tipo de mensaje dentro del array `messages` del SDK de OpenAI. En Chat Completions, cada mensaje suele tener la forma `{ role, content }` y el valor de `role` determina la función del mensaje.
  - **role system**: un mensaje de mayor jerarquía dentro del array `messages`; define instrucciones globales y de comportamiento que guían al modelo por encima del contenido del usuario. Es el lugar para poner consignas como “Eres un asistente que responde preguntas de geografía”, “Actúa como un profesor”, o “Responde siempre con formato JSON”. A diferencia de `user`, no es una pregunta concreta sino la política o el marco operativo de toda la conversación.
  - **role user**: el mensaje enviado por el usuario con la solicitud, tarea o pregunta concreta que se quiere resolver. Lo que popularmente se llama "prompt"
  - **role assistant**: la respuesta generada por el modelo; puede ser una respuesta textual, un resumen, una explicación o un mensaje que incluye llamadas a herramientas (`tool_calls`) según el flujo del agente.
- **Agente**:
  - **tool**: una acción concreta que el agente puede ejecutar, por ejemplo leer un archivo, ejecutar un comando, llamar a una API o editar un archivo.
  - **Built in tools**: herramientas nativas del entorno del agente, como leer archivos, escribir archivos, borrar archivos, correr comandos, buscar en internet, navegar páginas web o consultar repositorios.
  - **tool_call**: la invocación estructurada de una herramienta por parte del modelo; suele ser un JSON o un esquema que indica qué tool se ejecuta y con qué parámetros.
  - **mcp**: un conjunto de herramientas especializadas, normalmente expuestas por un servidor externo. Por ejemplo, un MCP de GitHub puede incluir tools para clonar repos, crear commits, abrir PRs o consultar issues.
  - **loop**: el ciclo de ejecución en el que el agente puede planificar, ejecutar tools, revisar resultados y volver a iterar hasta completar la tarea o alcanzar un límite de pasos.
  - **Skills**: artefactos de contexto que ayudan al agente a comportarse mejor: guías internas, convenciones del proyecto, comandos frecuentes, referencias y instrucciones operativas.
- **Sicofante**: un sistema que tiende a decir “sí” a todo, validar lo que el usuario quiere escuchar y evitar contradicciones o críticas. En inteligencia artificial, suele ser un patrón problemático porque refuerza opiniones sin cuestionarlas.
- **Estocástico vs determinista**
  - **estocástico**: el modelo responde con cierta variabilidad; aunque se use la misma entrada, no siempre devuelve exactamente lo mismo.
  - **determinista**: una función o proceso que, con los mismos inputs y condiciones, devuelve siempre el mismo resultado.
- **harness / scaffolding**: el entorno o estructura que conecta un modelo con herramientas, memoria, config, prompt, validación, logging y ejecución; es la capa que hace que un agente funcione en la práctica.
- **man-in-the-middle**: patrón de seguridad donde las acciones sensibles o potencialmente destructivas se validan antes de ejecutarse, idealmente pidiendo confirmación al usuario real para evitar errores o ejecuciones no intencionales.

### Gestión de proyecto

- Desarrollo en cascada
- Diagrama Gantt
- Metodologías ágiles
- MVP
- Spec driven development
- Test driven devélopment

### Interfaz

- FAB
- Footer
- Hamburguer menu
- Header

------

## <a name="agentes"></a> Agentes

- Array de messages con roles (system, user, assistant)
- tools: funciones locales que puede correr el agente
- El LLM va a nombrar en la respuesta json que tool_call
- loop

## <a name="recursos"></a> Recursos

### LLM gratis

- El free de copilot diario que da VsCode
- Big Pickle que lo da OpenCode
- OpenAI está regalando tokens por api si compartís tu código para entrenamiento
- Ollama se puede correr local
- Jev se puede correr local https://learnjev.com/tutorials/first-call (sirve para catalogar u obtener resultados tipo sí/no)

### Editores

- Cursor (pago)
- VsCode: Da Copilot gratis muy limitado
- Claude
- Claude Cli
- OpenCode <----- el más cool
- Codex

### Plugins

- Cline: Plugin que funciona con TODOS los llms entonces lo podés correr con claude, con big piclke, con llama local
