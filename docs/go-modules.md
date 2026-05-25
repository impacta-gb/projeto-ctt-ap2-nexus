# 📦 Gerenciamento de Pacotes em Go (Go Modules)

# 🚀 Introdução

Go Modules é o sistema oficial de gerenciamento de dependências do Go.

Ele permite organizar, versionar e instalar bibliotecas externas de forma simples.

---

# 📌 O que é um módulo?

Um módulo é um conjunto de pacotes Go versionados juntos.

Ele é definido pelo arquivo:

```plaintext
go.mod
```

---

# 🧱 Criando um módulo

Para iniciar um projeto em Go:

```bash
go mod init nome-do-projeto
```

## Exemplo:

```bash
go mod init api-loja
```

---

# 📄 Arquivo go.mod

Depois de criar o módulo, o arquivo será gerado:

```go
module api-loja

go 1.21
```

---

# 📥 Instalando dependências

Quando você importa uma biblioteca externa, o Go baixa automaticamente.

Exemplo:

```go
import "github.com/gin-gonic/gin"
```

Depois execute:

```bash
go mod tidy
```

---

# 🔍 O que o go mod tidy faz?

| Comando | Função |
|---|---|
| go mod tidy | remove dependências não usadas |
| go mod tidy | baixa dependências faltantes |

---

# 📦 Exemplo prático

```go
package main

import (
    "fmt"
    "github.com/google/uuid"
)

func main() {

    id := uuid.New()

    fmt.Println("ID gerado:", id)

}
```

---

# ⚠️ Importante

!!! warning

    Se você não rodar `go mod tidy`, o projeto pode ficar com dependências quebradas.

---

# 🧠 Estrutura do projeto

```plaintext
meu-projeto/
 ├── go.mod
 ├── go.sum
 ├── main.go
 └── handlers/
```

---

# 📌 go.sum

Esse arquivo guarda o hash das dependências instaladas.

Ele garante segurança e integridade.

---

# 🔄 Atualizando dependências

Para atualizar uma dependência:

```bash
go get -u nome-da-biblioteca
```

---

# 🧪 Removendo dependências

Se não estiver usando mais:

```bash
go mod tidy
```

---

# 💡 Vantagens do Go Modules

- controle de versões 📌
- dependências organizadas 📦
- projetos mais seguros 🔐
- fácil replicação em outros ambientes 🚀

---

# 🧠 Comparação

| Sem Go Modules | Com Go Modules |
|---|---|
| dependências manuais | automáticas |
| difícil controle | versionado |
| erros frequentes | mais seguro |

---

# 🚀 Exemplo completo

```go
package main

import (
    "fmt"
    "github.com/google/uuid"
)

func main() {

    fmt.Println("Projeto com Go Modules")

    fmt.Println("UUID:", uuid.New())

}
```

---

# 🎯 Conclusão

Go Modules é essencial para qualquer projeto Go moderno.

Ele garante organização, segurança e facilidade no gerenciamento de bibliotecas.
