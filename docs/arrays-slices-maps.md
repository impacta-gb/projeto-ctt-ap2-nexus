# 📦 Arrays, Slices e Maps

## 📖 Introdução

Go possui estruturas importantes para armazenar conjuntos de dados.

As principais são:

- 📌 Arrays → tamanho fixo
- 📌 Slices → tamanho dinâmico
- 📌 Maps → estrutura chave-valor

Cada uma possui características específicas e usos diferentes.

---

## 🔹 Arrays

Arrays possuem tamanho definido e não podem ser alterados após serem criados.

### 💻 Exemplo:

```go
package main

import "fmt"

func main() {

    numeros := [5]int{10,20,30,40,50}

    fmt.Println(numeros)

}
```

### 📤 Saída:

```text
[10 20 30 40 50]
```

### 📋 Características

| Característica | Descrição |
|---|---|
| 📏 Tamanho | Fixo |
| 🔢 Índice | Começa em 0 |
| 🧩 Tipo | Todos elementos devem ser iguais |

---

## 🔹 Slices

Slices funcionam como arrays dinâmicos.

### 💻 Exemplo:

```go
package main

import "fmt"

func main() {

    nomes := []string{"Ana","Carlos","Pedro"}

    nomes = append(nomes,"Maria")

    fmt.Println(nomes)

}
```

### 📤 Saída:

```text
[Ana Carlos Pedro Maria]
```

### 📋 Funções principais

| Função | Descrição |
|---|---|
| ➕ append() | Adiciona elementos |
| 📐 len() | Retorna quantidade |
| 📦 cap() | Retorna capacidade |

!!! warning "⚠️ Atenção"

    Slices aumentam dinamicamente e podem gerar novas alocações de memória.

---

## 🔹 Maps

Maps armazenam dados usando pares de chave e valor.

### 💻 Exemplo:

```go
package main

import "fmt"

func main() {

    aluno := map[string]int{

        "João":8,
        "Maria":10,

    }

    fmt.Println(aluno)

}
```

### 📤 Saída:

```text
map[João:8 Maria:10]
```

### 📋 Operações comuns

| Operação | Exemplo |
|---|---|
| ➕ Inserir | mapa["Pedro"]=9 |
| 🔍 Ler | mapa["João"] |
| ❌ Remover | delete(mapa,"João") |

---

## 📊 Diferenças entre Arrays, Slices e Maps

| Estrutura | Tamanho | Uso |
|---|---|---|
| 📦 Arrays | Fixo | Quantidade conhecida |
| 📜 Slices | Dinâmico | Listas variáveis |
| 🗂️ Maps | Dinâmico | Associação chave-valor |

---

## ✅ Conclusão

- 📦 Arrays → tamanho fixo
- 📜 Slices → tamanho flexível
- 🗂️ Maps → associação chave-valor

Cada estrutura é utilizada em situações diferentes e ajuda a organizar dados de forma eficiente.
