# 📡 Concorrência II: Channels

Channels (canais) são mecanismos utilizados em Go para permitir comunicação segura entre Goroutines.

Enquanto Goroutines executam tarefas simultaneamente, os Channels são responsáveis por trocar informações entre elas.

---

## 📌 Criando um Channel

Um channel é criado utilizando a função `make()`:

```go
package main

import "fmt"

func main() {

	canal := make(chan string)

	go func() {
		canal <- "Olá do Channel"
	}()

	mensagem := <- canal

	fmt.Println(mensagem)

}
```

---

## 🔎 Como funciona

No exemplo anterior:

📤 `canal <- "Olá do Channel"`

Envia uma informação para o canal.

📥 `mensagem := <- canal`

Recebe uma informação do canal.

---

## 🚀 Exemplo com múltiplas mensagens

```go
package main

import "fmt"

func enviarMensagem(canal chan string){

	canal <- "Primeira mensagem"

	canal <- "Segunda mensagem"

}

func main(){

	canal := make(chan string)

	go enviarMensagem(canal)

	fmt.Println(<-canal)

	fmt.Println(<-canal)

}
```

---

## ⚠️ Channels com Buffer

Channels podem armazenar uma quantidade limitada de dados sem bloquear imediatamente a execução.

Exemplo:

```go
package main

import "fmt"

func main(){

	canal := make(chan string,2)

	canal <- "Mensagem 1"

	canal <- "Mensagem 2"

	fmt.Println(<-canal)

	fmt.Println(<-canal)

}
```

Neste exemplo:

- `2` representa a capacidade do canal
- duas mensagens podem ser armazenadas antes do bloqueio

---

## 📋 Boas práticas

✅ Utilizar channels para comunicação entre Goroutines  
✅ Evitar excesso de Goroutines desnecessárias  
✅ Fechar channels quando não forem mais utilizados  
✅ Utilizar buffer apenas quando necessário  

---

## 📊 Comparação

| Recurso | Função |
|----------|----------|
| `make(chan tipo)` | Cria um channel |
| `canal <- valor` | Envia valor |
| `<-canal` | Recebe valor |
| `close(canal)` | Fecha o channel |
| `make(chan tipo, n)` | Cria channel com buffer |

---

## 💡 Conclusão

Channels tornam a comunicação entre Goroutines mais segura e organizada. Eles ajudam a evitar problemas de concorrência e tornam o código mais fácil de manter.
