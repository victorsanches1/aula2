# aula2
temperatura = []
def tempera(lista):
    for i in range(7):
        temperatu = int(input('insira a temperatura atual: '))
        lista.append(temperatu)
def media1(lista):
    soma = int(sum(lista))
    media = int (soma/len(lista))
    return media

def acima_media(lista):
    tempera_acimaMedia = 0
    soma = int(sum(lista))
    media = int(soma/len(lista))
    for i in lista:
        tempera_acimaMedia += 1
        return tempera_acimaMedia
    
tempera(temperatura)
print(f'temperatura: segunda({temperatura[0]}), terça({temperatura[1]}), quarta({temperatura[2]}), quinta ({temperatura[3]}), sexta ({temperatura[4]}, sabado ({temperatura[5]}), domingo ({temperatura[6]}))')
media = media1(temperatura)
print(f'A media das temperaturas é: {media}')

maior = max(temperatura)
menor = min(temperatura)

print(f'a temperatura maior é {maior}, e a temperatura menor é {menor}')
acimamedia = acima_media(temperatura)
print(f'as temperaturas acima da media são {acimamedia}')



# 2 
compras = []
def adicionar_itens(lista):
    item = input('Insira seu Produto: ')
    while item != 'Sair':
        item = input('insira seu item: ')
        lista.appen(item)
        return lista
lista_compras = adicionar_itens(compras)
compras.sort()
compras.remove('sair')
print(f'Seus itens em ordem: {compras}')

# 3 
par = []
impar = []
def par_impar(par, impar):
    for numeros in range(10):
        numeros = int(input('insira seu numero:'))
        if numeros % 2 == 0:
            par.append(numeros)
        else:
            impar.append(numeros)
    return par,impar

par_impar(par, impar)
print (f'os numeros pares são: {par}, os numeros impares são: {impar}. ')

#4

produtos_venda = []

def guarda_valor (produtos_venda):
    while True:
        produto = input('''
Tabela de preços: 
Televisão = 1200 (1)
Celular = 800 (2)
Notebook = 2500 (3)
Smartwatch = 500 (4)
                        
Escolha o produto pelo numero:  
(Se nao quiser compra digite: sair)''')
        if produto == '1':
         produtos_venda.append ( {'nome':'Televisão','preço':1200})
         break
        elif produto == '2':
             produtos_venda.append ( {'nome':'Celular','preço':800})
        elif produto == '3':
            produtos_venda.append ( {'nome':'Notebook','preço':2500})
        elif produto == '4':
            produtos_venda.append ( {'nome':'Smartwatch','preço':500})
        return produtos_venda
def valor_total(lista_vendas):
    total = 0 
    for venda in lista_vendas:
        total += venda['preço']
    return total
def maior_menor(produto_vendas):
    maior = max(produto_vendas, key=lambda item: item ['preço'])
    menor = min(produto_vendas, key=lambda item: item ['preço'])
    return maior, menor
def procurar_produtos(produtos_venda):
    produto = input('Insira o nome do produto que deseja saber se foi vendido:')
    for produtos in produtos_venda:
        if produtos ['Nome']== produto:
            print(f'O produto foi vendido{produto}')
    else:
        print(f'o produto {produto} não foi vendido:')

guarda_valor(produtos_venda)
print(produtos_venda)
total = valor_total(produtos_venda)
print(f'O valor é :{total}')
maior, menor = maior_menor(produtos_venda)
print(f'O valor maior é {maior}, e o menor é: {menor}')
procurar_produtos(produtos_venda)
