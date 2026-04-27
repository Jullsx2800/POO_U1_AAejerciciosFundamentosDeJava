# Ejercicio 15 (Java Dequeue)

En informática, una cola de doble extremo (dequeue, a menudo abreviado como deque, pronunciado deck) es un tipo de datos abstracto que generaliza una cola, para la cual se pueden agregar o eliminar elementos del frente (cabeza) o de la parte posterior (cola).

## Descripción

-Formato de entrada

La primera línea de entrada contiene dos números enteros N y M: representa el número total de números enteros y el tamaño de la submatriz, respectivamente. La siguiente línea contiene N números enteros separados por espacios.

-Restricciones

1 <= N <= 100000

1 <= M <= 100000

M <= N

-Formato de salida

Imprimir el máximo Número de números enteros únicos entre todas las posibles submatrices contiguas de tamaño M

## Datos de Entrada y Salida

| N° | Dato de Entrada | Dato de Salida |
| :---: | :---: | :---: |
| 1 | 6 3 <br> 5 3 5 2 3 2 | 3 |


## Código Fuente

```
//Julian Merino
import java.util.*;

public class test {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        Deque<Integer> deque = new ArrayDeque<>();
        HashMap<Integer, Integer> frequencyMap = new HashMap<>();
        
        int n = in.nextInt();
        int m = in.nextInt();
        int maxUnique = 0;

        for (int i = 0; i < n; i++) {
            int num = in.nextInt();

            deque.addLast(num);
            frequencyMap.put(num, frequencyMap.getOrDefault(num, 0) + 1);

            if (deque.size() == m) {
                if (frequencyMap.size() > maxUnique) {
                    maxUnique = frequencyMap.size();
                }

                if (maxUnique == m) {
                    break;
                }

                int oldest = deque.removeFirst();
                int count = frequencyMap.get(oldest);

                if (count == 1) {
                    frequencyMap.remove(oldest);
                } else {
                    frequencyMap.put(oldest, count - 1);
                }
            }
        }
        System.out.println(maxUnique);
        in.close();
    }
}

```

Este código es una herramienta excelente para principiantes porque introduce de manera práctica el algoritmo de ventana deslizante (Sliding Window) y el uso avanzado del Java Collections Framework, específicamente Deque y HashMap.

## Comprobación por HackerRank

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1494512379105509467/1498121782303916114/image.png?ex=69f00222&is=69eeb0a2&hm=a543ae586c51fcc02715d9fa6a8d30a12949870e0210e588e2b424bca060d23b&" alt="Ejercicio 15">
</div>

<p align="right">
  <a href="PortadaEjercicios.md">Volver a la página principal</a>
</p>
