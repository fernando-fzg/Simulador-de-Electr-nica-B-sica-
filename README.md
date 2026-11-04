# Banco de Electrónica Básica

Simulador de circuitos en un solo archivo HTML para un curso de Electrónica Básica. Funciona en el navegador, sin instalar nada: abre `index.html`.

## Qué hace

- **Armado de circuitos:** coloca componentes en el papel y arrastra desde un pin para cablear.
- **Osciloscopio:** hasta 6 canales de voltaje o corriente, disparo, acople AC/DC, modo X-Y y mediciones de mínimo, máximo, promedio, RMS y frecuencia.
- **Regiones de operación:** muestra sobre el esquema si un transistor está en corte, activa, saturación u óhmica, con la explicación y los parámetros de pequeña señal.
- **Curvas y recta de carga:** curvas características con el punto Q en vivo.
- **Respuesta en frecuencia:** diagrama de Bode con frecuencia de corte a −3 dB.
- **43 circuitos de ejemplo**, ordenados por capítulo: diodos, transistores bipolares, amplificadores de pequeña señal, JFET, MOSFET, amplificadores operacionales, filtros, tiristores y conversores.

## Teclas

| Tecla | Acción |
| --- | --- |
| `R` | Girar |
| `F` | Espejar |
| `W` | Herramienta de cable |
| `P` | Sonda de voltaje |
| `Supr` | Borrar la selección |
| `Ctrl+Z` | Deshacer |
| `Ctrl+D` | Duplicar |
| `Espacio` | Pausar o seguir |

## Cómo calcula

Usa análisis nodal modificado con Newton-Raphson para los componentes no lineales e integración BDF2 con paso fijo. No depende de ninguna librería.

## Limitaciones

- Los parámetros de los modelos comerciales (2N2222, IRF530, LM741, etc.) son aproximados, no los de la hoja de datos. Se pueden editar en el panel derecho.
- Los transistores no incluyen capacitancias internas, así que no reproducen la caída de ganancia en alta frecuencia.
- El OpAmp no tiene pines de alimentación: su saturación se fija con los parámetros Vsat+ y Vsat−.
- SCR, DIAC, TRIAC y el comparador de colector abierto usan un modelo simple de encendido y apagado.

Es una herramienta de estudio. No reemplaza a un simulador profesional ni a la medición en laboratorio.
