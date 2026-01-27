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
![Ejemplo de paso por valor](https://github.com/ElvisGuayllas/Teor-a-de-la-Programaci-n/blob/main/imagenes/imagen1.png)

- **2. Paso por Referencia (Pass by Reference)**
  En lugar de duplicar el dato, el emisor entrega la dirección de memoria (el puntero o referencia) donde reside la información original.
**Mecánica:** El módulo receptor no posee una copia; tiene acceso directo al "contenedor" original. Cualquier alteración realizada por el módulo impacta directamente en el dato global.
**Contexto de uso**: Esencial para estructuras de datos masivas, objetos complejos o arreglos (arrays), donde duplicar la información penalizaría el rendimiento del sistema.
**Atributo técnico:** Optimiza la eficiencia de memoria y velocidad. Sin embargo, aumenta el riesgo de efectos colaterales, por lo que requiere una gestión más cuidadosa de la lógica de programación.



[⬅️ Regresar al índice principal](./index.md)
