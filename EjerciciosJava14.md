# Ejercicio 14 (Java Comparator)

Los comparadores se utilizan para comparar dos objetos. En este desafío, crearás un comparador y lo usarás para ordenar una matriz.

## Descripción

-Formato de entrada

La entrada desde stdin se maneja mediante el código stub bloqueado en el Solución clase.

La primera línea contiene un número entero, n , que indica el número de jugadores.
Cada uno de los n.Las líneas subsiguientes contienen la información de un jugador name y score, respectivamente.

-Restricciones

0 <= score <= 1000

2 Los jugadores pueden tener el mismo nombre.

Los nombres de los jugadores constan de letras minúsculas en inglés.

-Formato de salida

No es responsable de imprimir ninguna salida en stdout. El código auxiliar bloqueado en Solución creará un Comprobador objeto, úselo para ordenar el Jugador matriz e imprimir cada elemento ordenado.


## Datos de Entrada y Salida

| N° | Dato de Entrada | Dato de Salida |
| :---: | :---: | :---: |
| 1 | 5 <br> amy 100 <br> david 100 <br> heraldo 50 <br> aakansha 75 <br> aleksa 150 | aleksa 150 <br> amy 100 <br> david 100 <br> aakansha 75 <br> heraldo 50 |


## Código Fuente

```
//Julian Merino
import java.util.*;

class Checker implements Comparator<Player> {
    @Override
    public int compare(Player a, Player b) {
        if (a.score == b.score) {
            return a.name.compareTo(b.name);
        }
        return Integer.compare(b.score, a.score);
    }
}

class Player {
    String name;
    int score;

    Player(String name, int score) {
        this.name = name;
        this.score = score;
    }
}

class Solution {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int n = scan.nextInt();

        Player[] player = new Player[n];
        Checker checker = new Checker();

        for (int i = 0; i < n; i++) {
            player[i] = new Player(scan.next(), scan.nextInt());
        }
        scan.close();

        Arrays.sort(player, checker);
        for (int i = 0; i < player.length; i++) {
            System.out.printf("%s %s\n", player[i].name, player[i].score);
        }
    }
}

```
Este código es fundamental para principiantes porque introduce el manejo de objetos personalizados y la interfaz Comparator, permitiendo definir criterios de ordenamiento complejos (como jerarquías de puntajes y orden alfabético simultáneo) que superan las limitaciones de los arreglos simples.

## Comprobación por HackerRank

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1494512379105509467/1498119737547292803/image.png?ex=69f0003b&is=69eeaebb&hm=719e2634fb84da7dddaae09a578dce60a77570bf76355dafd828c6fee1cf7462&" alt="Ejercicio 14">
</div>
