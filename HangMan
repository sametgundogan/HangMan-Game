import random

liste = ["CROW", "OWL", "EAGLE", "PIGEON", "SWALLOW", "FALCON", "PARROT", "SPARROW", "SWAN", "FLAMINGO", "PELICAN"]
word = None

def keyword(): # select a word from list randomly
    word = liste[random.randint(0,len(liste))]
    return word


the_word = keyword()
empty_key = list("_" * len(the_word)) 
print(empty_key)
def writer(takenletterr): # shows the letters if given is in the word
    for i in range(len(the_word)):
        if the_word[i] == takenletterr:
            empty_key[i] = takenletterr
    return empty_key


def checkLetter(): # for checking the letter
    takenletter = str(input("Write a letter: ")).upper()
    if not control(takenletter): 
        checkLetter() # to start again if the input is invalid
    else:
        flag = True
        for i in range(len(the_word)):
            if the_word[i] == takenletter:
                flag = False
                return writer(takenletter) # if the user hits, this shows the modifies step
        if flag:
            print("Try again!..") # if the user misses...
            flag = True


def control(takenletter): # controls the input if it is valid
    control = True
    if len(takenletter) > 1 or len(takenletter) == 0:
        print("You can write just one letter!")
        control = False
    return control


def checkWinner(): # to check whether the word is completed
    if empty_key.__contains__("_"):
        return False
    else:
        return True


print("Welcome to the Hangman Game!")
print("You have 12 attempts and have to guess a bird species... Let the game begin...")
count = 0
while count < 12: # 12 lives...
    count += 1
    print(checkLetter())
    if checkWinner():
        print("Congratulations! You won!!")
        break
    print("Last {} attempts..".format(12-count))
else:
    print("Sorry.. You Lost... The answer was: ", word)
