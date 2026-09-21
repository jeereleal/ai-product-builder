# AI-Product-Builder Roadmap and resources

Index:
* [Diccionario](#diccionario)
* [Agentes](#agentes)

------
## <a name="diccionario"></a> Diccionario

- LLM:
- role system
- role user
- role assistant: (es probable que un modelo a otro cambien)
- tool: 
- tool_call: 
- loop: sistema en el que el agente LLM puede volver a lanzarse después de haber completado tareas
- mcp: un conjunto de tools de un area, por ejemplo el mcp de github tendrá una tool clonar, una tool commitear, etc.
- Built in tools: las tools por default que tienen los agentes más conocidos tipo Claude Code, OpenAI agent, Anything LLM, etc. son: leer archivos, escribir archivos, borrar archivo, correr comandos.
- Skills: contexto, guias, lista de comandos habituales, referencias a otros archivos
- Sicofante: te dice todo que sí, todo lo que querés escuchar. SIEMPRE responde algo.
- Estocástico: estadístico, que no responde siempre lo mismo

------

## <a name="agentes"></a>  Agentes

- Array de messages con roles (system, user, assistant)
- tools: funciones locales que puede correr el agente
- El LLM va a nombrar en la respuesta json que tool_call
- loop
