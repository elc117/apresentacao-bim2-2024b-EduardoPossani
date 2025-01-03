# apresentacao-bim2-2024b-EduardoPossani
apresentacao-bim2-2024b-EduardoPossani created by GitHub Classroom


# Exceções *Checked* e *Unchecked* em Java

Este repositório aborda as diferenças entre exceções *checked* e *unchecked* em Java, com exemplos para facilitar o entendimento.

## 📖 O que são Exceções em Java?

Exceções em Java são eventos que podem alterar o fluxo normal de execução de um programa. Elas são usadas para indicar problemas que ocorrem durante a execução de um programa, como erros de entrada/saída, operações matemáticas inválidas ou falhas em conexões de rede.

Em Java, as exceções são divididas em duas categorias principais:

- **Exceções *Checked***
- **Exceções *Unchecked***

---

## 🔍 Exceções *Checked*

As exceções *checked* são verificadas pelo compilador em tempo de compilação. Isso significa que o programador é obrigado a tratar essas exceções usando um bloco `try-catch` ou a declará-las no método com a palavra-chave `throws`.

### Exemplos de Exceções *Checked*
- `IOException`
- `SQLException`
- `FileNotFoundException`

### Características
- São derivadas diretamente da classe `Exception` (exceto `RuntimeException` e suas subclasses).
- O tratamento é obrigatório no momento da compilação.

#### Exemplo em Código
```java
import java.io.File;
import java.io.FileReader;
import java.io.IOException;

public class CheckedExample {
    public static void main(String[] args) {
        try {
            File file = new File("arquivo.txt");
            FileReader fr = new FileReader(file);
        } catch (IOException e) {
            System.out.println("Arquivo não encontrado: " + e.getMessage());
        }
    }
}
```
## 🔍 Exceções Unchecked
As exceções unchecked não são verificadas pelo compilador. Elas ocorrem normalmente devido a erros de lógica no programa e podem ser evitadas com código adequado.

Exemplos de Exceções Unchecked
ArithmeticException
NullPointerException
ArrayIndexOutOfBoundsException
Características
São derivadas da classe RuntimeException.
O tratamento não é obrigatório, mas é recomendado para melhorar a robustez do programa.
Exemplo em Código
```java

public class UncheckedExample {
    public static void main(String[] args) {
        int[] numeros = {1, 2, 3};
        System.out.println(numeros[5]); // Gera uma ArrayIndexOutOfBoundsException
    }
}
```
## Diferenças entre Checked e Unchecked Exceptions

| **Aspecto**             | **Checked Exceptions**                             | **Unchecked Exceptions**                      |
|--------------------------|---------------------------------------------------|-----------------------------------------------|
| **Herança**              | Subclasse de `Exception` (exceto `RuntimeException`) | Subclasse de `RuntimeException`             |
| **Obrigação de Tratamento** | O compilador exige tratamento ou declaração         | Não exige tratamento ou declaração          |
| **Causa Comum**          | Erros externos (ex.: falhas de I/O)               | Erros de lógica ou programação               |

## 📚 Referências
Documentação Oficial do Java - Exceções
Java Exception Handling
Oracle Java Tutorials - Exceptions






