---

### **2. main.py**  
```python
from utils.calculadora import Calculadora

def main():
    print("Calculadora Simples")
    calc = Calculadora()

    while True:
        print("\nEscolha a operação:")
        print("1 - Adição")
        print("2 - Subtração")
        print("3 - Multiplicação")
        print("4 - Divisão")
        print("0 - Sair")

        escolha = input("Opção: ")

        if escolha == '0':
            print("Encerrando...")
            break

        try:
            a = float(input("Digite o primeiro número: "))
            b = float(input("Digite o segundo número: "))

            if escolha == '1':
                print("Resultado:", calc.adicionar(a, b))
            elif escolha == '2':
                print("Resultado:", calc.subtrair(a, b))
            elif escolha == '3':
                print("Resultado:", calc.multiplicar(a, b))
            elif escolha == '4':
                print("Resultado:", calc.dividir(a, b))
            else:
                print("Opção inválida!")
        except ValueError:
            print("Entrada inválida. Tente novamente.")

if __name__ == "__main__":
    main()
