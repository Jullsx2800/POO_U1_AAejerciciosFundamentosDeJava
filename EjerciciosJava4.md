# Ejercicio 4 (Java Loops)

En este desafío, usaremos bucles para ayudarnos a hacer algunos cálculos matemáticos simples.

## Descripción

Dado un número entero, N, imprime su primero 10 múltiplos. Cada múltiplo N * i (donde 1 <= i <= 10) debe imprimirse en una nueva línea con el formato: N x i = result.

-Formato de entrada
Un solo número entero, N.

-Restricciones
2 <= N <= 20

-Formato de salida
Imprimir 10 líneas de salida; cada línea i (donde 1 <= i <= 10) contiene el result de N * i en la forma: N x i = result.


## Datos de Entrada y Salida

| N° | Dato de Entrada | Dato de Salida |
| :---: | :---: | :--- |
| 1 | 2 | 2 x 1 = 2 <br> 2 x 2 = 4 <br> 2 x 3 = 6 <br> 2 x 4 = 8 <br> 2 x 5 = 10 <br> 2 x 6 = 12 <br> 2 x 7 = 14 <br> 2 x 8 = 16 <br> 2 x 9 = 18 <br> 2 x 10 = 20 |


## Código Fuente

```
//Julian Merino
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.function.*;
import java.util.regex.*;
import java.util.stream.*;
import static java.util.stream.Collectors.joining;
import static java.util.stream.Collectors.toList;

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

        int N = Integer.parseInt(bufferedReader.readLine().trim());

        for (int i = 1; i <= 10; i++) {
            int result = N * i;
            System.out.println(N + " x " + i + " = " + result);
        }

        bufferedReader.close();
    }
}

```

Este código es fundamental para principiantes porque introduce el concepto clave de automatización mediante ciclos, permitiendo que una tarea repetitiva como una tabla de multiplicar se resuelva con pocas líneas de lógica algorítmica.

## Comprobación por HackerRank

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1494512379105509467/1498089604811587694/image.png?ex=69efe42a&is=69ee92aa&hm=ecad726ff6512b56871f0e8c901cc40f58684a446a0173c8fddd4e35483be4e1&" alt="Ejercicio 4">
</div>
