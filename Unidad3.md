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



**Ejemplo en lenguaje C:**
![Paso por Valor](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/PASE%20POR%20VALOR.png?raw=true)

---

#### **2. Paso por Referencia (Pass by Reference) 📤**
El emisor entrega la **dirección de memoria** (el puntero) donde reside la información original.

* **Mecánica:** El módulo receptor tiene acceso directo al **contenedor original**. Cualquier alteración impacta directamente en el dato global.
* **Contexto de uso:** Esencial para estructuras masivas, objetos complejos o **arreglos (arrays)**.
* **Atributo técnico:** Optimiza la **eficiencia de memoria y velocidad**, permitiendo modificar variables originales desde funciones.



**Ejemplo en lenguaje C:**
![Paso por Referencia](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/PASE%20POR%20REFERENCIA.png?raw=true)

#### 🔍 **Análisis del Código**
* **Línea 8 (`&numero`):** Obtiene la dirección de memoria (ej: `0x1000`). La función ahora "sabe dónde vive" la variable.
* **Línea 14 (`*n = 15`):** Accede a esa dirección y cambia el valor original de `5` a `15`.
* **Intercambio de valores (Líneas 20-22):**
    ```text
    ANTES: a=3, b=5
    1. aux = *x  (guarda 3)
    2. *x = *y   (a recibe 5)
    3. *y = aux  (b recibe 3)
    DESPUÉS: a=5, b=3 ✓
    ```

**¿Para qué sirve?** Modificar originales, intercambiar valores, pasar datos grandes (eficiencia: solo pasas 4-8 bytes) y funciones reutilizables (ej. bubble sort).

---

## 📊 **ARREGLOS (ARRAYS)**

Un **array** es una colección de elementos con tres propiedades técnicas obligatorias:

1.  **Finita:** Tamaño definido desde su creación (reserva de memoria específica).
2.  **Homogénea:** Elementos del mismo tipo de dato (no puedes mezclar tipos).
3.  **Contigua:** Ubicados en posiciones de memoria físicamente seguidas para un acceso rápido por índice.



### 🗂️ **Clasificación de Arrays**

| Tipo | Descripción | Acceso |
| :--- | :--- | :--- |
| **Unidimensional** | Colección lineal (Vector). | `nombre[i]` |
| **Bidimensional** | Tabla rectangular (Matriz). | `nombre[i][j]` |
| **Multidimensional** | Estructuras en 3D o más (Cubos). | `nombre[i][j][k]` |

#### 🖼️ **Galería de Ejemplos en C**

* **Unidimensional:**
    ![Vector](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/UNIDIMENCIONAL.png?raw=true)
* **Bidimensional:**
    ![Matriz](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/BIDIMENCIONAL.png?raw=true)
* **Multidimensional:**
    ![Cubo](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/MULTIDIMENSIONAL.png?raw=true)

---

## 💭 **Reflexión Crítica**
En esta unidad me costó demasiado entender los temas de tipos de array y la modularidad, se me hicieron complejos pero gracias a la Ing. y sus tutorías logré reforzar mis conocimientos y quitar dudas fundamentales.

---

## 📑 **Tareas Entregadas**
* ✅ [APE 1. Construcción de funciones y procedimientos](https://drive.google.com/file/d/1z92v5GO-P8uBfDW4pjwX6G5OhAi3Tyka/view?usp=drive_link)
* ✅ [AA 1. Curso Fundamentos de Python 1. Computación UNL](https://drive.google.com/file/d/1MyLiiQJ8KwwSUACr6XMBxE7UdEbG6XKS/view?usp=drive_link)

---
[⬅️ Regresar al índice principal](./index.md)
