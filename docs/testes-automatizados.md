# 🧪 Testes Automatizados em Go

Testes automatizados são utilizados para verificar se partes do sistema funcionam corretamente sem a necessidade de executar tudo manualmente.

Em Go, os testes fazem parte da própria linguagem através do pacote `testing`.

Eles ajudam a identificar erros rapidamente, aumentam a qualidade do código e facilitam futuras alterações.

---

## 📌 Estrutura básica de um teste

Os arquivos de teste em Go utilizam o padrão:

```plaintext
nome_arquivo_test.go
```

Exemplo:

```go
package main

func somar(a int, b int) int {
	return a + b
}
```

Arquivo de teste:

```go
package main

import "testing"

func TestSomar(t *testing.T){

	resultado := somar(2,3)

	if resultado != 5{
		t.Errorf("Esperado 5, mas recebeu %d", resultado)
	}

}
```

---

## ▶️ Executando testes

Para executar todos os testes do projeto:

```bash
go test
```

Para mostrar mais detalhes:

```bash
go test -v
```

---

## 🔎 Entendendo a função de teste

```go
func TestSomar(t *testing.T)
```

- `Test` → obrigatório no início do nome
- `Somar` → nome do teste
- `t *testing.T` → objeto responsável por controlar o teste

---

## 🚀 Exemplo com múltiplos testes

```go
package main

import "testing"

func multiplicar(a int, b int) int{
	return a * b
}

func TestMultiplicar(t *testing.T){

	if multiplicar(2,4) != 8{
		t.Errorf("Erro na multiplicação")
	}

	if multiplicar(3,3) != 9{
		t.Errorf("Erro na multiplicação")
	}

}
```

---

## 📋 Boas práticas

✅ Criar testes pequenos  
✅ Utilizar nomes claros  
✅ Testar diferentes cenários  
✅ Executar testes frequentemente  
✅ Evitar duplicação de código  

---

## 📊 Principais comandos

| Comando | Função |
|----------|----------|
| `go test` | Executa testes |
| `go test -v` | Exibe detalhes |
| `t.Errorf()` | Exibe erro |
| `*_test.go` | Arquivo de teste |

---

## 💡 Conclusão

Os testes automatizados ajudam a garantir a qualidade do software, detectando problemas antes que eles cheguem à produção. Em Go, o suporte nativo da linguagem torna a criação e execução de testes simples e eficiente.
