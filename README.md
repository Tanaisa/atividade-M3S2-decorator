# atividade-M3S2-decorator
def decorator_imprimir(funcao):
    def mostrar_na_tela(*args, **kwargs):
     capital, taxa, tempo = args
        resultado = funcao(*args, **kwargs):
        return print(f"Capital: {capital}")
        (Taxa:{taxa},(Tempo: {tempo}"),
    (f"Resultado: {resultado}")
      return mostrar_na_tela


    @decorator_imprimir
    def juros_simples(capital, taxa, tempo):
        return capital * (taxa/100) * tempo
       capital = 1000.0
       taxa= 6.0
       tempo = 10.0

juros_simples(capital , taxa, tempo)
