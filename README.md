# Gestational-age-and-pregnancy-risk-calculator
This is a basic calculator to compute pregnancy weeks, and risk of a pregnancy based on the age of the mother.
I used python, as I'm currently learning the basics of programming. Here is the code. It works as of June 3rd 2020.
I'd like to know how to keep the today date updated. 


user_name = input('Hi, welcome to our hospital. Im a bot that calculates your babys age. Please, tell me your name: ')
user_baby = input(f'Hi {user_name} Have you decided your babys name? Write it, please: ')
age_user = int(input('Whats your age?: '))
pregnancy_risk = 0
if age_user <= 18 or age_user >=40:
    pregnancy_risk = ('high risk')
else:
    pregnancy_risk = ('low risk')
lmp_day = int(input('When was the day of LMP? (dd): '))
lmp_month = int(input('When was the month of LMP (mm): '))
lmp_year= int(input('When was the year of LMP (yy): '))
baby_days = 0
if lmp_year == 19:
    baby_days = ((365 - (lmp_day + ((lmp_month - 1)*30)))+ 156)
elif lmp_year == 20:
    baby_days = (156 - (lmp_day + ((lmp_month - 1)*30)))    
else:
    print('Your baby cant be that old.')
baby_weeks = baby_days//7 + (baby_days%7 * 0.1)

print (f'Ok {user_name}. Your baby {user_baby}, is {baby_days} days old, which is {baby_weeks} weeks old. You have a {pregnancy_risk} pregnancy.') 
