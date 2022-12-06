import os
import  math 

def simple_sum(x,char,y):
    match char:
        case '+':
            return(x+y)
        case '-':
            return(x-y)
        case '*':
            return(x*y)
        case '%':
            return(x%y)
        case '**':
            return(x**y)
        case '/':
            return(x/y)
# for sicentific calculater 
def sicentific_calculater(choice,x):
    match choice:
        case 1:
            return math.sin(x)
        case 2:
            return math.cos(x)
        case 3:
            return math.tan(x)
        case 4:
            return math.asin(x)
        case 5:
            return math.acos(x)
        case 6:
            return math.atan(x)




def inputs_user(choice):
    if choice=='1':
        os.system('cls')
        print('''
                --Welcome To Simple Calculater--
    ''')
        x = int(input('Enter The first number: '))
        char = input('Enter the opration: ')
        y = int(input('enter the second number: '))
        print(simple_sum(x,char,y))
    elif choice=='3':
        exit()
    else:
         os.system('cls')
         print('''
                --Welcome To Scietific Calculater--
                [1] for sin
                [2] for cos
                [3] for tan
                [4] for sec
                [5] for cosec
                [6] for cot


    ''')
         choice_user = int(input('Enter Your Choice: '))

         x = int(input('Enter The value: '))
         print(sicentific_calculater(choice_user,x))

def main():
    os.system('cls')
    print('''
                --Welcome To Scietific Calculater--
            Enter the choice:
            [1] : simple calculater
            [2] :scientific calculater
            [3] :exit



    ''')

    inputs_user(input('Enter the choice: '))

while True:
    main()
    input('Press Enter To Proseed....')
