# 🚀 Introdução e Instalação do Go

## 📘 O que é Go?

Go (ou Golang) é uma linguagem de programação criada pelo Google.

Ela foi desenvolvida para ser:

* ✅ simples
* ⚡ rápida
* 🛠️ eficiente
* 🔄 concorrente
* 📚 fácil de manter

Go é muito utilizada em:

* 🌐 APIs
* 🧩 microsserviços
* ☁️ cloud computing
* ⚙️ DevOps
* 🔗 sistemas distribuídos

---

# 💻 Instalação do Go

## 🪟 Windows

1. 🌍 Acesse o site oficial:

[Go Downloads](https://go.dev/dl/?utm_source=chatgpt.com)

2. 📥 Baixe o instalador do Windows.

3. ▶️ Execute o instalador.

4. 🖥️ Verifique a instalação no terminal:

```bash id="m3w7os"
go version
```

---

## 🐧 Linux (Ubuntu)

Atualize os pacotes:

```bash id="f3p0d4"
sudo apt update
```

Instale o Go:

```bash id="m8u3y6"
sudo apt install golang-go -y
```

Verifique a instalação:

```bash id="r5z9x1"
go version
```

---

## 🍎 macOS

Instale utilizando Homebrew:

```bash id="k9t1q2"
brew install go
```

Verifique:

```bash id="w2c8n7"
go version
```

---

# 👨‍💻 Primeiro Programa em Go

Crie um arquivo chamado `main.go`:

```go id="u4f8m3"
package main

import "fmt"

func main() {
    fmt.Println("Olá Mundo!")
}
```

Execute:

```bash id="d6r2v9"
go run main.go
```

Resultado esperado:

```bash id="n1x5p7"
Olá Mundo!
```

---

# ⭐ Vantagens do Go

| Vantagem           | Descrição                     |
| ------------------ | ----------------------------- |
| ✅ Simples          | Sintaxe limpa                 |
| ⚡ Performance      | Muito rápida                  |
| 🔄 Concorrência    | Suporte nativo com goroutines |
| 🏗️ Compilada      | Gera executáveis rápidos      |
| 🌎 Multiplataforma | Funciona em vários sistemas   |

---

# 🏁 Conclusão

Go é uma linguagem moderna, eficiente e muito utilizada no mercado atualmente.
