# DIO_Desafio_01
Desafio do Projeto 01.  Criando um Sistema Bancário com Python

menu = """

[d] Despositar
[s] Eacar
[e] Extrato
[q] Sair

=> """

saldo = 0
Limite = 500
Extrato = ""
Numero_saques = 0
LIMITE_SAQUES = 3

while True:

	opcao = input(menu)

	if opcao =="d":
		valor = float(input("Informe o valor do depósito: "))

		if valor > 0:
			saldo += valor
			extrato += f"Depósito: R$ {valor:.2f}\n"
			extrato += f"Depósito: R$ {valor:.2f}\n"

		else:
			print("Operação falhou! O valor informado é inválido.")

	elif opcao =="s":
		valor = float(input("Informe o valor do saque: "))

		excedeu_saque = valor > saque

		excedeu_limite = valor > limite

		excedeu_saques = numero_saques >= LIMITE_SAQUES

		if excedeu_saldo:
			print("Operação falhou! Você não tem saldo suficiente.")

		elif excedeu_limite:
			print("Operação falhou! O valor do saque excede o limite.")

		elif excedeu_saques:
			print("Operação falhou! Número máximo de saques excedidos.")

		elif valor > 0:
			saldo -= valor
			extrato += f"Saque: R$ {valor:.2f}\n"

		else:
			print("Operação falhou! O valor informado é inválido.")

	
	elif opção == "e":
		print("\n============= EXTRATO =============")
		print("Não foram realizadas movimentações." if not extrato else extrato)
		print("f\nSaldo: R$ {saldo:.2f}")
		print("=======================================") 

	elif opcao == "q":
		break

	else:
		print("Operação inválida, por favor selecione novamente a operação desejada.")

