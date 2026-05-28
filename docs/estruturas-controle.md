# 🔀 Estruturas de Controle em Go

## 📘 Introdução

As estruturas de controle são utilizadas para controlar o fluxo de execução do programa.

Em Go, as principais estruturas são:

* 🔹 `if`
* 🔁 `for`
* 🔀 `switch`

---

# ✅ Estrutura If

O `if` é utilizado para executar uma condição.

## 🧪 Exemplo simples

```go
package main

import "fmt"

func main() {

    idade := 18

    if idade >= 18 {
        fmt.Println("Maior de idade")
    }

}
```

---

## 🔄 If e Else

```go
package main

import "fmt"

func main() {

    numero := 10

    if numero % 2 == 0 {
        fmt.Println("Número par")
    } else {
        fmt.Println("Número ímpar")
    }

}
```

---

## 📊 If, Else If e Else

```go
package main

import "fmt"

func main() {

    nota := 7

    if nota >= 9 {
        fmt.Println("Excelente")
    } else if nota >= 6 {
        fmt.Println("Aprovado")
    } else {
        fmt.Println("Reprovado")
    }

}
```

---

# 🔁 Estrutura For

Em Go existe apenas a estrutura `for` para repetição.

---

## 🧮 For tradicional

```go
package main

import "fmt"

func main() {

    for i := 1; i <= 5; i++ {
        fmt.Println(i)
    }

}
```

---

## 🔄 For como While

```go
package main

import "fmt"

func main() {

    contador := 0

    for contador < 5 {
        fmt.Println(contador)
        contador++
    }

}
```

---

## ♾️ Loop infinito

```go
for {
    fmt.Println("Executando...")
}
```

!!! warning

```
⚠️ Loops infinitos podem travar o programa se não houver controle.
```

---

# 🔀 Estrutura Switch

O `switch` é utilizado para múltiplas condições.

---

## 🧪 Exemplo básico

```go
package main

import "fmt"

func main() {

    dia := 3

    switch dia {

    case 1:
        fmt.Println("Domingo")

    case 2:
        fmt.Println("Segunda")

    case 3:
        fmt.Println("Terça")

    default:
        fmt.Println("Dia inválido")

    }

}
```

---

## 🧠 Switch sem condição

```go
package main

import "fmt"

func main() {

    idade := 20

    switch {

    case idade >= 18:
        fmt.Println("Maior de idade")

    default:
        fmt.Println("Menor de idade")

    }

}
```

---

# 📋 Comparação das Estruturas

| Estrutura   | Função                        |
| ----------- | ----------------------------- |
| ✅ `if`      | Executar condições            |
| 🔁 `for`    | Criar repetições              |
| 🔀 `switch` | Trabalhar com múltiplos casos |

---

# 🏁 Conclusão

As estruturas de controle são fundamentais em Go para tomada de decisões e repetição de tarefas.
