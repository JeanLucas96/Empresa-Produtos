import os

class Produtos:
    #O _init_ deve ter dois underlines(_), colocar em todo o resto do código assim
    def _init_(self, nome, valor, quantidade):
        self.nomeproduto = nome
        self.valorproduto = valor
        self.quantidadeproduto = quantidade


class SistemaCadastroProduto:

    def _init_(self):
        self.arquivo = r"c:\Users\User\Desktop\Empresa+ Produtos"

    def cadastrarproduto(self):

        print("\n===== CADASTRAR PRODUTO =====\n")

        while True:

            while True:

                nomeproduto = input("Digite o nome do produto: ").strip()

                if nomeproduto == "":
                    print("\nNome inválido\n")
                else:
                    break

            while True:

                try:

                    valorproduto = float(input("\nDigite a valor do produto: "))

                    if valorproduto < 0:
                        print("\nValor invalido")
                    else:
                        break
                except ValueError:
                    print("\nDigite apenas números")

            while True:

                try:

                    quantidadeproduto = int(input("\nDigite a quantidade de produtos: "))

                    if quantidadeproduto < 0:
                        print("\nQuantidade invalida")
                    else:
                        break
                except ValueError:
                    print("\nDigite apenas numeros")
                
            
            produto = Produtos(nomeproduto, valorproduto, quantidadeproduto)

            with open(self.arquivo, "a", encoding="utf-8") as arquivo:

                arquivo.write(
                    f"Produto: {produto.nomeproduto} |"
                    f"Valor: {produto.valorproduto}R$ |"
                    f"Estoque: {produto.quantidadeproduto} |\n"
                    )

            print("\nProduto cadastrado com sucesso!\n")

            break

SCP = SistemaCadastroProduto()

SCP.cadastrarproduto()

#Troque o salvar no arquivo por este caminho:
  class SistemaCadastroProduto:

    def _init_(self):
        self.arquivo = r"c:\Users\User\Desktop\Empresa+ Produtos\produtos.txt"

#Também adicione um tratamento de erro no nome, pois estão estrando números.

#Adicione a função listar também.

#Adicionar colorama também

#Ou seja, adicionar tratamento de erro no nome usando str, adicionar a função listar e adicionar o colorama.
