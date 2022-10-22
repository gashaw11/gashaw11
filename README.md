import random, sys
wins = 0
losses = 0
ties = 0

while True:
    print(f"{wins} wins, {losses} losses, {ties} ties") 
    while True:
        print("enter r, p, s, or q")
        user = input()
        
        if user == 'q':
            sys.exit()
        elif user == 'r' or user == 'p' or user == 's':
            break
    randomNum = random.randint(1, 3)
    if randomNum == 1:
        computer = 'r'
    elif randomNum == 2:
        computer = 'p'
    elif randomNum == 3:
        computer = 's'
    if user == computer:
        ties = ties + 1 
    elif user == 'r' and computer == 'p':
        losses = losses + 1 
    elif user == 'p' and computer == 's':
        losses = losses + 1 
    elif user == 's' and computer == 'r':
        losses = losses + 1 
    elif computer == 'r' and user == 'p':
        wins = wins + 1 
    elif computer == 'p' and user == 's':
        wins = wins + 1 
    elif computer == 's' and user == 'r':
        wins = wins + 1 
            
