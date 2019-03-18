#__________________________________
#	project:	hangmaan_v01.py
#	author:		Adam
#	date:		20170104
#	purpose:    demonstrates use of Python loops (while & for), and conditions,
#               prompt human player for input 
#               evaluate player input and determine a winner
#   reference:  https://docs.python.org/3.5/library/random.html#random.randint
#
#__________________________________
import random

rollAgain = "Y"

while rollAgain == "Y":
    roll = random.randint(1,6)
    print "You rolled a ",roll,"!"
    rollAgain = raw_input("Type 'Y' to roll again, or 'N' to not.")

if rollAgain == "N":
    print "See ya later!"
# Hangman Advanced
word = "banana"
turns = len(word)

guesses = ''
playing = True

while playing:
    failed = 0
    for letter in word:
        if letter in guesses:
            print letter   
        else:
            print "_"
            failed += 1
    if failed == 0:        
        print "\nYou won"
        break             

    print
    guess = raw_input("guess a character:")
    guesses = guesses + guess
    if guess not in word:
        turns -= 1  
        print "Wrong!"
        print "You have", + turns, 'more guesses'
        if turns == 0:
            print "You Lose\n"
            break
