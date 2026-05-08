1.Hello World
programa {
  funcao inicio() {
    escreva("Hello, World!")
  }
}

2.Soma
programa {
  funcao inicio() {
    real n1, n2, total
    escreva("Digite um número: ", "\n")
    leia(n1)
    escreva("Digite outro número: ", "\n")
    leia(n2)

    total = n1 + n2

    escreva("A soma dos dois números é: ", total, "\n")

  }
}

3.Par ou ímpar
programa {
  funcao inicio() {
    inteiro numero

		escreva("Digite um número: ")
		leia(numero)

		se (numero % 2 == 0)
		{
			escreva("O número ", numero, " é par.")
		}
		senao
		{
			escreva("O número ", numero, " é ímpar.")
		}
  }
}


4.Maior número
programa {
	funcao inicio() {
		real n1, n2
		escreva("Digite o primeiro número: ")
		leia(n1)
		escreva("Digite o segundo número: ")
		leia(n2)
		se (n1 > n2) {
			escreva("O maior número é: ", n1)
		} senao {
			escreva("O maior número é: ", n2)
		}
	}
}

5.Média
programa {
	funcao inicio() {
		real n1, n2, n3, media
		escreva("Digite três números:\n")
		leia(n1, n2, n3)
		media = (n1 + n2 + n3) / 3
		escreva("A média aritmética é: ", media)
	}
}


6.Área do círculo
programa {
	funcao inicio() {
		real raio, area
		const real PI = 3.14
		escreva("Informe o raio do círculo: ")
		leia(raio)
		area = PI * (raio * raio)
		escreva("A área do círculo é: ", area)
	}
}

7.Conversão
programa {
	funcao inicio() {
		real c, f
		escreva("Digite a temperatura em Celsius: ")
		leia(c)
		f = (c * 9/5) + 32
		escreva("A temperatura em Fahrenheit é: ", f)
	}
}


8.Tabuada
programa {
	funcao inicio() {
		inteiro num, i
		escreva("Digite um número para ver a tabuada: ")
		leia(num)
		para (i = 1; i <= 10; i++) {
			escreva(num, " x ", i, " = ", num * i, "\n")
		}
	}
}


9.Fatorial
programa {
	funcao inicio() {
		inteiro num, i, fat = 1
		escreva("Digite um número inteiro positivo: ")
		leia(num)
		para (i = 1; i <= num; i++) {
			fat = fat * i
		}
		escreva("O fatorial de ", num, " é: ", fat)
	}
}


10.Contagem regressiva
programa {
	funcao inicio() {
		inteiro i
		para (i = 10; i >= 1; i--) {
			escreva(i, "\n")
		}
		escreva("BOOOOOM!!")
	}
}


11.Número primo
programa {
  funcao inicio() {
    inteiro num, i, divisores = 0
    escreva("Digite um número: ", "\n")
    leia(num)
    para (i = 1; i <= num; i++) {
      se (num % i == 0) { divisores++ }
    }
    se (divisores == 2) {escreva("O número é primo")}
    senao {escreva("O número não é primo")}
    
  }
}


12.Soma dos naturais
programa {
	funcao inicio() {
		inteiro n, i, soma = 0
		escreva("Somar até qual número? ")
		leia(n)
		para (i = 1; i <= n; i++) { soma += i }
		escreva("A soma é: ", soma)
	}
}


13.Fiboccini
programa {
	funcao inicio() {
		inteiro n, i, a = 0, b = 1, proximo
		escreva("Quantos termos? ")
		leia(n)
		para (i = 1; i <= n; i++) {
			escreva(a, " ")
			proximo = a + b
			a = b
			b = proximo
		}
	}
}


14.Inversão de números
programa {
	funcao inicio() {
		inteiro num, invertido = 0, resto
		escreva("Digite um número: ")
		leia(num)
		enquanto (num > 0) {
			resto = num % 10
			invertido = (invertido * 10) + resto
			num = num / 10
		}
		escreva("Invertido: ", invertido)
	}
}


15.Potência
programa
{
	funcao inicio()
	{
		inteiro base, expoente, i, resultado = 1
		escreva("Digite a base: ")
		leia(base)
		escreva("Digite o expoente: ")
		leia(expoente)
		se (expoente < 0) {
			escreva("Esse código só aguenta expoentes positivos.")
		} senao {
			para (i = 1; i <= expoente; i++)
			{
				resultado = resultado * base
			}
			escreva("Resultado: ", resultado)
		}
	}
}


16.MDC
programa {
	funcao inicio() {
		inteiro a, b, resto
		escreva("Digite um número: ")
		leia(a)
    escreva("Digite outro número: ")
    leia(b)
		enquanto (b != 0) {
			resto = a % b
			a = b
			b = resto
		}
		escreva("MDC: ", a)
	}
}


17.MMC
programa {
	funcao inicio() {
		inteiro a, b, num1, num2, resto, mdc, mmc
		escreva("Digite um número: ")
		leia(a)
    escreva("Digite outro número: ")
    leia(b)
		num1 = a
		num2 = b
		enquanto (num2 != 0) {
			resto = num1 % num2
			num1 = num2
			num2 = resto
		}
		mdc = num1
		mmc = (a * b) / mdc
		escreva("MMC: ", mmc)
	}
}


18.Números perfeitos
programa {
	funcao inicio() {
		inteiro num, i, soma = 0
		escreva("Digite um número: ")
		leia(num)
		para (i = 1; i < num; i++) {
			se (num % i == 0) { soma += i }
		}
		se (soma == num) { escreva("É um número perfeito.") }
		senao { escreva("Não é um número perfeito.") }
	}
}


19.Adivinha
programa {
	inclua biblioteca Util --> u
	funcao inicio() {
		inteiro secreto = u.sorteia(1, 100), palpite = 0
		enquanto (palpite != secreto) {
			escreva("Adivinhe o número (1-100): ")
			leia(palpite)
			se (palpite < secreto) { escreva("Mais alto!\n") }
			senao se (palpite > secreto) { escreva("Mais baixo!\n") }
		}
		escreva("ACERTOU AMIGO, ACERTOU!")
	}
}


20.TUDO
programa 
{
	funcao inicio()
	{
		inteiro n, i, divisores = 0, soma = 0, inv = 0, resto, temp, fat = 1, a = 0, b = 1, proximo

		escreva("Digite um número inteiro positivo: ")
		leia(n)

		se (n < 0) {
			escreva("Por favor, digite um número positivo.")
		} senao {
			
			// 1. Olhar se é primo
			para (i = 1; i <= n; i++) {
				se (n % i == 0) {
					divisores++
				}
			}

			// 2. Soma dos naturais até N
			para (i = 1; i <= n; i++) {
				soma = soma + i
			}

			// 3. Inverter número
			temp = n
			enquanto (temp > 0) {
				resto = temp % 10
				inv = (inv * 10) + resto
				temp = temp / 10
			}

			// 4. Calcular fatorial
			para (i = 1; i <= n; i++) {
				fat = fat * i
			}

			// Resultados
			escreva("\n--- Resultados para o número ", n, " ---")
			
			escreva("\n1. Primo: ")
			se (divisores == 2) { escreva("Sim") } senao { escreva("Não") }

			escreva("\n2. Soma de 1 até ", n, ": ", soma)

			escreva("\n3. Inversão dos dígitos: ", inv)

			escreva("\n4. Fatorial: ", fat)

			escreva("\n5. Sequência de Fibonacci (", n, " termos): ")
			a = 0 
			b = 1
			para (i = 1; i <= n; i++) {
				escreva(a, " ")
				proximo = a + b
				a = b
				b = proximo
			}
		}
	}
}
































































