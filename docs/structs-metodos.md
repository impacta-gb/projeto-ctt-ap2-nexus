# 🧱 Structs e Métodos em Go

# 📖 Introdução

Em Go, as `structs` são utilizadas para agrupar diferentes tipos de dados em uma única estrutura.

Elas funcionam de forma parecida com "objetos" em outras linguagens.

Já os **métodos** permitem adicionar comportamentos para essas structs.

---

# 🧱 O que é uma Struct?

Uma struct é um conjunto de campos (atributos).

## 🧪 Exemplo básico

```go
package main

import "fmt"

type Pessoa struct {
    Nome  string
    Idade int
}

func main() {

    pessoa1 := Pessoa{
        Nome:  "João",
        Idade: 20,
    }

    fmt.Println(pessoa1)

}
```

---

# 🔍 Explicando o código

| Parte                   | Função                   |
| ----------------------- | ------------------------ |
| 🧱 `type Pessoa struct` | Cria uma struct          |
| 📝 `Nome string`        | Campo do tipo texto      |
| 🔢 `Idade int`          | Campo numérico           |
| 📦 `Pessoa{}`           | Cria um objeto da struct |

---

# 🎯 Acessando campos da Struct

Podemos acessar os valores usando `.`

## 🧪 Exemplo

```go
package main

import "fmt"

type Pessoa struct {
    Nome  string
    Idade int
}

func main() {

    pessoa1 := Pessoa{
        Nome:  "Maria",
        Idade: 25,
    }

    fmt.Println(pessoa1.Nome)
    fmt.Println(pessoa1.Idade)

}
```

---

# ✏️ Alterando valores

Os valores também podem ser modificados.

```go
package main

import "fmt"

type Pessoa struct {
    Nome  string
    Idade int
}

func main() {

    pessoa1 := Pessoa{
        Nome:  "Carlos",
        Idade: 18,
    }

    pessoa1.Idade = 19

    fmt.Println(pessoa1)

}
```

---

# 🛠️ O que são Métodos?

Métodos são funções associadas a uma struct.

Eles permitem criar comportamentos específicos.

---

# 🚗 Exemplo de Método

```go
package main

import "fmt"

type Carro struct {
    Marca string
    Ano   int
}

func (c Carro) ExibirInformacoes() {

    fmt.Println("Marca:", c.Marca)
    fmt.Println("Ano:", c.Ano)

}

func main() {

    carro1 := Carro{
        Marca: "Toyota",
        Ano:   2024,
    }

    carro1.ExibirInformacoes()

}
```

---

# 🔍 Explicação do Método

| Código                    | Significado               |
| ------------------------- | ------------------------- |
| ⚙️ `func (c Carro)`       | Método ligado à struct    |
| 🏷️ `ExibirInformacoes()` | Nome do método            |
| 📦 `c.Marca`              | Acessa atributo da struct |

---

# 📦 Struct com vários campos

```go
package main

import "fmt"

type Produto struct {
    Nome    string
    Preco   float64
    Estoque int
}

func main() {

    produto1 := Produto{
        Nome:    "Notebook",
        Preco:   3500.99,
        Estoque: 10,
    }

    fmt.Println(produto1)

}
```

---

# 💸 Método para calcular desconto

```go
package main

import "fmt"

type Produto struct {
    Nome  string
    Preco float64
}

func (p Produto) Desconto() float64 {

    return p.Preco * 0.9

}

func main() {

    produto := Produto{
        Nome:  "Mouse Gamer",
        Preco: 200,
    }

    fmt.Println("Preço com desconto:")
    fmt.Println(produto.Desconto())

}
```

---

# ⚠️ Atenção

!!! warning

```
⚠️ Structs ajudam muito na organização do código, mas criar structs gigantes pode dificultar a manutenção.
```

---

# 💡 Boa prática

!!! note

```
🧠 Use nomes claros e objetivos para structs e métodos.
```

---

# 📋 Comparação rápida

| Conceito  | Função               |
| --------- | -------------------- |
| 🧱 Struct | Armazena dados       |
| ⚙️ Método | Executa ações        |
| 📦 Campo  | Informação da struct |

---

# 🚀 Exemplo Completo

```go
package main

import "fmt"

type Usuario struct {
    Nome  string
    Email string
}

func (u Usuario) Apresentar() {

    fmt.Println("Usuário:", u.Nome)
    fmt.Println("Email:", u.Email)

}

func main() {

    usuario1 := Usuario{
        Nome:  "Ana",
        Email: "ana@email.com",
    }

    usuario1.Apresentar()

}
```

---

# ✅ Conclusão

As `structs` e os `métodos` são fundamentais em Go.

Com eles é possível:

* 📦 organizar dados
* ♻️ reutilizar código
* 🧹 criar sistemas mais limpos
* 🔧 facilitar manutenção

Eles são extremamente utilizados em APIs, sistemas web e aplicações profissionais.
