# Solución de Sistemas de Ecuaciones Lineales - Método de Gauss

Implementación modular en Java del método numérico de **Eliminación Gaussiana simple con Sustitución Regresiva** para la resolución de sistemas de ecuaciones lineales algebraicas.

---

## Lenguaje de programación
* **Lenguaje:** Java (Java SE 17, 21 o superior).
* **Paradigma:** Modular / Programación estructurada orientada a métodos estáticos.
* **Paquete:** `programagauss`
* **Módulos del proyecto (`src/programagauss/`):**
    * `MetodoGauss.java`: Algoritmos numéricos de triangulación superior y sustitución hacia atrás.
    * `Matriz.java`: Definición de coeficientes y vector de términos independientes (matriz aumentada).
    * `Main.java`: Módulo orquestador con el método `main`.

---

## Compilación y ejecución

### Opción A: Desde la terminal (Línea de comandos)

1. Abrir una terminal y acceder al directorio `src/` del proyecto:
   ```bash
   cd src
   ```

2. Compilar los módulos dentro del paquete `programagauss`:
   ```bash
   javac programagauss/MetodoGauss.java programagauss/Matriz.java programagauss/Main.java
   ```
   *(o de manera abreviada: `javac programagauss/*.java`)*

3. Ejecutar la clase principal utilizando su nombre completamente cualificado:
   ```bash
   java programagauss.Main
   ```

### Opción B: Desde IntelliJ IDEA

1. Abrir el proyecto `EcuacionesLineales` en IntelliJ IDEA.
2. En el panel de navegación (`Project`), desplegar la ruta `src` -> `programagauss` -> `Main`.
3. Hacer clic derecho sobre `Main` y seleccionar **Run 'Main.main()'** (o presionar el atajo `Shift + F10`).

---

## Ejemplo de prueba y salida en consola

### Sistema de ecuaciones evaluado
El sistema cargado en `Matriz.java` corresponde a 3 ecuaciones lineales con 3 incógnitas:

$$\begin{aligned} 3.0x_1 - 0.1x_2 - 0.2x_3 &= 7.85 \\ 0.1x_1 + 7.0x_2 - 0.3x_3 &= -19.3 \\ 0.3x_1 - 0.2x_2 + 10.0x_3 &= 71.4 \end{aligned}$$

Representación en forma de matriz aumentada $[A \mid b]$:

```text
[  3.0  -0.1  -0.2 |   7.85 ]
[  0.1   7.0  -0.3 | -19.30 ]
[  0.3  -0.2  10.0 |  71.40 ]
```

### Salida obtenida en consola

```text
Soluciones del sistema:
x1 = 3.0
x2 = -2.5
x3 = 7.0
```