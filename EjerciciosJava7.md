# Ejercicio 7 (Java End-of-file)

El desafío aquí es leer n líneas de entrada hasta llegar EOF, luego numera e imprime todo n líneas de contenido.

## Descripción

-Formato de entrada

Lea algo desconocido n líneas de entrada desde stdin(Sistema.in) hasta que llegues EOF; cada línea de entrada contiene una línea no vacía Cadena.

-Formato de salida

Para cada línea, imprima el número de línea, seguido de un solo espacio y luego el contenido de la línea recibido como entrada.

## Datos de Entrada y Salida

| N° | Dato de Entrada | Dato de Salida |
| :---: | :---: | :---: |
| 1 | Hello world <br> I am a file <br> Read me until end-of-file. | 1 Hello world <br> 2 I am a file <br> 3 Read me until end-of-file. |

## Código Fuente

```
//Julian Merino
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int lineNumber = 1;

        while (scanner.hasNext()) {
            String line = scanner.nextLine();
            System.out.println(lineNumber + " " + line);
            lineNumber++;
        }

        scanner.close();
    }
}

```
Este código es fundamental para principiantes porque introduce el manejo de bucles indefinidos mediante la condición hasNext(), enseñando cómo procesar flujos de datos cuya longitud es desconocida (EOF).

## Comprobación por HackerRank

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1494512379105509467/1498099605567443154/image.png?ex=69efed7b&is=69ee9bfb&hm=cdad713c30a167b172b40cf7bb717aa1ec393af0cca5a09596eacc7db9c8fd26&" alt="Ejercicio 3">
</div>

 <p align="right">
  <a href="PortadaEjercicios.md">Volver a la página principal</a>
</p>
