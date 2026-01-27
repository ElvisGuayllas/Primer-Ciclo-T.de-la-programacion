# 📚 **TEMAS PRINCIPALES**

---

## 🧩 **MODULARIDAD**

La **modularidad** es una estrategia de diseño fundamentada en el principio de **"Divide y Vencerás"**. Ante algoritmos extensos y complejos, la solución óptima consiste en fragmentar el sistema en componentes más pequeños y autónomos denominados **módulos**. 

Dependiendo del lenguaje o paradigma de programación, estos se conocen como:
* 🛠️ **Procesos** / **Funciones**
* 🏗️ **Métodos**
* 🔄 **Rutinas / Subrutinas**

> **💡 Beneficio:** Esta técnica reduce la carga cognitiva del programador y facilita el mantenimiento, la escalabilidad y la reutilización de código.

---

### ⚙️ **Mecanismos de Comunicación entre Módulos**

La forma en que los datos viajan entre módulos define la **integridad** y el **rendimiento** del sistema. Existen dos métodos fundamentales:

#### **1. Paso por Valor (Pass by Value) 📥**
En este modelo, el sistema genera una **réplica exacta** del dato en un nuevo espacio de memoria asignado al módulo receptor.

* **Mecánica:** El módulo receptor opera sobre la copia. Cualquier modificación permanece aislada; la variable original en el módulo emisor queda intacta.
* **Contexto de uso:** Ideal para datos **primitivos** como enteros (`int`), booleanos (`bool`) o caracteres (`char`).
* **Atributo técnico:** Maximiza el **aislamiento** y reduce el **acoplamiento**, evitando efectos secundarios accidentales.



- **Ejemplo en lenguaje C:**
![Paso por Valor](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/PASE%20POR%20VALOR.png?raw=true)

**¿Cómo funciona y para qué sirve el código de la imagen?**
* **Línea 8:** `modificarValor(&numero);` -> `&numero` obtiene la dirección de memoria donde está guardado `numero` y la pasa a la función. Resultado: La función "conoce dónde vive" la variable.
* **Línea 10:** `printf(...)` -> Imprime el valor actual. Como la función ya lo cambió, ahora imprime **15**. (Sin línea 8, imprimiría 5).
* **Línea 14:** `*n = 15;` -> `n` contiene la dirección; `*n` va a esa dirección y cambia el valor allí almacenado.
* **Efecto:** `numero` en `main()` pasa de `5 → 15`.

**¿Para qué sirve?** Modificar variables originales desde funciones, intercambiar valores, pasar datos grandes (eficiencia: solo pasas 4-8 bytes) y evitar copias innecesarias.

---

#### **2. Paso por Referencia (Pass by Reference) 📤**
El emisor entrega la **dirección de memoria** (el puntero o referencia) donde reside la información original.

* **Mecánica:** El módulo receptor no posee una copia; tiene acceso directo al **contenedor original**. Cualquier alteración realizada por el módulo impacta directamente en el dato global.
* **Contexto de uso:** Esencial para estructuras masivas, objetos complejos o **arreglos (arrays)**.
* **Atributo técnico:** Optimiza la **eficiencia de memoria y velocidad**, aunque requiere una gestión cuidadosa de la lógica.



- **Ejemplo en lenguaje C:**
![Paso por Referencia](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/PASE%20POR%20REFERENCIA.png?raw=true)

**¿Cómo funciona y para qué sirve el código de la imagen?**
* **Línea 12:** `intercambiarvalores(&a, &b);` -> Pasa direcciones de `a` y `b`. La función las recibe en `x` e `y`.
* **Líneas 20-22 (Algoritmo de intercambio):**
    ```text
    1. aux = *x  (guarda valor de a)
    2. *x = *y   (a recibe valor de b)
    3. *y = aux  (b recibe valor guardado en aux)
    ```
* **Salida:**
    ```text
    El Valor intercambiado de x es: 5
    El Valor intercambiado de y es: 3
    EL Valor de es a: 5
    El Valor de es b: 3
    ```

**¿Para qué sirve?** Intercambiar variables sin copiar valores grandes, algoritmos de ordenamiento (bubble sort) y crear funciones reutilizables.

---

## 📊 **ARREGLOS (ARRAYS)**

Un **array** (arreglo o vector) es una colección de elementos con tres propiedades técnicas obligatorias:

1.  **Finita:** Debe tener un tamaño definido desde su creación (reserva de memoria específica).
2.  **Homogénea:** Todos los elementos deben ser del mismo tipo de dato.
3.  **Contigua:** Los elementos se almacenan en posiciones de memoria físicamente seguidas para un acceso rápido por índice.



### 🗂️ **Tipos de Array y Conceptos**

#### **1. Array Unidimensional (Vector) 📏**
* **Concepto:** Es una estructura de datos lineal que almacena una colección finita de elementos del mismo tipo de dato en posiciones consecutivas de memoria. Cada elemento se accede mediante un único índice numérico que inicia en 0. Su simplicidad lo hace ideal para representar listas secuenciales, secuencias numéricas, colas o pilas. La organización lineal permite acceso directo O(1) y traversal eficiente El acceso es secuencial o directo mediante un único índice: `nombre[índice]`.
- **Ejemplo en C:**
    ![Vector](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/UNIDIMENCIONAL.png?raw=true)
* **¿Cómo funciona y para qué sirve?:** Permite almacenar listas de datos (como notas o nombres) y acceder a ellos rápidamente mediante su posición.

#### **2. Array Bidimensional (Matriz) 📋**
* **Concepto:** Estructura rectangular que organiza elementos en un sistema de filas y columnas, formando una tabla bidimensional. Cada elemento se identifica por dos índices: fila y columna. Perfecto para representar tablas de datos, mapas 2D, matrices matemáticas, imágenes en escala de grises o tableros de juegos. El total de elementos es filas × columnas, manteniendo memoria contigua para acceso rápido El acceso requiere dos índices: `nombre[fila][columna]`. El total de elementos es `filas × columnas`.
- **Ejemplo en C:**
    ![Matriz](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/BIDIMENCIONAL.png?raw=true)
* **¿Cómo funciona y para qué sirve?:** Ideal para representar tablas de datos, mapas de juego o matrices matemáticas.

#### **3. Array Multidimensional (n-dimensional) 🧊**
* **Concepto:** Generalización a tres o más dimensiones que organiza datos en estructuras volumétricas o hiperdimensionales. Cada elemento requiere n índices para localización precisa. Se usa en gráficos 3D, procesamiento de imágenes médicas (tomografías), simulaciones físicas, bases de datos multidimensionales y análisis de datos complejos. Mantiene la propiedad de almacenamiento contiguo pero con complejidad exponencial en memoria. Acceso: `nombre[i1][i2][i3]...[in]`.
- **Ejemplo en C:**
    ![Cubo](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/MULTIDIMENSIONAL.png?raw=true)
* **¿Cómo funciona y para qué sirve?:** Usado para datos volumétricos complejos, como simulaciones físicas o procesamiento de video (píxeles en 3D).

---

## 💭 **Reflexión Crítica**
En esta unidad me costó demasiado entender los temas de tipos de array y la modularidad, se me hicieron complejos pero gracias a la Ing. y sus tutorías logré reforzar mis conocimientos y quitar dudas fundamentales.

---

## 📑 **Tareas Entregadas**
* ✅ [APE 1. Construcción de funciones y procedimientos](https://drive.google.com/file/d/1z92v5GO-P8uBfDW4pjwX6G5OhAi3Tyka/view?usp=drive_link)
* ✅ [AA 1. Curso Fundamentos de Python 1. Computación UNL](https://drive.google.com/file/d/1MyLiiQJ8KwwSUACr6XMBxE7UdEbG6XKS/view?usp=drive_link)

---
[⬅️ Regresar al índice principal](./index.md)
