# 📚 **TEMAS PRINCIPALES**

---

## 🧩 **MODULARIDAD**

La **modularidad** es una estrategia de diseño fundamentada en el principio de **"Divide y Vencerás"**. Ante algoritmos extensos y complejos, la solución óptima consiste en fragmentar el sistema en componentes más pequeños y autónomos denominados **módulos**. 

**⭐ Los tipos principales según el lenguaje o paradigma son:**
* 🛠️ **Procesos / Funciones**
* 🏗️ **Métodos**
* 🔄 **Rutinas / Subrutinas**

> **✨ Beneficio:** Esta técnica reduce la carga cognitiva del programador y facilita enormemente el mantenimiento, la escalabilidad y la reutilización de código.

---

### ⚙️ **Mecanismos de Comunicación entre Módulos**

Al segmentar un programa, los módulos deben intercambiar información. La forma en que los datos viajan define la **integridad** y el **rendimiento** del sistema.

**Definición técnica**

Cuando un parámetro se pasa por valor, la función recibe una copia independiente del dato.
Cualquier modificación realizada dentro de la función no afecta al valor original fuera de ella.

#### 1️⃣ **Paso por Valor (Pass by Value) 📥**
En este modelo, el sistema genera una **réplica exacta** del dato en un nuevo espacio de memoria asignado al módulo receptor.Es un mecanismo de paso de parámetros en programación en el cual se envía una copia del valor de una variable a una función, y no la variable original.

* **🧠 Lógica:** *"Te envío una fotocopia de mi documento; puedes rayarla, pero mi original sigue intacto."* 📄
* **⚙️ Mecánica:** El módulo receptor opera sobre la copia. Cualquier modificación permanece aislada; la variable original en el módulo emisor queda intacta.
* **🎯 Contexto de uso:** Ideal para datos **primitivos** como enteros (`int`), booleanos (`bool`) o caracteres (`char`).
* **🛡️ Atributo técnico:** Maximiza el **aislamiento** y reduce el **acoplamiento**, evitando efectos secundarios accidentales.



**💻 Ejemplo en lenguaje C:**

![Paso por Valor](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/PASE%20POR%20VALOR.png?raw=true)

**🔍 ¿Cómo funciona?**

🔢 **1.** `modificarValor(&numero);` -> `&numero` obtiene la dirección de memoria de la variable.

🔢 **2.** `printf(...)` -> Muestra el valor actual. Como la función ya lo cambió, imprime **15**.

🔢 **3.** `*n = 15;` -> `n` tiene la dirección; `*n` va a ese punto y cambia el valor allí guardado.

🚀 **Efecto:** `numero` en `main()` pasa de `5 → 15`.

---

#### 2️⃣ **Paso por Referencia (Pass by Reference) 📤**
El emisor entrega la **dirección de memoria** (el puntero o referencia) donde reside la información original. Es un mecanismo de paso de parámetros en programación en el cual la función recibe una referencia (dirección de memoria) de la variable original, no una copia de su valor.

**Definición técnica**

Cuando un parámetro se pasa por referencia, la función accede directamente a la variable original, por lo que cualquier modificación dentro de la función afecta al valor original fuera de ella.

* **🧠 Lógica:** *"Te doy las llaves de mi casa; cualquier cambio que hagas adentro se quedará ahí permanentemente."* 🔑
* **⚙️ Mecánica:** El módulo receptor tiene acceso directo al **contenedor original**. Cualquier alteración impacta directamente en el dato global.
* **🎯 Contexto de uso:** Esencial para estructuras masivas, objetos complejos o **arreglos (arrays)**.
* **⚡ Atributo técnico:** Optimiza la **eficiencia de memoria y velocidad**, aunque requiere una gestión cuidadosa.



**💻 Ejemplo en lenguaje C:**

![Paso por Referencia](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/PASE%20POR%20REFERENCIA.png?raw=true)

**🔍 ¿Cómo funciona?**

🔢 **1.** `intercambiarvalores(&a, &b);` -> Pasa las direcciones de `a` y `b`.

🔢 **2.** **Algoritmo de intercambio:**
    ```text
    1. aux = *x  (guarda valor de a)
    2. *x = *y   (a recibe valor de b)
    3. *y = aux  (b recibe valor de aux)
    ```
✅ **Resultado:** Las variables originales en `main()` intercambian sus valores exitosamente.

---

## 📊 **ARREGLOS (ARRAYS)**

Un **array** es una colección de elementos con tres propiedades técnicas fundamentales:

1.  **📏 Finita:** Tamaño definido desde su creación.
2.  **🧬 Homogénea:** Elementos del mismo tipo de dato.
3.  **🧱 Contigua:** Ubicados en posiciones de memoria físicamente seguidas para un acceso veloz.



### 🗂️ **Tipos de Array y Conceptos**

---

### 1️⃣ **Array Unidimensional (Vector) 📏**

📖 **Concepto:** Un array unidimensional es una estructura de datos lineal que permite almacenar múltiples valores del mismo tipo bajo un solo nombre, organizados en una sola dimensión.

**Definición técnica**

Es una colección de elementos del mismo tipo de dato, accesibles mediante un único índice, que representa su posición dentro de una secuencia continua en memoria.

* **🎯 Usos:** Listas secuenciales, secuencias numéricas, colas o pilas.
* **🚀 Atractivo:** Acceso directo $O(1)$ y recorrido eficiente.

**💻 Ejemplo en C:**

![Vector](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/UNIDIMENCIONAL.png?raw=true)

*✨ Ideal para almacenar listas de notas o nombres y acceder a ellos por su posición.*

---

### 2️⃣ **Array Bidimensional (Matriz) 📋**

📖 **Concepto:** Estructura rectangular organizada en **filas y columnas**. Cada elemento se identifica por dos índices: `[fila][columna]`.

**Definición técnica**

Es una colección de elementos del mismo tipo de dato, almacenados de manera contigua en memoria y accesibles mediante dos índices: el primero indica la fila,el segundo indica la columna.

* **🎯 Usos:** Tablas de datos, mapas 2D, matrices matemáticas o tableros de juegos.
* **🚀 Atractivo:** Mantiene memoria contigua para un acceso rápido a datos tabulares.

**💻 Ejemplo en C:**

![Matriz](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/BIDIMENCIONAL.png?raw=true)

*✨ Representación perfecta para tablas Excel o coordenadas en un plano.*

---

### 3️⃣ **Array Multidimensional (n-dimensional) 🧊**

📖 **Concepto:** Un array multidimensional es una estructura de datos que organiza información en dos o más dimensiones, permitiendo representar datos en forma de tablas, matrices o estructuras más complejas.

**Definición técnica**

Es un conjunto de elementos del mismo tipo de dato, organizados en múltiples índices, donde cada dimensión añade un nivel adicional de acceso.

* **🎯 Usos:** Gráficos 3D, tomografías médicas, simulaciones físicas y análisis de datos complejos.
* **🚀 Atractivo:** Permite manejar volúmenes de datos con precisión volumétrica.

**💻 Ejemplo en C:**

![Cubo](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/MULTIDIMENSIONAL.png?raw=true)

*✨ Utilizado para procesar video o píxeles en espacios tridimensionales.*

---

## 💭 **Reflexión Crítica**
Durante esta unidad, el aprendizaje de los tipos de arreglos y la modularidad representó un desafío significativo debido a su complejidad. Sin embargo, gracias al apoyo de la ingeniera y a las tutorías recibidas, logré consolidar mis conocimientos, resolver dudas críticas y fortalecer mi comprensión de estos conceptos fundamentales

---

## 📑 **Tareas Entregadas**
* ✅ [APE 1. Construcción de funciones y procedimientos](https://drive.google.com/file/d/1z92v5GO-P8uBfDW4pjwX6G5OhAi3Tyka/view?usp=drive_link)
* ✅ [AA 1. Curso Fundamentos de Python 1](https://drive.google.com/file/d/1MyLiiQJ8KwwSUACr6XMBxE7UdEbG6XKS/view?usp=drive_link)

---
[⬅️ Regresar al índice principal](./index.md)
