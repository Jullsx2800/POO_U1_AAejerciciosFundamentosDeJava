# Ejercicio 10 (Date and Time in Java )

El Clase de calendario es una clase abstracta que proporciona métodos para convertir entre un instante específico en el tiempo y un conjunto de campos de calendario como AÑO, MES, DÍA_DE_MES, HORA, etc.

## Descripción

-Formato de entrada

Una única línea de entrada que contiene el espacio separado mes, día y año, respectivamente, en MM/DD/YYYY formato.

-Restricciones

2000 < year < 3000


-Formato de salida

cadena: El día de la semana en letras mayúsculas


## Datos de Entrada y Salida

| N° | Dato de Entrada | Dato de Salida |
| :---: | :---: | :---: |
| 1 | 08 05 2015 | WEDNESDAY |

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

class Result {
    public static String findDay(int month, int day, int year) {
        Calendar Cal = Calendar.getInstance();
        Cal.set(year, month - 1, day);
        return Cal.getDisplayName(Calendar.DAY_OF_WEEK, Calendar.LONG, Locale.US).toUpperCase();
    }
}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        String[] firstMultipleInput = bufferedReader.readLine().replaceAll("\\s+$", "").split(" ");

        int month = Integer.parseInt(firstMultipleInput[0]);
        int day = Integer.parseInt(firstMultipleInput[1]);
        int year = Integer.parseInt(firstMultipleInput[2]);

        String res = Result.findDay(month, day, year);

        bufferedWriter.write(res);
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}

```
Este código es superior para principiantes porque utiliza la clase Calendar, una herramienta estándar de Java que automatiza cálculos temporales complejos, como años bisiestos y la duración variable de los meses, evitando errores manuales de lógica matemática.

## Comprobación por HackerRank

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1494512379105509467/1498115326724931624/image.png?ex=69effc1f&is=69eeaa9f&hm=551822b0c842313424f7f1b57ccbda88d1172becdfb6cce47939f97e4a350e00&" alt="Ejercicio 10">
</div>

<p align="right">
  <a href="PortadaEjercicios.md">Volver a la página principal</a>
</p>
