# tic-tac-toe
import random

def printf(a):
    for row in a:
        for elem in row:
            print(elem, end=' ')
        print()


i=0
a=[['-','-','-'],['-','-','-'],['-','-','-']]
printf(a)
while True:
    if i%2==0:
        c,e=input().split()
        c=int(c)
        e=int(e)
        if c>2 and e>2:
            print('Введите правильные координаты')
            continue
        if a[c][e] != '-':
            continue
        
        a[c][e]='x'
    else:
        n=random.randint(0,2)
        m=random.randint(0,2)
        print('Бот выбрал координаты',n,m)
        if a[n][m] != '-':
            continue
        a[n][m]='0'

    printf(a)
    print()
    if a[0][0]==a[0][1]==a[0][2]=='x':
        print('You win')
        break
    if [1][0]==a[1][1]==a[1][2]=='x':
        print('You win')
        break
    if [2][0]==a[2][1]==a[2][2]=='x':
        print('You win')
        break
    
    if a[0][0]==a[1][0]==a[2][0]=='x':
        print('You win')
        break
    if a[0][1]==a[1][1]==a[2][1]=='x':
        print('You win')
        break
    if a[0][2]==a[1][2]==a[2][2]=='x':
        print('You win')
        break

    if a[0][0]==a[1][1]==a[2][2]=='x':
        print('You win')
        break
    if a[0][2]==a[1][1]==a[0][0]=='x':
        print('You win') 
        break   

    
    if a[0][0]==a[0][1]==a[0][2]=='0':
        print('Bot win')
        break
    if [1][0]==a[1][1]==a[1][2]=='0':
        print('Bot win')
        break
    if [2][0]==a[2][1]==a[2][2]=='0':
        print('Bot win')
        break
    
    if a[0][0]==a[1][0]==a[2][0]=='0':
        print('Bot win')
        break
    if a[0][1]==a[1][1]==a[2][1]=='0':
        print('Bot win')
        break
    if a[0][2]==a[1][2]==a[2][2]=='0':
        print('Bot win')
        break

    if a[0][0]==a[1][1]==a[2][2]=='0':
        print('Bot win')
        break
    if a[0][2]==a[1][1]==a[0][0]=='0':
        print('Bot win')    
        break
    
    i+=1
    if i>9:
        print('Ничья')
        break
