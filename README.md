# Guessing-Game-From-3-to-20-Python
import random

def guess(x):
  random_n=random.randint(1,x)
  guess_n=0
  while(guess_n!=random_n):
    guess_n=int(input(f'Guess the number which is between 1 and {x}: '))
    print("")
    if (guess_n<random_n):
      print("Your number is lower than, the number you are guessing.")
    elif guess_n>random_n:
      print("Your number is higher than, the number you are guessing.")

  print("Congratulations! You have guessed the correct number.")
random_num=random.randint(3,20)
guess(random_num)
