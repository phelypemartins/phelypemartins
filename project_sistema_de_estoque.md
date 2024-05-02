#Definição de variáveis/interação com usuário   

nome_produto = input('Digite o nome do produto: ')
categoria = input('Digite a categoria: ')
quantidade_atual = input('Digite a quantidade atual: ')

#Definição do estoque mínimo

estoque_alimentos = int(50)
estoque_bebidas = int(75)
estoque_limpeza = int(30)

#Nesse bloco, foi desenvolvido um programa para retornar ao usuário, qual a quantidade disponível em estoque. Também acrescentei ao bloco de código, sistema de verificação, onde o usuário deve digitar a categoria correta para ter acesso a quantidade e digitar todas as opções disponíveis para preenchimento

if nome_produto and categoria and quantidade_atual:

    if 'bebidas' in categoria:
        if (f'{quantidade_atual}') < (f'{estoque_bebidas}'):
            estoque = estoque_bebidas - int(quantidade_atual)
            print(f'Solicitar {nome_produto} à equipe de compras, temos apenas {estoque} em estoque')
        else:
            print('Categoria incorreta')

    if 'alimentos' in categoria:
        if (f'{quantidade_atual}') < (f'{estoque_alimentos}'):
            estoque = estoque_alimentos - int(quantidade_atual)
            print(f'Solicitar {nome_produto} à equipe de compras, temos apenas {estoque} em estoque')
        else:
            print('Categoria incorreta')

    if 'limpeza' in categoria:
        if (f'{quantidade_atual}') < (f'{estoque_limpeza}'):
            estoque = estoque_limpeza - int(quantidade_atual)
            print(f'Solicitar {nome_produto} à equipe de compras, temos apenas {estoque} em estoque')
        else:
            print('Categoria incorreta')        
else:
    print('Preencha todas as informações')
