print("Jogo de adivinhação de número")
print("Vou escolher um número aleatório entre 0 e 100 e você precisa descobrir qual é!!")

import random

while True:
    num = random.randint(0, 100)
    tentativa = 1

    while tentativa <= 10:
        escolha = int(input("Qual o seu palpite de 0 a 100? "))

        if escolha > num:
            print("Chute alto")
        elif escolha < num:
            print("Chute baixo")
        else:
            print(f"Você acertou em {tentativa} tentativas!!")
            break

        tentativa += 1

    if tentativa > 10:
        print(f"Você perdeu! O número era {num}.")

    j = input("Quer jogar de novo? (s/n): ")

    if j != "s":
        break

print("Fim de jogo!")