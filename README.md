# My projets
This is my projects from beginning in my career as software engeneering
# 🔐 Login Simulation (Python Project)
A simple Python project that simulates a user login system.  
It includes user registration, username verification, password checking with limited attempts, and clear user feedback.

---

##  What I used
- Python code with functions
- Basic logic for user authentication
- Using loops and conditionals
- Creating clean, readable code

------
## Code

username=input("You will register with this username:")

password=input('Set strong password adn remember it :')

attempts = 3

print("======\Entering in the system/======")

new_user=input("Please enter your saved username:")

while new_user != username:
    print(f'{new_user} do not match !')
    new_user = input()
    if new_user == username:
        print('This user was fount ,now type password!')

new_pass = input("Enter your password here:")

while new_pass != password:
        print(f'This password is wrong! You have {attempts} attempts left! ')
        attempts-=1
        if attempts==-1:
            print(f'Please try again later! ')
            break
        new_pass = input('Password:')
        elif new_pass == password:
            print(f'Welcome back {username}!')
            break







----------------
---------------
----------------
------------------
-------------------

#  Mini game(Guess the number)
Easy Python project where the system create random number from range and you need to guess it ,the game dont stop till you type "Stop".
---------
##  What I used
- Python code with functions
- Basic logic for user authentication
- Using loops and conditionals
- Creating clean, readable code
 ----------

## Code

import random
print(f"Hello this is 'Guess the number' if you want to stop playing type 'Stop'")
print('==============')
number=input("Please enter you're guess here: ")
random_numb=random.randint(1,100+1)
while number!='Stop':
   int_num=int(number)
   if int_num==random_numb:
    print(f'Exellent you guessed it right!')
    break

   else:
       if int_num>random_numb:
           print('Too High!')
       if int_num<random_numb:
           print('Too Low!')

   number = input("Please enter you're guess here: ")
   continue
   if number=='Stop':
        print(f'Have a grat day!Come back soon!')

# Qrcodes
import pyqrcode
import png
from pyqrcode import QRCode
address = "https://www.youtube.com/watch?v=r8ETeQX_Zv4&list=RDr8ETeQX_Zv4&start_radio=1"
url=pyqrcode.create(address)
url.png("capitalt.png", scale = 10)

# Login simulation2

import time
print('Hello user, can you enter your nickname and password so we can remember you?')
real_nickname = input('Enter nickname here: ')
real_password = input('Enter strong password here: ')

nick_trys = 4
while nick_trys > 0:
    current_nickname = input('Login nickname: ')
    if current_nickname == real_nickname:
        print(f'{current_nickname} matched with our database.')
        break
    else:
        nick_trys -= 1
        print(f'{current_nickname} not matching!')
        if nick_trys == 0:
            print('Too many attempts. Try again later.')
            exit()
        print(f'Remaining attempts: {nick_trys}')
        
pass_trys = 4
while pass_trys > 0:
    current_pass = input('Now type your password to identify: ')
    if current_pass == real_password:
        print(f'{current_pass} matched with our database. Have fun!')
        break
    else:
        pass_trys -= 1
        print(f'{current_pass} not matching!')
        if pass_trys == 0:
            print('Too many attempts. Try again later.')
            exit()
        print(f'Remaining attempts: {pass_trys}')

#SET TIMER
-----------------------------
#What i use
-Importing from library
-Loops
-Time_sleep option
-printing string from type(int)
#Code
import time


timerDuration = int(input('Time in sec:'))
hours=0
mins=0
sec=0
for i in range(timerDuration):
    print('\n'*100)
    sec+=1
    if sec ==60:
        mins+=1
        sec=0
    if mins==60:
        hours+=1
        mins=0
print(f'{str(hours)}:{str(mins)}:{str(sec)}')
time.sleep(1)
