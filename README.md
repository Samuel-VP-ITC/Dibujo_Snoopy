# Dibujo_Snoopy
Realice un dibujo en Blender y aproveché las herramientas que me ofrece

Dibujo de Snoopy en Blender (Grease Pencil)
¡Hola! Este proyecto es una recreación digital del icónico personaje Snoopy sentado junto a su casita roja. Fue realizado utilizando las herramientas de dibujo 2D de Blender 5.0.1.

2. Características del Proyecto
Software: Blender 5.0.1.

Herramienta principal: Grease Pencil (Lápiz de cera).

Técnica: Entintado digital con capas de colores planos (Sombreado tipo cel-shading).

Estado: En progreso / Finalizado (elige uno).

3. Proceso de Creación
Para este dibujo seguí los siguientes pasos:

Referencia: Importación de una imagen de referencia (Snoopy-PNG-Pic) como objeto vacío para calcar las líneas principales.

Lineart: Uso de trazos negros definidos para el contorno de Snoopy y la estructura de la casa.

Color: Aplicación de materiales de relleno (Fill) sólidos para el rojo de la casa y el blanco de Snoopy.

Organización: Uso de colecciones en el Outliner para separar la referencia de los trazos finales.

4. Capturas de Pantalla
<img width="1024" height="576" alt="image" src="https://github.com/user-attachments/assets/9873d204-ce70-4ed6-83af-89b60ca0c672" />

🚀 Nueva Sección: Interactividad con Python
Para este proyecto, no solo dibujé al personaje, sino que programé un Operador Modal en Python que permite controlar el movimiento de Snoopy en tiempo real usando el teclado.

El Código: Control de Movimiento XZ
El script utiliza la biblioteca bpy para detectar eventos del teclado y transformar la ubicación del objeto en los ejes X (horizontal) y Z (vertical dentro del entorno 2D de Blender).

Python
# Resumen de la lógica principal
'''
if event.type == 'UP_ARROW':
    obj.location.z += 0.2  # Mueve hacia arriba
elif event.type == 'LEFT_ARROW':
    obj.location.x -= 0.2  # Mueve hacia la izquierda
'''

Es importante explicar estos conceptos clave:

bpy.types.Operator (Modal): A diferencia de un script normal que se ejecuta una sola vez, un operador modal se mantiene "escuchando" las acciones del usuario (teclado/mouse) hasta que se cancela (en este caso, con la tecla ESC).

invoke: Es el punto de entrada que prepara a Blender para empezar a capturar los eventos del teclado.

modal: Es el "cerebro" que se ejecuta constantemente. Aquí es donde verificamos si se presionó una flecha para actualizar la propiedad obj.location.

Ejes XZ: Dado que el dibujo está orientado en un plano frontal, usamos el eje X para los lados y el Z para la altura, simulando un movimiento 2D tradicional.

Cómo probarlo
Abre el archivo .blend.

Ve a la pestaña de Scripting.

Pega el código del archivo MoverXZ.py.

Haz clic en Run Script.

Usa las flechas del teclado para mover a Snoopy y ESC para detener el script.

<img width="1024" height="576" alt="image" src="https://github.com/user-attachments/assets/a8bea4ea-b80f-4440-b5b7-2f0b37daaf19" />
