# Ejercicio 12 (Java BigDecimal)

La clase BigDecimal de Java puede manejar números decimales con signo de precisión arbitraria. ¡Pongamos a prueba tus conocimientos sobre ellos!

## Descripción

-Formato de entrada

La primera línea consta de un solo número entero, n , que indica el número de cadenas enteras.
Cada línea i de la n Las líneas subsiguientes contienen un número real que denota el valor de si.

-Restricciones

1 <= n <= 200

Cada si has como máximo 300 dígitos.

-Formato de salida

El código auxiliar bloqueado en el editor imprimirá el contenido de la matriz s a stdout. Sólo eres responsable de reordenar los elementos de la matriz.

## Datos de Entrada y Salida

| N° | Dato de Entrada | Dato de Salida |
| :---: | :---: | :---: |
| 1 | 9 <br> -100 <br> 50 <br> 0 <br> 56.6 <br> 90 <br> 0.12 <br> .12 <br> 02.34 <br> 000.000 | 90 <br> 56.6 <br> 50 <br> 02.34 <br> 0.12 <br> .12 <br> 0 <br> 000.000 <br> -100 |


## Código Fuente

```
import java.math.BigDecimal;
import java.util.*;

class Solution {
    public static void main(String []args) {
        //Input
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        String []s = new String[n+2];
        for(int i=0; i<n; i++) {
            s[i] = sc.next();
        }
        sc.close();

        //Julian Merino
        Arrays.sort(s, 0, n, (String s1, String s2) -> {
            BigDecimal b1 = new BigDecimal(s1);
            BigDecimal b2 = new BigDecimal(s2);
            return b2.compareTo(b1);
        });

        //Output
        for(int i=0; i<n; i++) {
            System.out.println(s[i]);
        }
    }
}

```
Este código es fundamental para principiantes porque introduce el uso de BigDecimal para manejar números con precisión absoluta, evitando los errores de redondeo comunes en tipos como double o float.

## Comprobación por HackerRank

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1494512379105509467/1498112458458665121/image.png?ex=69eff973&is=69eea7f3&hm=0c3a919c4e8d8ee2797cc79ebf2af5577dfd720f60492846e9c888233c9adddc&" alt="Ejercicio 12">
</div>

<p align="right">
  <a href="PortadaEjercicios.md">Volver a la página principal</a>
</p>
