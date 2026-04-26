# Ejercicio 3 (Java Output Formatting)

De Java Sistema.out.printf La función se puede utilizar para imprimir una salida formateada. El propósito de este ejercicio es poner a prueba su comprensión del formato de salida utilizando printf.

## Descripción

-Formato de entrada

Cada línea de entrada contendrá un Cadena seguido de un entero.
Cada Cadena tendrá un máximo de 10 caracteres alfabéticos, y cada uno entero estará en el rango inclusivo de 0to 999.

-Formato de salida

En cada línea de salida debe haber dos columnas:

La primera columna contiene el Cadena y se deja justificado utilizando exactamente 15 personajes.
La segunda columna contiene el entero, expresado exactamente 3 dígitos; si la entrada original tiene menos de tres dígitos, debe rellenar los dígitos iniciales de su salida con ceros.


## Datos de Entrada y Salida

| N° | Dato de Entrada | Dato de Salida |
| :---: | :---: | :---: |
| 1 | java 100 <br> cpp 65 <br> python 50 | java       100 <br> cpp        065 <br> python     050  |


## Código Fuente

```
//Julián Merino
import java.util.Scanner;

public class Solucion {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("================================");
        for (int i = 0; i < 3; i++) {
            String s1 = sc.next();
            int x = sc.nextInt();
            // Formateo de salida: 15 caracteres para texto y 3 dígitos con ceros para enteros
            System.out.printf("%-15s%03d%n", s1, x);
        }
        System.out.println("================================");
    }
}

```
Este código es fundamental para principiantes porque introduce el manejo de salida con formato mediante printf, una herramienta potente que permite alinear columnas de texto y rellenar números con ceros automáticamente sin recurrir a complejas concatenaciones manuales.

## Comprobación por HackerRank

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1494512379105509467/1498084562285236245/image.png?ex=69efdf78&is=69ee8df8&hm=2d169f0a1b4b5b8e1b82be592a19b70670212800252627dfbf8867de64b2db95&" alt="Ejercicio 3">
</div>
