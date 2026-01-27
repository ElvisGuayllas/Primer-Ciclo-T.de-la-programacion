# 📚 TEMAS PRINCIPALES

## 🧩 MODULARIDAD

La **modularidad** es una estrategia de diseño fundamentada en el principio de **"Divide y Vencerás"**. Ante algoritmos extensos y complejos, la solución óptima consiste en fragmentar el sistema en componentes más pequeños y autónomos denominados **módulos**. 

Dependiendo del lenguaje o paradigma de programación, estos se conocen como:
* 🛠️ **Procesos**
* ⚙️ **Funciones**
* 🏗️ **Métodos**
* 🔄 **Rutinas / Subrutinas**

> **Beneficio:** Esta técnica reduce la carga cognitiva del programador y facilita enormemente el mantenimiento, la escalabilidad y la reutilización de código.

---

### ⚙️ Mecanismos de Comunicación entre Módulos

Al segmentar un programa, los módulos deben intercambiar información. La forma en que los datos viajan define la **integridad** y el **rendimiento** del sistema.

#### 1. Paso por Valor (*Pass by Value*) 📥
En este modelo, el sistema genera una **réplica exacta** del dato en un nuevo espacio de memoria asignado al módulo receptor.

* **Mecánica:** El módulo receptor opera sobre la copia. Cualquier modificación permanece aislada; la variable original en el módulo emisor queda intacta.
* **Contexto de uso:** Ideal para datos **primitivos** como enteros (`int`), booleanos (`bool`) o caracteres (`char`).
* **Atributo técnico:** Maximiza el **aislamiento** y reduce el **acoplamiento**, evitando efectos secundarios accidentales.



**Ejemplo en lenguaje C:**
![Paso por Valor](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/PASE%20POR%20VALOR.png?raw=true)

---

#### 2. Paso por Referencia (*Pass by Reference*) 📤
El emisor entrega la **dirección de memoria** (el puntero) donde reside la información original.

* **Mecánica:** El módulo receptor tiene acceso directo al **contenedor original**. Cualquier alteración impacta directamente en el dato global.
* **Contexto de uso:** Esencial para estructuras masivas, objetos complejos o **arreglos (arrays)**.
* **Atributo técnico:** Optimiza la **eficiencia de memoria y velocidad**, aunque requiere una gestión cuidadosa para evitar errores colaterales.



**Ejemplo en lenguaje C:**
![Paso por Referencia](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/PASE%20POR%20REFERENCIA.png?raw=true)

#### 🔍 Análisis del Código
* **Línea 8 (`&numero`):** Obtiene la dirección de memoria (ej: `0x1000`). La función ahora "sabe dónde vive" la variable.
* **Línea 14 (`*n = 15`):** Accede a esa dirección y cambia el valor original de `5` a `15`.
* **Resultado:** Al regresar al `main`, la variable ha sido modificada globalmente.

---

## 📊 ARREGLOS (ARRAYS)

Un **array** es una colección de elementos con tres propiedades técnicas obligatorias:

1.  **Finita:** Tamaño definido desde su creación.
2.  **Homogénea:** Elementos del mismo tipo de dato.
3.  **Contigua:** Ubicados en posiciones de memoria físicamente seguidas para un acceso rápido por índice.



### 🗂️ Clasificación de Arrays

| Tipo | Descripción | Acceso |
| :--- | :--- | :--- |
| **Unidimensional** | Una sola fila de elementos (Vector). | `array[i]` |
| **Bidimensional** | Tabla organizada en filas y columnas. | `array[i][j]` |
| **Multidimensional** | Estructuras en 3D o más (Cubos). | `array[i][j][k]` |

#### 🖼️ Galería de Ejemplos en C

* **Unidimensional:**
    ![Vector](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/UNIDIMENCIONAL.png?raw=true)
* **Bidimensional:**
    ![Matriz](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/BIDIMENCIONAL.png?raw=true)
* **Multidimensional:**
    ![Cubo](https://github.com/ElvisGuayllas/Primer-Ciclo-T.de-la-programacion/blob/main/imagenes/MULTIDIMENSIONAL.png?raw=true)

---

## 💭 Reflexión Crítica
Durante esta unidad, los temas de **tipos de array** y **modularidad** presentaron un desafío considerable debido a su complejidad lógica. Sin embargo, gracias a las tutorías y el refuerzo académico, logré consolidar estos conceptos fundamentales.

---

## 📂 Tareas Entregadas
* ✅ [APE 1. Construcción de funciones y procedimientos](https://drive.google.com/file/d/1z92v5GO-P8uBfDW4pjwX6G5OhAi3Tyka/view?usp=drive_link)
* ✅ [AA 1. Curso Fundamentos de Python 1](https://drive.google.com/file/d/1MyLiiQJ8KwwSUACr6XMBxE7UdEbG6XKS/view?usp=drive_link)

---
[⬅️ Regresar al índice principal](./index.md)
