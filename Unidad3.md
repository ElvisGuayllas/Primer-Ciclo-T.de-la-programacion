# 📚 **TEMAS PRINCIPALES**

---

## 🧩 **MODULARIDAD**

La **modularidad** es una estrategia de diseño basada en el principio de **"Divide y Vencerás"**. Ante algoritmos extensos y complejos, la solución óptima es fragmentar el sistema en componentes más pequeños y autónomos denominados **módulos**. Dependiendo del lenguaje o paradigma, estos se conocen como:
* 🔹 Procesos
* 🔹 Funciones
* 🔹 Métodos
* 🔹 Rutinas o subrutinas

Esta técnica no solo reduce la carga cognitiva para el programador, sino que facilita el **mantenimiento**, la **escalabilidad** y la **reutilización de código**.

### ⚙️ **Mecanismos de Comunicación entre Módulos**
Al segmentar un programa, los módulos deben intercambiar información. La forma en que los datos viajan de un punto a otro define la integridad y el rendimiento del sistema. Existen dos métodos fundamentales:

---

#### **1. Paso por Valor (Pass by Value) 📥**
En este modelo, el sistema genera una **réplica exacta** del dato en un nuevo espacio de memoria asignado al módulo receptor.

* **Mecánica:** El módulo receptor opera sobre la copia. Cualquier modificación interna permanece aislada, por lo que la variable original en el módulo emisor se mantiene inalterada.
* **Contexto de uso:** Ideal para tipos de datos primitivos (escalares) como enteros ($int$), booleanos ($bool$) o caracteres ($char$).
* **Atributo técnico:** Maximiza el aislamiento y reduce el acoplamiento. Es la opción más segura para evitar "efectos secundarios".



**Ejemplo en lenguaje C:**
![Ejemplo de paso por valor](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/PASE%20POR%20VALOR.png)

**¿Cómo funciona y para qué sirve el código de la imagen?**
* **Línea 8:** `modificarValor(&numero);` -> `&numero` obtiene la dirección de memoria donde está guardado el número y la pasa a la función. Resultado: La función "conoce dónde vive" la variable.
* **Línea 10:** `printf(...)` -> Imprime el valor actual. Como la función ya lo cambió, ahora imprime **15**. (Sin línea 8, imprimiría 5).
* **Línea 14:** `*n = 15;` -> `n` contiene la dirección; `*n` va a esa dirección y cambia el valor allí almacenado.

**¿Para qué sirve?**
1. Modificar variables originales desde funciones.
2. Intercambiar valores.
3. Pasar arreglos grandes sin copiarlos.
4. **Eficiencia:** solo pasas direcciones (4-8 bytes), no todo el dato.

---

#### **2. Paso por Referencia (Pass by Reference) 📤**
En lugar de duplicar el dato, el emisor entrega la **dirección de memoria** (el puntero o referencia) donde reside la información original.

* **Mecánica:** El módulo receptor no posee una copia; tiene acceso directo al "contenedor" original. Cualquier alteración impacta directamente en el dato global.
* **Contexto de uso:** Esencial para estructuras de datos masivas, objetos complejos o arreglos (arrays).
* **Atributo técnico:** Optimiza la eficiencia de memoria y velocidad. Requiere gestión cuidadosa de la lógica.



**Ejemplo en lenguaje C:**
![Ejemplo de paso por referencia](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/PASE%20POR%20REFERENCIA.png)

**¿Cómo funciona y para qué sirve el código de la imagen?**
* **Línea 12:** `intercambiarvalores(&a, &b);` -> Pasa direcciones de `a` y `b`. La función las recibe en `x` e `y`.
* **Líneas 20-22:** Algoritmo de intercambio clásico:
    ```text
    ANTES: a=3, b=5
    1. aux = *x  (guarda 3)
    2. *x = *y   (a recibe 5)
    3. *y = aux  (b recibe 3)
    DESPUÉS: a=5, b=3 ✓
    ```
* **Salida:**
    ```text
    El Valor intercambiado de x es: 5
    El Valor intercambiado de y es: 3
    EL Valor de es a: 5
    El Valor de es b: 3
    ```

**¿Para qué sirve?**
* Intercambiar variables sin copiar valores grandes, ordenamiento (bubble sort) y funciones reutilizables.

---

## 📊 **ARREGLOS (ARRAYS)**

Un **array** (arreglo o vector) es una colección **finita, homogénea y contigua** de elementos.

1.  **Finita:** Debe tener un tamaño definido desde su creación (reserva de memoria específica).
2.  **Homogénea:** Todos los elementos deben ser del mismo tipo de dato.
3.  **Contigua:** Los elementos se almacenan en posiciones de memoria físicas seguidas.



### 📂 **Tipos de Array**

#### **1. Array Unidimensional (Vector)** 📏
Colección lineal de elementos del mismo tipo en una sola fila. Acceso mediante un único índice: `nombre[índice]`.
![Ejemplo unidimensional](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/UNIDIMENCIONAL.png)

#### **2. Array Bidimensional (Matriz)** 📋
Estructura rectangular (filas y columnas). Representa una tabla 2D. Acceso: `nombre[fila][columna]`.
![Ejemplo bidimensional](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/BIDIMENCIONAL.png)

#### **3. Array Multidimensional (n-dimensional)** 🧊
Extensión a 3 o más dimensiones (cubos). Acceso: `nombre[i1][i2][i3]...`. Usado para datos volumétricos.
![Ejemplo multidimensional](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/MULTIDIMENSIONAL.png)

---

## 📝 **Reflexión crítica**
En esta unidad me costó demasiado entender los temas de tipos de array y la modularidad, se me hicieron complejos pero gracias a la Ing. y sus tutorías logré reforzar mis conocimientos y quitar dudas.

---

## 📑 **Tareas Entregadas**
* ✅ [APE 1. Construcción de funciones y procedimientos](https://drive.google.com/file/d/1z92v5GO-P8uBfDW4pjwX6G5OhAi3Tyka/view?usp=drive_link)
* ✅ [AA 1. Curso Fundamentos de Python 1. Computación UNL](https://drive.google.com/file/d/1MyLiiQJ8KwwSUACr6XMBxE7UdEbG6XKS/view?usp=drive_link)

---
[⬅️ Regresar al índice principal](./index.md)
