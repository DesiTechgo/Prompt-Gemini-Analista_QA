La fórmula mágica de un buen prompt es: Rol + Contexto + Tarea + Formato
# Prompt: Casos de Prueba para Página de Login

## Instrucción para Gemini

```
Actúa como un Analista QA meticuloso. Estoy probando la página de inicio de sesión de una aplicación web que requiere un correo electrónico y una contraseña.

Genera una tabla Markdown con 15 casos de prueba que cubran escenarios positivos, negativos y de borde (edge cases).

Las columnas deben ser: ID, Título del Caso, Pasos, Resultado Esperado, y Prioridad (Alta/Media/Baja).
```
# 👑 Prompt Maestro (El que lo cubre todo)
### Este prompt es ideal cuando quieres una visión general y completa de todos los posibles casos de prueba en un solo lugar.

## Instrucción para Gemini
```
Actúa como un Ingeniero QA Senior experto en seguridad y automatización.

Estoy a punto de probar una página de login de una aplicación web de e-commerce. Las características de la página son:
- Login con correo electrónico y contraseña.
- La contraseña debe tener al menos 8 caracteres, una mayúscula, una minúscula y un número.
- Existe un enlace de "Olvidé mi contraseña".
- Hay un checkbox de "Recuérdame".
- Tras 5 intentos fallidos, la cuenta se bloquea por 30 minutos.
- El login es exitoso si las credenciales son correctas y redirige al dashboard del usuario.

Tu tarea es generar una suite de pruebas exhaustiva. Organiza los casos de prueba en las siguientes categorías:
1.  **Pruebas Funcionales (Casos Positivos y Negativos)**
2.  **Pruebas de UI/UX (Interfaz y Experiencia de Usuario)**
3.  **Pruebas de Seguridad**
4.  **Pruebas de Accesibilidad (WCAG 2.1 AA)**
5.  **Pruebas de Rendimiento**
6.  **Pruebas a nivel de API**
Preséntalos en formato de tabla Markdown para cada categoría. Las columnas deben ser: `ID de Prueba`, `Categoría`, `Descripción del Caso de Prueba`, 
`Pasos para Reproducir`, y `Resultado Esperado`.
```
# 🔬 Prompts Específicos por Categoría
## 1. Prompts de Pruebas Funcionales: Estos verifican que la funcionalidad principal opera como se espera.
### Prompt para Casos Positivos:
## Instrucción para Gemini
```
Actúa como un Analista QA. Para una página de login que usa email y contraseña, genera una tabla con casos de prueba funcionales POSITIVOS. 
Incluye pruebas para credenciales válidas, uso de la tecla 'Enter' para iniciar sesión y la funcionalidad del checkbox 'Recuérdame'.
```
### Prompt para Casos Negativos y de Borde (Edge Cases):
## Instrucción para Gemini
```
Actúa como un Analista QA meticuloso. Para una página de login con validación de contraseña (8 caracteres, mayúscula, minúscula, número) y 
bloqueo de cuenta tras 5 intentos fallidos, genera una tabla con casos de prueba NEGATIVOS y DE BORDE.

Incluye, pero no te limites a:
- Combinaciones de email/contraseña incorrectos.
- Casos de sensibilidad a mayúsculas/minúsculas.
- Probar el 4to, 5to y 6to intento fallido.
- Campos vacíos.
- Formatos de email inválidos (ej. sin '@', con espacios, etc.).
- Contraseñas que no cumplen con los requisitos (muy cortas, sin mayúscula, etc.).
```
# Prompts de Pruebas de UI/UX
### Se enfocan en la apariencia visual y la facilidad de uso.
## Instrucción para Gemini
```
Actúa como un especialista en UI/UX. Voy a probar una página de login. Genera una lista de verificación (checklist) en Markdown para evaluar los siguientes aspectos:
- **Diseño Responsivo:** Visualización en resoluciones de móvil, tablet y escritorio.
- **Consistencia Visual:** Alineación de campos, botones, etiquetas y mensajes de error.
- **Navegación por Teclado:** Uso de 'Tab' para moverse entre campos y 'Enter' para enviar.
- **Mensajes de Error:** Claridad, visibilidad y ayuda al usuario.
- **Comportamiento de los Campos:** Placeholder text, foco automático en el campo de email, enmascaramiento de la contraseña.
- **Estado de los Botones:** Estados normal, hover, activo y deshabilitado.
```
