from datetime import datetime, timedelta

# Corrected operations list
operations = ['1. Seconds to minutes', '2. Seconds to hours', '3. Minutes to seconds', '4. Minutes to hours', '5. Hours to seconds', 
              '6. Hours to minutes', '7. Differences between numbers', '8. Seconds from now', '9. Minutes from now', '10. Hours from now']

calculations = [lambda x: x / 60, lambda x: x / 3600, lambda x: x * 60, lambda x: x / 60, lambda x: x * 3600, 
                lambda x: x * 60, lambda x, y: x - y, lambda x: datetime.now().replace(microsecond=0) + timedelta(seconds=x), 
                lambda x: datetime.now().replace(microsecond=0) + timedelta(minutes=x), lambda x: datetime.now().replace(microsecond=0) + timedelta(hours=x)]

# Printing the operations
for o in operations:
    print(o)

# Getting a valid operation input from the user
while True:
    try:
        user_input = input('Enter your operator number: ')
        if user_input.isdigit() and 1 <= int(user_input) <= 10:
            user_input = int(user_input)
            break
        else:
            print('Invalid input. Please enter a number between 1 and 10.')
    except ValueError:
        print('Invalid input. Please enter a number between 1 and 10.')

# Getting the required numbers from the user
while True:
    try:
        num = int(input('Enter your number: '))
        if  user_input == 7:
            num2 = int(input('Enter the second number: '))
            result = calculations[user_input - 1](num, num2)
        else:
            result = calculations[user_input - 1](num)
        break
    except ValueError:
        print('Not an integer. Try again.')

f = [w.split() for w in operations]
time_format = f[user_input-1][3]

if user_input == 7:
    print(f'The difference is: {result}')
elif user_input in [8, 9, 10]:
    print(f'Your result is: {result} from {time_format}')
else:
    print(f'Your result is : {result} {time_format}')
