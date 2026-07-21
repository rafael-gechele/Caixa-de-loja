# ==========================================
# Simulador de Caixa de Loja
# Autor: Rafael Gechele
# Descrição:
# Programa que calcula o valor de uma compra,
# aplica desconto de 10% para compras acima
# de R$100 e classifica o tamanho da compra.
# ==========================================

print("=" * 35)
print("      🛒 CAIXA DA LOJA 🛒")
print("=" * 35)

# Entrada de dados
produto = input("\nNome do produto: ")
preco = float(input("Preço do produto (R$): "))
quantidade = int(input("Quantidade: "))

# Cálculo do valor total
valor_total = preco * quantidade

print("\n" + "=" * 35)

# Aplicação de desconto
if valor_total >= 100:
    desconto = valor_total * 0.10
    valor_final = valor_total - desconto

    print("🎉 DESCONTO APLICADO (10%) 🎉\n")
    print(f"Produto........: {produto}")
    print(f"Quantidade.....: {quantidade}")
    print(f"Valor original.: R$ {valor_total:.2f}")
    print(f"Desconto.......: R$ {desconto:.2f}")
    print(f"Valor final....: R$ {valor_final:.2f}")

else:
    valor_final = valor_total

    print("🛍️ RESUMO DA COMPRA 🛍️\n")
    print(f"Produto........: {produto}")
    print(f"Quantidade.....: {quantidade}")
    print(f"Valor total....: R$ {valor_total:.2f}")

# Classificação da compra
print("\nClassificação da compra:")

if valor_total < 100:
    print("🟢 Compra pequena")
elif valor_total < 300:
    print("🟡 Compra média")
else:
    print("🔴 Compra grande")

print("\n" + "=" * 35)
print("🛒 Obrigado pela compra!")
print("=" * 35)
