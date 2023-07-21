# atividade-M3S2-decorator
def decorator_imprimir(funcao):
    def wrapper(capital, taxa, tempo):
        resultado = funcao(capital, taxa, tempo)
        print("Parâmetros:")
        print(f"Capital: {capital}")
        print(f"Taxa: {taxa}")
        print(f"Tempo: {tempo}")
        print(f"Resultado: {resultado}")
        return resultado
    return wrapper

class CalculadoraJuros:
    @staticmethod
    @decorator_imprimir
    def calcular_juros(capital, taxa, tempo):
        juros = capital * taxa * tempo
        return juros

# Utilização da classe CalculadoraJuros
capital = float(input("Digite o valor do capital: "))
taxa = float(input("Digite o valor da taxa: "))
tempo = float(input("Digite o valor do tempo: "))

CalculadoraJuros.calcular_juros(capital, taxa, tempo)
