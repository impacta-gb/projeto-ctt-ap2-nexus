# 🚨 Tratamento de Erros (Error Handling)

Erros são situações inesperadas que podem ocorrer durante a execução de um programa. Em Go, erros não são tratados com exceções (`try/catch`), mas sim através do tipo `error`.

O tratamento de erros é importante porque evita falhas inesperadas e torna o sistema mais confiável.

---

## 📌 O tipo error

Em Go, funções podem retornar um valor e um erro ao mesmo tempo:

```go
package main

import (
	"fmt"
	"errors"
)

func dividir(a int, b int) (int, error) {

	if b == 0 {
		return 0, errors.New("não é possível dividir por zero")
	}

	return a / b, nil
}

func main() {

	resultado, erro := dividir(10,0)

	if erro != nil{
		fmt.Println("Erro:", erro)
		return
	}

	fmt.Println(resultado)
}
```

---

## 🔎 Verificando erros

Normalmente o erro é verificado utilizando:

```go
if erro != nil {
    // tratar erro
}
```

Exemplo:

```go
arquivo, erro := os.Open("arquivo.txt")

if erro != nil{
	fmt.Println("Erro ao abrir arquivo")
	return
}
```

---

## ⚠️ Criando erros personalizados

Podemos criar mensagens específicas usando:

```go
errors.New()
```

Exemplo:

```go
package main

import (
	"errors"
	"fmt"
)

func validarIdade(idade int) error {

	if idade < 18 {
		return errors.New("idade mínima não atingida")
	}

	return nil
}

func main(){

	erro := validarIdade(16)

	if erro != nil{
		fmt.Println(erro)
		return
	}

	fmt.Println("Acesso liberado")
}
```

---

## 📋 Boas práticas

✅ Sempre verificar erros retornados  
✅ Criar mensagens claras  
✅ Não ignorar erros importantes  
✅ Usar erros personalizados quando necessário  

---

## 📊 Comparação

| Método | Função |
|----------|----------|
| `error` | Representa um erro |
| `errors.New()` | Cria um novo erro |
| `if erro != nil` | Verifica erro |
| `return nil` | Indica ausência de erro |

---

## 💡 Conclusão

Go utiliza uma abordagem simples e explícita para tratamento de erros. Ao invés de exceções automáticas, o desenvolvedor verifica e trata cada situação manualmente, tornando o código mais previsível e seguro.
