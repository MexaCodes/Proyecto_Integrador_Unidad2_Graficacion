# REPORTE DE PROYECTO INTEGRADOR
# Obtención y Conceptualización de la Fuente de Referencia

## Descripción General
El pilar fundamental de este proyecto es la creación de una guía visual de alta precisión. A diferencia de los métodos tradicionales de búsqueda manual, este proceso integra el uso de Inteligencia Artificial como motor de preproducción, optimizando tanto la calidad como la eficiencia del flujo de trabajo.

## Sinergia con Inteligencia Artificial
El uso de modelos generativos permite obtener una secuencia de movimiento (*walk/run cycle*) que respeta las leyes de la física y la anatomía del personaje de manera casi instantánea.

La Inteligencia Artificial actúa como un asistente de *layout*, resolviendo problemas complejos de perspectiva y escorzo en las extremidades del personaje. Esto reduce significativamente el tiempo de corrección técnica en etapas posteriores del proceso.

## Estructura de la Hoja de Movimiento
La imagen generada no se limita a ser un recurso visual, sino que funciona como un mapa de animación estructurado. Se diseña bajo un formato tipo *strip* (tira), en el cual se definen los distintos estados mecánicos del cuerpo:

- **Puntos de Contacto**: Momentos en los que el pie toca el suelo para iniciar el impulso.
- **Fases de Paso**: Transición del peso corporal de una pierna a otra.
- **Fases de Elevación (Up)**: Punto máximo de energía, donde ambos pies pueden estar en el aire.

## Consistencia de Diseño
Uno de los principales retos en la animación por cuadros (*frame-by-frame*) es mantener la consistencia del modelo del personaje, evitando variaciones en tamaño o apariencia entre dibujos.

La referencia generada mediante Inteligencia Artificial proporciona una plantilla de proporciones fijas, garantizando coherencia en elementos clave como:
- Cabello  
- Pliegues del vestuario (*gi*)  
- Estructura muscular  

Esto permite establecer un “norte visual” constante a lo largo de los 8 frames de animación.

## Propósito Técnico
La imagen generada cumple la función de *blueprint* (plano base) del proyecto. Contar con una referencia clara desde el inicio permite minimizar errores de vibración (*jittering*), los cuales suelen ocurrir cuando no se dispone de una guía sólida para el trazado o dibujo.

En consecuencia, se mejora la estabilidad visual y la calidad final de la animación.
<img width="1380" height="752" alt="imagen de goku" src="https://github.com/user-attachments/assets/047ab8e7-2c71-4f04-9373-7af78ccb81a4" />

# 2. Preparación y Calibración del Entorno de Trabajo (Blender)

## Descripción General
Una vez obtenida la hoja de referencia generada mediante Inteligencia Artificial, el proceso de configuración (*set-up*) en Blender resulta fundamental para garantizar un calco preciso y una escala de animación profesional.

## Importación como "Empty Image"
En lugar de importar la imagen como un plano con textura convencional, se emplea la opción:


Add > Image > Reference


Esto genera un objeto de tipo *Empty* dentro del espacio 3D.

### Ventajas técnicas:
- No aparece en el render final  
- Menor carga computacional  
- Mayor fluidez en el *viewport*  
- Manipulación más eficiente de la referencia  

## Alineación Ortográfica (Vista Frontal)
Para evitar distorsiones de perspectiva que puedan afectar la anatomía del personaje, la imagen se alinea en el eje Y utilizando la vista frontal:


Numpad 1


### Beneficios:
- Trabajo en un plano 2D puro  
- Eliminación de errores de profundidad  
- Simulación de una mesa de luz tradicional  
- Mayor precisión en el trazado de los frames  

## Ajuste de Opacidad y Profundidad (Alpha Blending)
En las propiedades del objeto (*Object Data Properties*), se activa la opción de opacidad (*Opacity*), ajustando su valor entre:

- **0.4 – 0.5 (40% – 50%)**

### Importancia del ajuste:
- Mantiene visible la referencia  
- Evita contaminación visual por colores intensos  
- Mejora la legibilidad de los nuevos trazos  
- Facilita el proceso de calco  

## Configuración de Grease Pencil (Lienzo Digital)
Se añade un objeto de tipo:


Grease Pencil > Blank


Este objeto funcionará como el lienzo principal de dibujo dentro del entorno.

### Organización por capas:
Se recomienda estructurar el trabajo en capas internas:

- **Capa "Lines"**  
  - Destinada al trazado limpio de contornos  

- **Capa "Fills"**  
  - Utilizada para aplicar color sólido (piel, vestuario, etc.)  

### Ventajas:
- Mayor orden en el flujo de trabajo  
- Separación de responsabilidades gráficas  
- Facilidad de edición y corrección  

## Bloqueo de Selección (Selectability)
Como medida técnica avanzada, se recomienda bloquear la selección del objeto de referencia desde el *Outliner*, desactivando el ícono de selección.

### Beneficios:
- Previene movimientos accidentales  
- Mantiene la alineación constante  
- Asegura consistencia en el punto de apoyo  
- Conserva la línea de horizonte durante todo el proceso  

## Propósito Técnico
La correcta preparación del entorno en Blender garantiza un flujo de trabajo estable, preciso y profesional, permitiendo al animador concentrarse en la ejecución del trazo sin interferencias técnicas.

# 3. Trazado y Definición del Primer Frame Clave (Keyframe 1)

## Descripción General
El tercer paso marca el inicio de la producción artística real. En esta etapa, la referencia estática generada por Inteligencia Artificial comienza a transformarse en un elemento funcional de animación dentro de Blender.

Este proceso se conoce técnicamente como el **posicionamiento clave del contacto inicial (Key Positioning)**.

## Selección del Punto de Origen (Contacto Inicial)
El animador se posiciona en el **Frame 1** de la línea de tiempo (*Timeline*) y selecciona la primera pose de la hoja de referencia: el momento exacto en que el talón de Goku impacta el suelo.

Esta pose es la más importante del ciclo, ya que define:

- La zancada  
- La altura de la cadera  
- La actitud del personaje (agresiva, relajada o veloz)  

## Trazado de Contornos con Grease Pencil
Utilizando una tableta digitalizadora o el mouse, se inicia el calco detallado en la capa **Lines**.

### Prioridad Anatómica
- Se traza primero el torso y la cabeza para asegurar el centro de gravedad  

### Detalle del Personaje
- Se delinean los mechones característicos del cabello  
- Se definen los pliegues del gi naranja  

Gracias a la claridad de la referencia, el animador puede simplificar ciertas líneas de sombra, logrando una animación más fluida y menos pesada visualmente.

## Aplicación de Color Sólido (Flat Colors)
Una vez cerrado el contorno, se utiliza la herramienta **Fill (bote de pintura)** en una capa inferior.

### Asignación de colores:
- Naranja para el traje  
- Azul para muñequeras y cinturón  
- Tono de piel para las áreas expuestas  

Aplicar color desde el primer frame permite visualizar el **peso visual** del personaje, facilitando la consistencia de volumen en los siguientes cuadros.

## Establecimiento de la Línea de Tierra (Floor Line)
En este paso es fundamental colocar una guía horizontal en Blender alineada con la base de los pies de la referencia.

### Propósito:
- Evitar que el personaje parezca flotar o hundirse  
- Mantener consistencia espacial  
- Establecer un punto de anclaje sólido  

Este trazo inicial funcionará como referencia para el pie de apoyo en el Frame 1 y los cuadros posteriores.

## Creación del Primer Keyframe de Objeto
Finalmente, se inserta un **Keyframe (I)** en Blender para registrar la posición y los datos del dibujo en ese punto exacto del tiempo.

Con esto, el **dibujo 01** queda oficialmente registrado dentro del proyecto, listo para continuar con la siguiente fase del ciclo de animación.

<img width="1017" height="608" alt="Screenshot 2026-03-25 181014" src="https://github.com/user-attachments/assets/f6501245-b460-457c-9a6d-3332255e70ca" />


# 4. Desarrollo de la Secuencia de Frames Clave (Frames 2 al 8)

## Descripción General
Una vez definido el primer punto de contacto, el proceso entra en una fase de iteración técnica. En esta etapa, el animador debe garantizar que la energía del movimiento se mantenga constante, siguiendo la lógica de la hoja de referencia para completar el ciclo de carrera de 8 posiciones.

## Navegación en el Timeline (Espaciado)
El animador avanza en la línea de tiempo de Blender, generalmente en intervalos de:

- 2 frames (*animación a doses*)  
- 3 frames (según el estilo requerido)  

En cada intervalo, se alinea el lienzo de **Grease Pencil** con el siguiente dibujo de la referencia.

### Objetivo:
- Mantener consistencia temporal  
- Respetar el ritmo del movimiento  
- Sincronizar cada pose con la referencia  

## Técnica de "Papel Cebolla" (Onion Skinning)
Para evitar que la animación se perciba inestable o deformada, se activa la función de **Onion Skinning** en Blender.

### Funcionalidad:
- Muestra una silueta del frame anterior (generalmente en verde o rojo)  
- Permite comparar directamente con el frame actual  

### Beneficios:
- Mantener proporciones consistentes  
- Evitar deformaciones en torso y extremidades  
- Preservar el volumen del personaje respecto al Frame 1  

## Captura de las Fases de Altura (Up Position)
Durante los frames intermedios (especialmente Frames 4 y 5), se debe prestar especial atención al eje vertical (**eje Z**).

### Consideraciones:
- El personaje se eleva del suelo  
- Se debe representar correctamente la energía del movimiento  

### Impacto visual:
- Frames demasiado bajos → movimiento pesado  
- Frames demasiado altos → sensación de flotación  

El equilibrio correcto transmite realismo y dinamismo en la carrera.

## Tratamiento de Elementos Secundarios
A lo largo de la secuencia, se deben animar adecuadamente los elementos secundarios del personaje.

### Elementos clave:

- **Cabello**  
  - Reacciona a la inercia  
  - Sube cuando el cuerpo baja  
  - Baja cuando el cuerpo sube  

- **Cintas del cinturón**  
  - Siguen un movimiento tipo látigo  
  - Se benefician de la referencia generada por IA  

### Importancia:
- Añaden dinamismo  
- Refuerzan la sensación de movimiento  
- Mejoran la calidad visual de la animación  

## Cierre del Ciclo (Looping)
Al llegar al Frame 8, se debe verificar que la última pose conecte de manera fluida con el Frame 1.

### Procedimiento:
- Reproducir la animación en modo *Loop* dentro de Blender  

### Objetivo:
- Evitar saltos bruscos  
- Lograr una transición continua  
- Crear un ciclo de carrera infinito y natural  

## Limpieza de Trazos (Inking)
Una vez completados los 8 frames, se realiza una fase de pulido final.

### Acciones:
- Cerrar correctamente todas las líneas  
- Refinar contornos  
- Eliminar imperfecciones  

### Resultado:
- Dibujos listos para el relleno de color final  
- Preparación para integración con el fondo  
- Mejora de la calidad visual general

<img width="726" height="388" alt="Screenshot 2026-03-25 181228" src="https://github.com/user-attachments/assets/02dcdfde-3afb-4480-b9cc-caaf65edf427" />


# 5. Ambientación y Finalización (Imagen de Fondo Estático)

## Descripción General
En esta etapa final, el proyecto transiciona de la fase de dibujo técnico a la composición visual. Una vez que los 8 frames de la animación están limpios y coloreados, se procede a integrar al personaje dentro de un entorno definido que aporte contexto y profundidad, manteniendo una cámara fija.

## Retiro de la Guía Técnica
Se desactiva la visibilidad de la hoja de referencia generada por Inteligencia Artificial desde el *Outliner* de Blender.

### Resultado:
- Se elimina la plantilla de apoyo visual  
- Permanece únicamente la animación final en Grease Pencil  
- Se puede evaluar la fluidez del movimiento sin interferencias  

## Inserción del Escenario (Background)
Se importa una imagen de fondo (por ejemplo, un paisaje o entorno de entrenamiento) y se coloca en una capa inferior, detrás del personaje.

### Configuración Estática:
- El fondo permanece completamente inmóvil  
- Se simula una cámara fija (*efecto trípode*)  
- El enfoque visual se centra en la animación del personaje  

## Alineación con el Suelo (Contact Points)
Es fundamental que los pies del personaje coincidan con la superficie del fondo.

### Ajustes necesarios:
- Escala de la imagen de fondo  
- Posición respecto al personaje  

### Objetivo:
- Evitar efecto de flotación  
- Mantener coherencia espacial  
- Asegurar contacto realista con el entorno  

## Enfoque en la Silueta y el Contraste
Al utilizar un fondo estático, el contraste visual se vuelve un elemento clave.

### Consideraciones:
- Los colores del personaje deben resaltar sobre el fondo  
- Se puede aplicar un ligero desenfoque (*Blur*) al fondo  

### Beneficios:
- Mejora la legibilidad de la animación  
- Dirige la atención del espectador al personaje  
- Refuerza la percepción de profundidad  

## Renderizado del Ciclo en Bucle
Para finalizar, se configura el rango de renderizado en la línea de tiempo:

- **Frames 1 al 8**

### Resultado final:
- Animación en bucle continuo (*loop infinito*)  
- Movimiento fluido y constante  
- Integración visual completa del personaje en el entorno  

Este resultado demuestra la precisión del proceso de calco, la consistencia de los frames y la calidad de la referencia inicial generada con apoyo de Inteligencia Artificial.


https://github.com/user-attachments/assets/db8c2c12-6039-48cd-a4d7-8ad510c33745







