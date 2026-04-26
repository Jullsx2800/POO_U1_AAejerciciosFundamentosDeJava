# Ejercicio 1 (Java If-Else)

En este desafío, ponemos a prueba tus conocimientos sobre el uso if-else Declaraciones condicionales para automatizar los procesos de toma de decisiones. 

## Descripción

Dado un número entero, , realice las siguientes acciones condicionales:

-Si es extraño, imprimir Weird

-Si es uniforme y está en el rango inclusivo de to , imprimir Not Weird

-Si es uniforme y está en el rango inclusivo de to , imprimir Weird

-Si es par y mayor que , imprimir Not Weird

## Datos de Entrada y Salida

| N° | Dato de Entrada | Dato de Salida |
| :---: | :---: | :---: |
| 1 | 3 | Weird |
| 2 | 24 | Not Weird |

## Código Fuente

```
//Julián Merino

import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solucion {

    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        int N = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        if (N % 2 != 0) {
            System.out.println("Raro");
        } else {
            if (N >= 2 && N <= 5) {
                System.out.println("No es raro");
            } else if (N >= 6 && N <= 20) {
                System.out.println("Raro");
            } else if (N > 20) {
                System.out.println("No es raro");
            }
        }

        scanner.close();
    }
}

```
Este código es ideal para principiantes porque transforma reglas matemáticas en lógica de decisión. Su mayor beneficio es que enseña a estructurar el pensamiento mediante el uso de condicionales y rangos, entendiendo cómo la computadora evalúa estados (par o impar) y límites numéricos.

## Comprobación por HackerRank

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1494512379105509467/1498075985688531065/image.png?ex=69efd77b&is=69ee85fb&hm=ffe41c8c1fbb828267a912e1accf3acc5851a6faacdb92be7d084b92c5d1529e&" alt="Ejercicio 1">
</div>



