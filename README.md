while True:
    print("---- MENU ----")
    print("1 - Cadastrar")
    print("2 - Listar")
    print("3 - Sair")

    opcao = input("Escolha uma opção: ")

    if opcao == "1":
        nome = input("Nome: ")
        idade = int(input("Idade: "))
        with open("cadastros.txt", "a") as arquivo:
            arquivo.write(f"{nome} - {idade} anos\n")
        print(f"{nome} cadastrado com sucesso!")

    if opcao == "2":
        print("---- CADASTROS ----")
        with open("cadastros.txt", "r") as arquivo:
            print(arquivo.read())

    if opcao == "3":
        print("Saindo...")
