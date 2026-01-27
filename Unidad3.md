#  **📚 TEMAS PRINCIPALES** 
MODULARIDAD
- La modularidad es una estrategia de diseño basada en el principio de "Divide y Vencerás". Ante algoritmos extensos y complejos, la solución óptima es fragmentar el sistema en componentes más pequeños y autónomos denominados módulos. Dependiendo del lenguaje o paradigma, estos se conocen como procesos, funciones, métodos o subrutinas.
Esta técnica no solo reduce la carga cognitiva para el programador, sino que facilita el mantenimiento, la escalabilidad y la reutilización de código.
- **Mecanismos de Comunicación entre Módulos**
Al segmentar un programa, los módulos deben intercambiar información. La forma en que los datos viajan de un punto a otro define la integridad y el rendimiento del sistema.
- Existen dos métodos fundamentales:
- **1. Paso por Valor (Pass by Value)**
  En este modelo, el sistema genera una réplica exacta del dato en un nuevo espacio de memoria asignado al módulo receptor.
- **Mecánica:** El módulo receptor opera sobre la copia. Cualquier modificación interna permanece aislada, por lo que la variable original en el módulo emisor se mantiene inalterada.
- **Contexto de uso:** Ideal para tipos de datos primitivos (escalares) como enteros ($int$), booleanos ($bool$) o caracteres ($char$).
- **Atributo técnico:** Maximiza el aislamiento y reduce el acoplamiento. Es la opción más segura para evitar "efectos secundarios" (cambios accidentales en otras partes del programa).
- **Ejemplo en lenguaje C**
- **Ejemplo:**  
![Ejemplo de paso por valor](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/PASE%20POR%20VALOR.png)
¿Como funciona y para que sirve el codigo de la imagen?
Línea 8: modificarValor(&numero);
&numero = obtiene la dirección de memoria donde está guardado numero
Pasa esa dirección (ej: 0x1000) a la función
Resultado: La función "conoce dónde vive" numero
Línea 10: printf("El valor de numero en main es: %d\n", numero);
Imprime el valor actual de numero en main()
Como la función ya lo cambió, ahora imprime 15
Prueba: Sin línea 8, imprimiría 5
Línea 14: *n = 15; (dentro de función)
n contiene la dirección 0x1000
*n = va a esa dirección y cambia el valor que hay ahí
Efecto: numero en main() pasa de 5 → 15
**¿Para qué sirve?**
Modificar variables originales desde funciones
Intercambiar valores (como tu ejemplo de intercambiarvalores)
Pasar arreglos grandes sin copiarlos
Eficiencia: solo pasas direcciones (4-8 bytes), no todo el dato
- **2. Paso por Referencia (Pass by Reference)**
  En lugar de duplicar el dato, el emisor entrega la dirección de memoria (el puntero o referencia) donde reside la información original.
**Mecánica:** El módulo receptor no posee una copia; tiene acceso directo al "contenedor" original. Cualquier alteración realizada por el módulo impacta directamente en el dato global.
**Contexto de uso**: Esencial para estructuras de datos masivas, objetos complejos o arreglos (arrays), donde duplicar la información penalizaría el rendimiento del sistema.
**Atributo técnico:** Optimiza la eficiencia de memoria y velocidad. Sin embargo, aumenta el riesgo de efectos colaterales, por lo que requiere una gestión más cuidadosa de la lógica de programación.
- **Ejemplo en lenguaje C**
**.**
![Ejemplo de paso por referencia](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/PASE%20POR%20REFERENCIA.png)
¿Como funciona y para que sirve el codigo de la imagen?
Línea 12: intercambiarvalores(&a, &b);
Pasa direcciones de a (ej: 0x1000) y b (ej: 0x1004)
Función recibe esas direcciones en x e y
Líneas 20-22: Algoritmo de intercambio clásico
text
ANTES: a=3(0x1000)  b=5(0x1004)
1. aux = *x     → aux=3
2. *x = *y      → a=5  
3. *y = aux     → b=3
DESPUÉS: a=5       b=3 ✓
Líneas 13-14: Imprimen resultado final en main(): a=5, b=3
Flujo completo
text
Inicio: a=3, b=5
→ Función recibe direcciones
→ aux guarda 3, a recibe 5, b recibe 3  
→ main() ve: a=5, b=3 ✓
Salida:
text
El Valor intercambiado de x es: 5
El Valor intercambiado de y es: 3
EL Valor de es a: 5
El Valor de es b: 3
**¿Para qué sirve?**
Intercambiar variables sin copiar valores grandes, ordenamiento (bubble sort), funciones reutilizables.

 ## ARREGLOS (ARRAYS) ##




[⬅️ Regresar al índice principal](./index.md)
