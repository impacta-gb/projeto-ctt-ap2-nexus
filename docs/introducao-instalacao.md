# Introdução e Instalação do Go

## O que é Go?

Go (ou Golang) é uma linguagem de programação criada pelo Google.

Ela foi desenvolvida para ser:

- simples
- rápida
- eficiente
- concorrente
- fácil de manter

Go é muito utilizada em:

- APIs
- microsserviços
- cloud computing
- DevOps
- sistemas distribuídos

---

# Instalação do Go

## Windows

1. Acesse o site oficial:

https://go.dev/dl/

2. Baixe o instalador do Windows.

3. Execute o instalador.

4. Verifique a instalação no terminal:

```bash
go version
```

---

## Linux (Ubuntu)

Atualize os pacotes:

```bash
sudo apt update
```

Instale o Go:

```bash
sudo apt install golang-go -y
```

Verifique a instalação:

```bash
go version
```

---

## macOS

Instale utilizando Homebrew:

```bash
brew install go
```

Verifique:

```bash
go version
```

---

# Primeiro Programa em Go

Crie um arquivo chamado main.go:

```go
package main

import "fmt"

func main() {
    fmt.Println("Olá Mundo!")
}
```

Execute:

```bash
go run main.go
```

Resultado esperado:

```bash
Olá Mundo!
```

---

# Vantagens do Go

| Vantagem | Descrição |
|---|---|
| Simples | Sintaxe limpa |
| Performance | Muito rápida |
| Concorrência | Suporte nativo com goroutines |
| Compilada | Gera executáveis rápidos |
| Multiplataforma | Funciona em vários sistemas |

---

# Conclusão

Go é uma linguagem moderna, eficiente e muito utilizada no mercado atualmente.
