# Sintaxe Básica e Variáveis

## Introdução

A linguagem Go (Golang) possui uma sintaxe simples, limpa e fácil de aprender. Seu objetivo é oferecer alto desempenho e facilitar a manutenção do código.

---

## Estrutura básica de um programa Go

Todo programa em Go começa declarando o pacote principal (`package main`) e a função principal (`main()`).

```go
package main

import "fmt"

func main() {
    fmt.Println("Olá Mundo")
}
```

### Explicação

| Comando | Função |
|----------|---------|
| package main | Define o pacote principal |
| import | Importa bibliotecas |
| func main() | Função principal |
| fmt.Println() | Exibe algo na tela |

---

## Declaração de variáveis

Em Go existem diferentes maneiras de declarar variáveis.

### Forma tradicional

```go
var nome string = "João"
```

---

### Inferência automática de tipo

O Go consegue descobrir o tipo automaticamente.

```go
var idade = 20
```

---

### Declaração curta

A forma mais usada em Go:

```go
cidade := "São Paulo"
```

---

## Tipos básicos

| Tipo | Exemplo |
|-------|----------|
| int | 10 |
| float64 | 15.7 |
| string | "Texto" |
| bool | true |

---

## Exemplo completo

```go
package main

import "fmt"

func main() {

    nome := "João"
    idade := 20
    altura := 1.80
    estudante := true

    fmt.Println(nome)
    fmt.Println(idade)
    fmt.Println(altura)
    fmt.Println(estudante)

}
```

!!! warning

    Variáveis declaradas e não utilizadas geram erro em Go.

!!! note

    A declaração curta usando := só pode ser utilizada dentro de funções.
