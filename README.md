# StrongPassword
# Strong password detection code
# This is python code for the detection of strong password during login into any application.
import re
capsReg=re.compile(r'[A-Z]')
lowerReg=re.compile(r'[a-z]')
digitReg=re.compile(r'\d')
specialReg=re.compile(r'[!@#$%^&*()]')
while True:
    print('Enter your password')
    x=input()
    if (len(x.strip()))<8:
       print ('Password should be at least 8 characters')
       continue
    elif not capsReg.search(x):
        print('password needs contain one uppercase letter')
        continue
    elif not lowerReg.search(x):
        print('password needs contain one lowercase letter')
        continue
    elif not digitReg.search(x):
        print('password needs contain one digit letter')
        continue
    elif not specialReg.search(x):
        print('password needs contain one special letter')
        continue
    else:
        print ('Valid Password')
        break
