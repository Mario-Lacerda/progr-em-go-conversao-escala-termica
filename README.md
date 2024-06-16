# Programa em Go para Conversão de Escalas Termometricas


**Programa em Go para Conversão de Escalas Termométricas**

go

```go
package main

import "fmt"

func main() {
    var temperatura float64
    var escalaOrigem string
    var escalaDestino string

    fmt.Println("Digite a temperatura:")
    fmt.Scanln(&temperatura)

    fmt.Println("Digite a escala de origem (C/F):")
    fmt.Scanln(&escalaOrigem)

    fmt.Println("Digite a escala de destino (C/F):")
    fmt.Scanln(&escalaDestino)

    var temperaturaConvertida float64

    switch escalaOrigem {
    case "C":
        if escalaDestino == "F" {
            temperaturaConvertida = (temperatura * 9 / 5) + 32
        } else {
            fmt.Println("Escala de destino inválida.")
            return
        }
    case "F":
        if escalaDestino == "C" {
            temperaturaConvertida = (temperatura - 32) * 5 / 9
        } else {
            fmt.Println("Escala de destino inválida.")
            return
        }
    default:
        fmt.Println("Escala de origem inválida.")
        return
    }

    fmt.Printf("Temperatura convertida: %.2f %s\n", temperaturaConvertida, escalaDestino)
}
```



#### **Explicação:**

- O programa solicita ao usuário que insira a temperatura, a escala de origem e a escala de destino.
- Ele verifica se as escalas de origem e destino são válidas (Celsius ou Fahrenheit).
- Se as escalas forem válidas, o programa converte a temperatura usando as fórmulas apropriadas.
- O resultado é impresso na tela.





Descrição do Desafio:  
Um professor de ensino medio solicitou aos seus alunos que desenvolvessem um programa para converter o valor do ponto de ebulição da água de Kelvin para Graus Celsius.

Dica: C = K - 273



// declarar meu pacote principal
package main

//importar função fmt
import "fmt"

//declaração da variável CONST do ponto de ebulição da água em F
const ebulicaoK = 373.0

//função principal
func main() {

	tempk := ebulicaoK
	tempC := tempk - 273.0
	
	fmt.Printf("A temperatura de Ebulição da água em K = %g , e a Temperatura de Ebulição da água  em °C = %g", tempk, tempC)

}

