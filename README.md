# Guessing-Game-From-3-to-20-Python
import random

def guess(x):
  point=10
  random_n=random.randint(1,x)
  guess_n=0
  while(guess_n!=random_n):
    guess_n=int(input(f'Guess the number which is between 1 and {x}: '))
    print("")
    if (guess_n<random_n):
      point-=1
      print("Your number is lower than, the number you are guessing.")
    elif guess_n>random_n:
      point-=1
      print("Your number is higher than, the number you are guessing.")
  if point==10:
    print("Bravo! Obviously you are correct but,\n the bigger picture here is that\n you have scored a maximum of 10 points")
  else:
    print(f'Congratulations! You have guessed the correct number\n but, you only scored: {point} points from a possible of 10.')
random_num=random.randint(3,20)
guess(random_num)
