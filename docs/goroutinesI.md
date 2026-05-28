# 🚀 Concorrência I: Goroutines

# 📘 Introdução

As Goroutines são uma das funcionalidades mais poderosas da linguagem Go.

Elas permitem executar múltiplas tarefas ao mesmo tempo de forma simples e eficiente.

---

# 🧠 O que é Concorrência?

Concorrência é a capacidade de executar várias tarefas simultaneamente.

Exemplos:

* 📥 baixar arquivos
* 🌐 responder usuários
* 🛒 processar pedidos
* ⚡ executar APIs

---

# 🔥 O que é uma Goroutine?

Uma Goroutine é uma função executada concorrentemente.

Para criar uma Goroutine usamos a palavra:

```go
go
```

---

# 📌 Exemplo Básico

```go
package main

import (
    "fmt"
    "time"
)

func mensagem() {

    fmt.Println("Executando Goroutine")

}

func main() {

    go mensagem()

    time.Sleep(time.Second)

}
```

---

# 🔍 Explicação

| Código             | Função                         |
| ------------------ | ------------------------------ |
| 🚀 `go mensagem()` | Executa a função em paralelo   |
| ⏱️ `time.Sleep()`  | Dá tempo da goroutine executar |

---

# ⚠️ Importante

!!! warning

```
⚠️ Se o programa terminar antes da goroutine finalizar, ela será encerrada automaticamente.
```

---

# 📌 Executando várias Goroutines

```go
package main

import (
    "fmt"
    "time"
)

func tarefa(nome string) {

    for i := 1; i <= 3; i++ {

        fmt.Println(nome, "-", i)

        time.Sleep(time.Millisecond * 500)

    }

}

func main() {

    go tarefa("Goroutine 1")
    go tarefa("Goroutine 2")

    time.Sleep(time.Second * 3)

}
```

---

# 🎯 O que acontece?

As duas tarefas executam juntas.

A saída pode aparecer misturada:

```plaintext
Goroutine 1 - 1
Goroutine 2 - 1
Goroutine 1 - 2
Goroutine 2 - 2
```

Isso acontece porque ambas estão rodando simultaneamente.

---

# 🛠️ Vantagens das Goroutines

| Vantagem      | Benefício              |
| ------------- | ---------------------- |
| ⚡ Leves       | Consomem pouca memória |
| 🚀 Rápidas    | Alta performance       |
| 🧩 Simples    | Fácil implementação    |
| 📈 Escaláveis | Ótimas para servidores |

---

# 📦 Exemplo Simulando Download

```go
package main

import (
    "fmt"
    "time"
)

func download(arquivo string) {

    fmt.Println("Baixando:", arquivo)

    time.Sleep(time.Second * 2)

    fmt.Println("Download finalizado:", arquivo)

}

func main() {

    go download("video.mp4")
    go download("imagem.png")

    time.Sleep(time.Second * 5)

}
```

---

# 💡 Quando usar Goroutines?

As Goroutines são muito utilizadas em:

* 🌐 APIs REST
* ⚙️ Microsserviços
* 📡 Sistemas distribuídos
* 🚀 Processamento paralelo
* 📥 Upload e download de arquivos

---

# ⚠️ Cuidados

!!! warning

```
⚠️ Muitas Goroutines sem controle podem causar problemas de memória e concorrência.
```

---

# ✅ Boa prática

!!! note

```
🧠 Utilize Goroutines apenas quando realmente houver necessidade de concorrência.
```

---

# 📋 Comparação

| Sem Goroutines             | Com Goroutines         |
| -------------------------- | ---------------------- |
| Executa uma tarefa por vez | Executa várias tarefas |
| Mais lento                 | Mais rápido            |
| Menor complexidade         | Maior performance      |

---

# 🚀 Exemplo Completo

```go
package main

import (
    "fmt"
    "time"
)

func contador(nome string) {

    for i := 1; i <= 5; i++ {

        fmt.Println(nome, i)

        time.Sleep(time.Millisecond * 300)

    }

}

func main() {

    go contador("A")
    go contador("B")

    time.Sleep(time.Second * 3)

    fmt.Println("Programa finalizado")

}
```

---

# ✅ Conclusão

As Goroutines tornam o Go extremamente poderoso para aplicações modernas.

Com poucas linhas de código é possível:

* ⚡ executar tarefas paralelas
* 🚀 aumentar performance
* 📈 melhorar escalabilidade
* 🌐 criar aplicações robustas

Elas são um dos principais motivos da popularidade do Go no desenvolvimento backend.
