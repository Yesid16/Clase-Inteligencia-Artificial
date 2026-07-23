# Ficha de análisis

## 1. Nombre del Space

**Nombre:** Z-Image-Turbo

**Enlace:** https://huggingface.co/spaces/mrfakename/Z-Image-Turbo


------------------------------------------------------------------------

## 2. ¿Qué hace el agente?

El agente genera imágenes a partir de un prompt, se diferencia en el hecho
de que crea estas de una forma realista y vívida.

------------------------------------------------------------------------

## 3. Análisis PEAS

  Elemento          Respuesta
  ----------------- ----------------------------------------------------
  **Performance**   ¿Qué significa que el agente haga bien su trabajo? 
  
  Cuando genera o no la imagen, si se ajusta a lo que se solicita en el prompt, si es realista o genérica ya que este feature es lo que lo diferencia.
  
  **Environment**   ¿Con qué interactúa el agente?
  
  Pantalla, palabras, colores, imagen
  
  **Actuators**     ¿Qué acciones produce?
  
   Pintar pixeles, generar imagen
    
  **Sensors**       ¿Qué información recibe como entrada?
  
  Palabras, prompt, contexto de imagen a generar

------------------------------------------------------------------------

## 4. Clasificación del entorno

Complete la siguiente tabla y justifique brevemente cada respuesta.

  Propiedad      Clasificación     Justificación
  -------------- ----------------- ---------------
  Observable     Parcial, ya que si bien tiene acceso al prompt, hay muchas características que desconoce
  
  Determinista   No, porque no se puede determinar si generará la imagen de acuerdo al prompt o no 
  
  Episódico      No, ya que no genera imagenes secuencialmente, solo genera uno basada en un input  
  
  Estático       Sí, porque después de generar la imagen no la altera ni hace cambios en esta
  
  Discreto       Sí, cada generación funciona de forma separada mediante una entrada y salida, no cambian los valores continuamente   
  
  Conocido       Sí, conoce cómo hizo la imagen ya que tiene contexto de cada pixel que va pintando y cómo forma el resultado      

------------------------------------------------------------------------

## 5. ¿Qué tipo de programa de agente creen que es?

Seleccione la opción que consideren más adecuada y explique por qué.

-   Agente de reflejo simple
-   Agente basado en modelo
-   Agente basado en objetivos
-   Agente basado en utilidad
-   Agente con aprendizaje

Considero que es un agente de reflejo simple ya que no tiene acumula aprendizajes ni analiza diferentes caminos, simplemente tiene un input actual, el cual es el prompt que se le da con las condiciones de la imagen requerida. Se basa en una condicion actual de lo solicitado para generar la acción de crear imagen.


> **Importante:** No existe una única respuesta correcta. Lo importante
> es justificar la elección a partir del comportamiento observado.

------------------------------------------------------------------------

# Discusión en clase

Después de las presentaciones, discutiremos preguntas como:

-   ¿Dos Spaces diferentes pueden compartir el mismo tipo de entorno?
-   ¿Es posible saber con certeza qué tipo de agente implementa un Space
    únicamente observándolo?
-   ¿Qué diferencia existe entre el comportamiento observable de un
    agente y su implementación interna?

------------------------------------------------------------------------
# Reto adicional

Encuentre un Space que pueda clasificarse como:

1.  **Totalmente observable, determinista y episódico.**

UNESCO Language Translator

https://huggingface.co/spaces/UNESCO/nllb

Ya que tiene acceso a todo el texto que debe traducir, siempre traduce lo mismo a partir del mismo texto, cada traducción es independiente a la anterior


2.  **Parcialmente observable, estocástico y secuencial.**
   
https://huggingface.co/spaces/openai/whisper

Whisper Large V3: Transcribe Audio

Ya que puede no identificar todas las palabras, puede haber ruido o sonidos inesperados, cambia segun el contexto del audio, tiene en cuenta las palabras anteriores.
