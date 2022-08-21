# Estudos-de-Python
##Arquivo de estudos com meus promeiros codigos, e coisas que aprendi, e testes de conhecimento## 
## matemática##
n1 = int(input('digite um valor:'))
n2 = int(input('digite mais um valor:'))
soma = n1 + n2 
print ('a soma ente {} e {} é {}'.format(n1,n2,soma)) 
dv = n1 / n2
print ('a divisão de {} por {} é {} '.format(n1,n2,dv))
multiplicacao = n1*n2
print ('a multiplicação de {} por {} é igual a {}'.format(n1,n2,multiplicacao))
subtracao = n1-n2 
print ('{} menos {} é igual {}'.format(n1,n2,subtracao))
potencia = n1**n2
print ('{} elevado a {} é igual a {}'.format(n1,n2,potencia))
divinteira = n1//n2
print ('a divisão inteira entre {} e {} é igual a {}'.format(n1,n2,divinteira))
rd = n1%n2
print(' o resto da divisão entre {} e {} é {}'.format(n1,n2,rd))
##
##
##Exercicios##
##1) metro pra cm e pra mm##
print (' Então vc quer converter metros em centimetros e milimitros')
metros = int(input ('digite o valor em metros:'))
cent = metros * 100
milim = cent * 10 
print ('{}M são {} cm, e consequentemente são {} mm'.format(metros,cent,milim))
##
##
##raiz quadrada##
valor = int(input('digite um valor:'))
dobro = valor * 2 
print ('O dobro de {} é {}'.format(valor,dobro))
triplo = valor * 3
print ('O triplo de {} é {}'.format(valor,triplo))
raq = valor**(1/2)
print ('A raiz quadrada de {} é {}'.format(valor,raq))
raicub = valor **(1/3)
print ('A raiz cúbica de {} é {}'.format(valor,raicub))
##
##
##progrma pintura/ cada litro pinta 2m quadrados##
print ('Então você quer pintar uma parede')
alturaparede = float(input('qual aaltura dela?'))
compri = float(input('e o comprimento dela?'))
metqua = alturaparede * compri
tinta = metqua / 2
print ('Sabendo que a cada litro de tinta pinta 2m quadrados,\n para sua parede de {} metros quadrados vc vai usar {} litros de tinta'.format(metqua,tinta))
preco = float(input('qual o valor de cada litro de tinta?'))
total = tinta * preco
print ('Você irá gastar R${} em tinta fora a mão de obra!'.format(total))
####
##media de escola##
nota1= int(input('qual a sua primeira nota? :'))
nota2= int(input('qual sua segunda nota? :'))
nota3= int(input('qual sua terceira nota? :'))
smnots =nota1 + nota2 + nota3
print('SUA MEDIA É {:.2f}'.format(smnots /3))
####
#### ===== {:.2f} ==== este comando entro dos {} estipiula numero de casas decimais que será exibido após o '.'
####
##outra opção de fazer seria:
# média = smnots / 3  
#print('a media das suas notas é {}'.format(média))
##
##
##### Tabuada ####
numero= int(input("Digite um número para ver sua tabuada:"))
print('=' *12)
print('{} x {:2} = {} '.format(numero,1, numero*1))
print('{} x {:2} = {} '.format(numero,2, numero*2))
print('{} x {:2} = {} '.format(numero,3, numero*3))
print('{} x {:2} = {} '.format(numero,4, numero*4))
print('{} x {:2} = {} '.format(numero,5, numero*5))
print('{} x {:2} = {} '.format(numero,6, numero*6))
print('{} x {:2} = {} '.format(numero,7, numero*7))
print('{} x {:2} = {} '.format(numero,8, numero*8))
print('{} x {:2} = {} '.format(numero,9, numero*9))
print('{} x {:2} = {} '.format(numero,10, numero*10))
print('=' *12)
## podemos usar o simbolo "*" de multiplicação pra replicar strings, este caso: prit("=" *12) vai ser escrito 12x = ; "===========' desta forma '
## o comando {:2} indica que será ocupado o espaço de 2 digitos deixando mais alinhado
# 

### Desconto ###
preço= float(input('estamos com uma oferta de 5% desconto!\n digite o valor do produto que vc deseja:'))
valor100 = preço / 100
dcnt = valor100 * 5
print('Com o desconto o preço do seu produto fica R${:.2f}'.format(preço - dcnt))
#####
#####
 #Exercício Python 15: Escreva um programa que pergunte a quantidade de Km percorridos por um carro alugado e a quantidade de dias pelos quais ele foi alugado. Calcule o preço a pagar, sabendo que o carro custa R$60 por dia e R$0,15 por Km rodado.

diarias= int(input("pro quantos dias você alugou o carro?:"))
kms= float(input("quantos Kms você rodou com o carro?:"))
diariasrs = diarias * 60
kmsrs= kms * 0.15
#### ou poderia  ter feito:
#pagar= (diarias * 60) + (kms * 0.15)
#print("o total a pagar é R${:.2f}".format(pagar))
totalrs = diariasrs + kmsrs
print('o total de diarias ficou R${:.2F}\n o total de quilemtragem ficou R${:.2F}\n TOTAL A PAGAR R${:.2f}'.format(diariasrs, kmsrs, totalrs))
##
####
#### Jogo de adivinhar um numero#####
####                           ######

from ast import While
import random
def gera ():  
    return random.randint (1,10)
def game():
    resposta = gera()
    tentativa = 0
    print("\nPalpite gerado!")
    chute = 0
    while chute is not resposta:
        tentativa +=1
        chute = int(input('Qual seu chute:'))
        if chute > resposta:
            print ('Errou! É u valor menor que', chute)
        elif chute < resposta:
            print ("Errou! É um valor maior que ",chute)
        else:
            print("parabéns! O número gerado foi", resposta, "acertou em", tentativa, "tentativas")
while True:
 #   game()
    
## para funcionar o jog odeve-se apagar o sinal "#" na frente da linha 126 game()

#  
#### CONDICIONAIS IF,ELSE ####
##if condição: E SE? / o que fazer caso a condição seja verdadeira
##else: caso contrario / o que fazer cao a condição seja falsa

#  crie um programa para um fundo de investimentos, que analize o quato de taxa deve ser paga:
#retorno  minimo de 5% ao ano
#caso não atinja 5% de rentabilidade ele não cobra taxas dos investidores
#caso atinja 5% é cobrado 2% de taxa dso investidores
# caso cosiga entregar mais de 20% de retorno será cobrado 4% dos investidores
 ######################################################################################################

meta = 0.05
taxa = 0
rendimento = float(input('Digite a porcentagem do rendimento obtido:'))
rend = rendimento / 100

if rend> meta:
    if rend > 0.20:
        taxa = 0.04
        print("A taxa aplicada será: {}%".format(taxa *100))
    
    else:
     taxa = 0.02
     print("A taxa aplicada será: {}%".format(taxa*100))
    
else:
    taxa = 0
    print ('A taxa aplicada será: {}%'.format(taxa*100))    

#########################################################################
### programa que calcula meta de vendedor###
### se atingir meta ganha o dobro de comissão###
### se vender equivalente ao dobro da meta ou ganha bonus de 10% ####

venda = float(input('valor vendido no mês:'))
metav = float(input("Valor da meta:"))
comis = venda*0.015
comismet = comis*2
bonus = comismet * 0.1
comibon = comismet + bonus


if venda >= metav:
          
    if venda >= metav*2:
          print ("parabéns você estrassalhou a meta!! vendeu 2x mais que o esperado, então sua comissão será {} ".format(comibon))
    else:
         print(" Sua comissão será de {}".format(comis*2))       

else:
    print ("Sua comissão será {}".format(comis))
    print (" Esperamos qeu na proxia você atinja a meta!")
