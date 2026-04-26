# Ejercicio 5 (Java Loops II)

En este desafío, debes leer un entero, a doble, y a Cadena desde stdin, luego imprima los valores de acuerdo con las instrucciones del Formato de Salida.

## Descripción

-Formato de entrada

La primera línea contiene un número entero, q, indicando el número de consultas.
Cada línea i de las q líneas subsiguientes contienen tres números enteros separados por espacios que describen los respectivos ai, bi, y ni valores para esa consulta.

-Restricciones

0 <= q <= 500

0 <= a, b <= 50

1 <= n <= 15

-Formato de salida

Para cada consulta, imprima la serie correspondiente en una nueva línea. Cada serie debe imprimirse en orden como una sola línea de n números enteros separados por espacios.

## Datos de Entrada y Salida

| N° | Dato de Entrada | Dato de Salida |
| :---: | :---: | :---: |
| 1 | 2 <br> 0 2 10 <br> 5 3 5 | 2 6 14 30 62 126 254 510 1022 2046 <br> 8 14 26 50 98 |


## Código Fuente

```
//Julian Merino
import java.util.*;
import java.io.*;

class Solution{
    public static void main(String []argh){
        Scanner in = new Scanner(System.in);
        int t = in.nextInt();
        for(int i = 0; i < t; i++){
            int a = in.nextInt();
            int b = in.nextInt();
            int n = in.nextInt();

            int currentTerm = a;

            for (int j = 0; j < n; j++) {
                currentTerm += (int) Math.pow(2, j) * b;
                System.out.print(currentTerm + " ");
            }
            System.out.println();
        }
        in.close();
    }
}

```

Este código es fundamental para principiantes porque introduce el manejo de bucles anidados y el uso de la clase Math, herramientas esenciales para resolver series numéricas complejas de forma eficiente.

## Comprobación por HackerRank

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1494512379105509467/1498092615269220402/image.png?ex=69efe6f8&is=69ee9578&hm=e65a21253edd0e1cafbdeaca686006986aafc2b61ba8afb0d76f31ff04530bd0&" alt="Ejercicio 5">
</div>
