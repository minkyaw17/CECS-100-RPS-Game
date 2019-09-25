import random

def menu(): # the menu display
  print('Menu:')
  print('1. Play Game')
  print('2. Show Score')
  print('3. Quit')

def weaponmenu(): # the weaponmenu display
  print('Weapons')
  print('R. Rock')
  print('P. Paper')
  print('S. Scissors')
  print('L. Lizard')
  print('SP. Spock')

def compthrow(): # generating a computer throw
  ct = random.randint(1,5)
  if ct == 1:
    print('Computer Chose Rock')
  elif ct == 2:
    print('Computer Chose Paper')
  elif ct == 3:
    print('Computer Chose Scissors')
  elif ct == 4:
    print('Computer Chose Lizard')
  elif ct == 5:
    print('Computer Chose Spock')
  return ct

def checkmenu(low,high): # error checking for menu input
  choice = 0
  invalid = True
  while invalid:
    try:
      choice = int(input('Enter a # on the menu: '))
      if choice >= low and choice <= high:
        invalid = False
      else:
        print('Invalid Range')
    except ValueError:
        print('Invalid Entry')
    return choice

def user_choice(): # getting user input with validation
  while True:
    wpchoice = input('Choose your weapon: ')
    if wpchoice == 'R' or wpchoice == 'r':
      print('You Chose Rock')
      return 1
    elif wpchoice == 'P' or wpchoice == 'p':
      print('You Chose Paper')
      return 2
    elif wpchoice == 'S' or wpchoice == 's':
      print('You Chose Scissors')
      return 3
    elif wpchoice == 'L' or wpchoice == 'l':
      print('You Chose Lizard')
      return 4
    elif wpchoice == 'SP' or wpchoice == 'sp':
      print('You Chose Spock')
      return 5
    else:
      print('Invalid Input')

def winner(wpchoice, ct): # determining winner
  if wpchoice == ct:
    print('Tie!')
  elif (wpchoice == 1 and ct == 3) or (wpchoice == 2 and ct == 1) or (wpchoice == 3 and ct == 2) or (wpchoice == 1 and ct == 4) or (wpchoice == 5 and ct == 3) or (wpchoice == 4 and ct == 5) or (wpchoice == 2 and ct == 5) or (wpchoice == 4 and ct == 2) or (wpchoice == 3 and ct == 4) or (wpchoice == 5 and ct == 1):
    print('You Win!')
    return 1
  else:
    print('Computer Wins!')
    return 2

def main(): # main program
  myscore = 0
  cpuscore = 0
  
  while True:
    menu()
    choice = checkmenu(1,3)
    if choice == 1:
      weaponmenu()
      mychoice = user_choice()
      cpuchoice = compthrow()
      w = winner(mychoice, cpuchoice)
      if w == 1: # counting user score
        myscore +=1
      if w == 2: #counting computer score
        cpuscore +=1
    elif choice == 2:
      print('Player =', myscore)
      print('Computer =', cpuscore)
    elif choice == 3:
      print('Final Score:')
      print('Player =', myscore)
      print('Computer =', cpuscore)
      break
main()
