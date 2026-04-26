# Ejercicio 8 (Java Static Initializer Block)

Los bloques de inicialización estática se ejecutan cuando se carga la clase y puedes inicializar variables estáticas en esos bloques.

Es hora de probar tus conocimientos de Bloques de inicialización estáticos. Puedes leer sobre ello aquí.

Se te da una clase Solución con a principal método.

## Descripción

-Formato de entrada

Hay dos líneas de entrada. La primera línea contiene B: la anchura del paralelogramo. La siguiente línea contiene H: la altura del paralelogramo.

-Restricciones

-100 <= B <= 100

-100 <= H <= 100

-Formato de salida

Si ambos valores son mayores que cero, entonces el principal El método debe generar el área del paralelogramo. De lo contrario, imprimir "java.lang.Exception: La amplitud y la altura deben ser positivas" sin comillas.

## Datos de Entrada y Salida

| N° | Dato de Entrada | Dato de Salida |
| :---: | :---: | :---: |
| 1 | 1 <br> 3 | 3 |
| 2 | -1 <br> 2 | java.lang.Exception: Breadth and height must be positive |


## Código Fuente

```
//Julian Merino
import java.io.*;
import java.util.*;

public class Solution {

    static int B;
    static int H;
    static boolean isValid;

    static {
        Scanner scanner = new Scanner(System.in);
        B = scanner.nextInt();
        H = scanner.nextInt();

        if (B <= 0 || H <= 0) {
            isValid = false;
            System.out.println("java.lang.Exception: Breadth and height must be positive");
        } else {
            isValid = true;
        }
        scanner.close();
    }

    public static void main(String[] args) {
        if (isValid) {
            int area = B * H;
            System.out.println(area);
        }
    }
}

```
Este código es fundamental para principiantes porque introduce el concepto de bloques de inicialización estáticos, permitiendo ejecutar lógica de configuración y validación de datos antes de que el método main comience.

## Comprobación por HackerRank

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1494512379105509467/1498102344615727234/image.png?ex=69eff008&is=69ee9e88&hm=17eae7ca3a75eaf46def0a3a5953a3209a4f804793a8968f4c0245bd6c272f1a&" alt="Ejercicio 3">
</div>
