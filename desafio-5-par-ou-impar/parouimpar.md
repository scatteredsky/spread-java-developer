# Desafio de Código: Par ou Ímpar

## Desafio

Leia um valor inteiro N. Este valor será a quantidade de valores que serão lidos em seguida. Para cada valor lido, mostre uma mensagem em inglês dizendo se este valor lido é par (EVEN), ímpar (ODD), positivo (POSITIVE) ou negativo (NEGATIVE). No caso do valor ser igual a zero (0), embora a descrição correta seja (EVEN NULL), pois por definição zero é par, seu programa deverá imprimir apenas NULL

## Entrada

A primeira linha da entrada contém um valor inteiro N(N < 10000) que indica o número de casos de teste. Cada caso de teste a seguir é um valor inteiro X (-107 < X <107).

## Saída

Para cada caso, imprima uma mensagem correspondente, de acordo com o exemplo abaixo. Todas as letras deverão ser maiúsculas e sempre deverá haver um espaço entre duas palavras impressas na mesma linha.

| **Exemplos de Entrada** | **Exemplos de Saída** |
|:-----------------------:|:------------------------:|
| 4                       | ODD NEGATIVE             |
| -5                      | NULL                     |
| 0                       | ODD POSITIVE             |
| 3                       | EVEN NEGATIVE            |
| -4                      |                          |

### Exercício Resolvido: _Par ou Ímpar_

```java
import java.io.IOException;
import java.util.Scanner;

public class Problem {

    public static void main(String[] args) throws IOException {
        Scanner leitor = new Scanner(System.in);
        int N = leitor.nextInt();
        for (int i = 0; i < N; i++) {

          int number = leitor.nextInt();

        String evenOrOdd, positiveNegative, result;

        evenOrOdd = (number%2==0) ? "EVEN" : "ODD";
        positiveNegative = (number > 0) ? "POSITIVE" : "NEGATIVE";
        result = (number==0) ? "NULL" : evenOrOdd+" "+positiveNegative;

        System.out.println(result);

        }
    leitor.close();
    }
}
```
