# Python_Coding
Results of a 100 Days of Coding course with gradually increasing difficulty.

## **Day 1 Project: Band Name Generator**

**Instructions:**

#1. Create a greeting for your program. <br/>
#2. Ask the user for the city that they grew up in. <br/>
#3. Ask the user for the name of a pet. <br/>
#4. Combine the name of their city and pet and show them their band name. <br/>
#5. Make sure the input cursor shows on a new line, see the example at:
https://replit.com/@appbrewery/band-name-generator-end

**Code:**

print("Welcome to Band Name Generator") <br/>
city = input("What city did you grow up in? \n") <br/>
pet = input("What is the name of your pet? \n") <br/>
print("Your band name could be " + city + " " + pet) <br/>

**Output:**

Welcome to Band Name Generator <br/>
What city did you grow up in? <br/>
São Paulo <br/>
What is the name of your pet? <br/>
Freddy <br/>
Your band name could be São Paulo Freddy

## **Day 2 Project: Tip Calculator**

**Instructions:**

#If the bill was $150.00, split between 5 people, with 12% tip. <br/>
#Each person should pay (150.00 / 5) * 1.12 = 33.6 <br/>
#Format the result to 2 decimal places = 33.60 <br/>
#Tip: There are 2 ways to round a number. You might have to do some Googling to solve this.

**Code:**

print("Welcome to the tip calculator!") <br/>
bill = input("What was the total bill? \n") <br/>
tip = input("How much tip would you like to give? 10, 12, or 15? \n") <br/>
party = input("How many people to split the bill? \n") <br/>
total_per_person = round((float(bill)/int(party))*(1+int(tip)/100) , 2) <br/>
print(f"Each person should pay: ${total_per_person: .2f}")

**Output:**

Welcome to the tip calculator! <br/>
What was the total bill? <br/>
$150.00 <br/>
How much tip would you like to give? 10, 12, or 15? <br/>
12 <br/>
How many people to split the bill? <br/>
5 <br/>
Each person should pay: $ 33.60

## **Day 3 Project 1: Odd or Even**

**Instructions:**

#Write a program that works out whether if a given number is an odd or even number. <br/>
Even numbers can be divided by 2 with no remainder. <br/>
e.g. 86 is even because 86 ÷ 2 = 43 <br/>
43 does not have any decimal places. Therefore the division is clean. <br/>
e.g. 59 is odd because 59 ÷ 2 = 29.5 <br/>
29.5 is not a whole number, it has decimal places. Therefore there is a remainder of 0.5, so the division is not clean. <br/>

The modulo is written as a percentage sign (%) in Python. It gives you the remainder after a division. <br/>

**Code:**

number = int(input("Which number do you want to check? ")) <br/>

if number % 2 == 0: <br/>
&emsp;    print("This is an even number.") <br/>
else: <br/>
&emsp;    print("This is an odd number.") <br/>

**Output:**

Which number do you want to check? 43 <br/>
This is an odd number.

## **Day 3 Project 2: BMI Calculator**

**Instructions:**

#Write a program that interprets the Body Mass Index (BMI) based on a user's weight and height. <br/>
#It should tell them the interpretation of their BMI based on the BMI value. <br/>
* Under 18.5 they are underweight <br/>
* Over 18.5 but below 25 they have a normal weight <br/>
* Over 25 but below 30 they are slightly overweight <br/>
* Over 30 but below 35 they are obese <br/>
* Above 35 they are clinically obese. <br/>

#Warning you should round the result to the nearest whole number. The interpretation message needs to include the words in bold from the interpretations above. e.g. **underweight, normal weight, overweight, obese, clinically obese**.

**Code:**

height = float(input("enter your height in m: ")) <br/>
weight = float(input("enter your weight in kg: ")) <br/>

BMI = weight / height**2 <br/>

if BMI < 18.5: <br/>
&emsp;    print("Your BMI is " + str(f'{round(BMI, 0):.0f}') + ", you are underweight.") <br/>
elif BMI < 25: <br/>
&emsp;    print("Your BMI is " + str(f'{round(BMI, 0):.0f}') + ", you have a normal weight.") <br/>
elif BMI < 30: <br/>
&emsp;    print("Your BMI is " + str(f'{round(BMI, 0):.0f}') + ", you are slightly overweight.") <br/>
elif BMI < 35: <br/>
&emsp;    print("Your BMI is " + str(f'{round(BMI, 0):.0f}') + ", you are obese.") <br/>
else: <br/>
&emsp;    print("Your BMI is " + str(f'{round(BMI, 0):.0f}') + ", you are clinically obese.")

**Output:**

enter your height in m: 1.77 <br/>
enter your weight in kg: 100 <br/>
Your BMI is 32, you are obese. <br/>

## **Day 3 Project 3: Leap Year**

**Instructions:**

#Write a program that works out whether if a given year is a leap year. A normal year has 365 days, leap years have 366, with an extra day in February. The reason why we have leap years is really fascinating, this video does it more justice: https://www.youtube.com/watch?v=xX96xng7sAE

This is how you work out whether if a particular year is a leap year. <br/>
* on every year that is evenly divisible by 4 
* **except** every year that is evenly divisible by 100 
* **unless** the year is also evenly divisible by 400

**Code:**

year = int(input("Which year do you want to check? ")) <br/>
if year % 4 == 0: <br/>
&emsp;    if year % 100 == 0: <br/>
&emsp;&emsp;        if year % 400 == 0: <br/>
&emsp;&emsp;&emsp;            print("Leap year.") <br/>
&emsp;&emsp;        else: <br/>
&emsp;&emsp;&emsp;            print("Not leap year.") <br/>
&emsp;    else: <br/>
&emsp;&emsp;        print("Leap year.") <br/>
else: <br/>
&emsp;    print("Not leap year.")

**Output:**

Which year do you want to check? 2000 <br/>
Leap year. <br/>
Which year do you want to check? 2100 <br/>
Not leap year.

## **Day 3 Project 4: Pizza Order**

**Instructions:**

#Congratulations, you've got a job at Python Pizza. Your first job is to build an automatic pizza order program. <br/>
#Based on a user's order, work out their final bill. <br/>
* Small Pizza: $15 <br/>
* Medium Pizza: $20 <br/>
* Large Pizza: $25 <br/>
* Pepperoni for Small Pizza: +$2 <br/>
* Pepperoni for Medium or Large Pizza: +$3 <br/>
* Extra cheese for any size pizza: + $1

**Code:**

print("Welcome to Python Pizza Deliveries!") <br/>
size = input("What size pizza do you want? S, M, or L \n") <br/>
add_pepperoni = input("Do you want pepperoni? Y or N \n") <br/>
extra_cheese = input("Do you want extra cheese? Y or N \n") <br/>

if size == "S": <br/>
&emsp;    price = 15 <br/>
elif size == "M": <br/>
&emsp;    price = 20 <br/>
elif size == "L": <br/>
&emsp;    price = 25 <br/>

if add_pepperoni == "Y": <br/>
&emsp;    if size == "S": <br/>
&emsp;&emsp;        price += 2 <br/>
&emsp;    else: <br/>
&emsp;&emsp;        price += 3 <br/>

if extra_cheese == "Y": <br/>
&emsp;    price += 1

print(f"Your final bill is: ${price:.0f}.")

**Output:**

Welcome to Python Pizza Deliveries! <br/>
What size pizza do you want? S, M, or L <br/> 
L <br/>
Do you want pepperoni? Y or N <br/>
Y <br/>
Do you want extra cheese? Y or N <br/>
N <br/>
Your final bill is: $28.

## **Day 3 Project 5: Love Calculator**

**Instructions:**

#You are going to write a program that tests the compatibility between two people. <br/>
#To work out the love score between two people: <br/>
* Take both people's names and check for the number of times the letters in the word TRUE occurs. <br/>
* Then check for the number of times the letters in the word LOVE occurs. <br/>
* Then combine these numbers to make a 2 digit number. <br/>

For Love Scores less than 10 or greater than 90, the message should be: <br/>
"Your score is **x**, you go together like coke and mentos." <br/>

For Love Scores between 40 and 50, the message should be: <br/>
"Your score is **y**, you are alright together." <br/>

Otherwise, the message will just be their score. e.g.: <br/>
"Your score is **z**." <br/>

e.g. <br/>
name1 = "Angela Yu" <br/>
name2 = "Jack Bauer" <br/>
T occurs 0 times <br/>
R occurs 1 time <br/>
U occurs 2 times <br/>
E occurs 2 times <br/>
Total = 5 <br/>
L occurs 1 time <br/>
O occurs 0 times <br/>
V occurs 0 times <br/>
E occurs 2 times <br/>
Total = 3 <br/>
Love Score = 53 <br/>
Print: "Your score is 53."

**Code:**

print("Welcome to the Love Calculator!") <br/>
name1 = input("What is your name? \n") <br/>
name2 = input("What is their name? \n") <br/>
full_name = name1 + name2 <br/>
t = full_name.lower().count("t") <br/>
r = full_name.lower().count("r") <br/>
u = full_name.lower().count("u") <br/>
e = full_name.lower().count("e") <br/>
l = full_name.lower().count("l") <br/>
o = full_name.lower().count("o") <br/>
v = full_name.lower().count("v") <br/>
e = full_name.lower().count("e") <br/>
score = (t+r+u+e)*10 + (l+o+v+e) <br/>
if score < 10 or score > 90: <br/>
&emsp;    print(f"Your score is {score:.0f}, you go together like coke and mentos.") <br/>
elif score >= 40 and score <= 50: <br/>
&emsp;    print(f"Your score is {score:.0f}, you are alright together.") <br/>
else: <br/>
&emsp;    print(f"Your score is {score:.0f}.")

**Output:**

Welcome to the Love Calculator! <br/>
What is your name?  <br/>
Kanye West <br/>
What is their name? <br/> 
Kim Kardashian <br/>
Your score is 42, you are alright together.

## **Day 3 Final Project: Treasure Island Game**

**Instructions:**

#Make your own "Choose Your Own Adventure" game. Use conditionals such as if, else, and elif statements to lay out the logic and the story's path in your program. <br/>
Have a think about how you might write your program to make a player's answers less case-sensitive. In other words, your code should work regardless of whether your user answers "left" or "Left". <br/>
You can also add your own ASCII art. Just remember to add three single quotes ''' at the start and at the end of your artwork to turn it into a multi-line string. <br/>

**Code:**

print(''' <br/>
******************************************************************************* <br/>
          |                   |                  |                     | <br/>
 _________|________________.=""_;=.______________|_____________________|_______ <br/>
|                   |  ,-"_,=""     `"=.|                  | <br/>
|___________________|__"=._o`"-._        `"=.______________|___________________ <br/>
          |                `"=._o`"=._      _`"=._                     | <br/>
 _________|_____________________:=._o "=._."_.-="'"=.__________________|_______ <br/>
|                   |    __.--" , ; `"=._o." ,-"""-._ ".   | <br/>
|___________________|_._"  ,. .` ` `` ,  `"-._"-._   ". '__|___________________ <br/>
          |           |o`"=._` , "` `; .". ,  "-._"-._; ;              | <br/>
 _________|___________| ;`-.o`"=._; ." ` '`."\` . "-._ /_______________|_______ <br/>
|                   | |o;    `"-.o`"=._``  '` " ,__.--o;   | <br/>
|___________________|_| ;     (#) `-.o `"=.`_.--"_o.-; ;___|___________________ <br/>
____/______/______/___|o;._    "      `".o|o_.--"    ;o;____/______/______/____ <br/>
/______/______/______/_"=._o--._        ; | ;        ; ;/______/______/______/_ <br/>
____/______/______/______/__"=._o--._   ;o|o;     _._;o;____/______/______/____ <br/>
/______/______/______/______/____"=._o._; | ;_.--"o.--"_/______/______/______/_ <br/>
____/______/______/______/______/_____"=.o|o_.--""___/______/______/______/____ <br/>
/______/______/______/______/______/______/______/______/______/______/_____ / <br/>
******************************************************************************* <br/>
''') <br/>
print("Welcome to Treasure Island.") <br/>
print("Your mission is to find the treasure.") <br/>

choice1 = input('You\'re at a cross road. Where do you want to go? Type "left" or "right" \n').lower() <br/>
if choice1 == "left": <br/>
&emsp;  choice2 = input('You\'ve come to a lake. There is an island in the middle of the lake. Type "wait" to wait for a boat. Type "swim" to swim across. \n').lower() <br/>
&emsp;  if choice2 == "wait": <br/>
&emsp;&emsp;    choice3 = input("You arrive at the island unharmed. There is a house with 3 doors. One red, one yellow and one blue. Which colour do you choose? \n").lower() <br/>
&emsp;&emsp;    if choice3 == "red": <br/>
&emsp;&emsp;&emsp;      print("It's a room full of fire. Game Over.") <br/>
&emsp;&emsp;    elif choice3 == "yellow": <br/>
&emsp;&emsp;&emsp;      print("You found the treasure! You Win!") <br/>
&emsp;&emsp;    elif choice3 == "blue": <br/>
&emsp;&emsp;&emsp;      print("You enter a room of beasts. Game Over.") <br/>
&emsp;&emsp;    else: <br/>
&emsp;&emsp;&emsp;      print("You chose a door that doesn't exist. Game Over.") <br/>
&emsp;  else: <br/>
&emsp;&emsp;    print("You get attacked by an angry trout. Game Over.") <br/>
else: <br/>
&emsp;  print("You fell into a hole. Game Over.") <br/>

**Output:**

******************************************************************************* <br/>
          |                   |                  |                     | <br/>
 _________|________________.=""_;=.______________|_____________________|_______ <br/>
|                   |  ,-"_,=""     `"=.|                  | <br/>
|___________________|__"=._o`"-._        `"=.______________|___________________ <br/>
          |                `"=._o`"=._      _`"=._                     | <br/>
 _________|_____________________:=._o "=._."_.-="'"=.__________________|_______ <br/>
|                   |    __.--" , ; `"=._o." ,-"""-._ ".   | <br/>
|___________________|_._"  ,. .` ` `` ,  `"-._"-._   ". '__|___________________ <br/>
          |           |o`"=._` , "` `; .". ,  "-._"-._; ;              | <br/>
 _________|___________| ;`-.o`"=._; ." ` '`."\` . "-._ /_______________|_______ <br/>
|                   | |o;    `"-.o`"=._``  '` " ,__.--o;   | <br/>
|___________________|_| ;     (#) `-.o `"=.`_.--"_o.-; ;___|___________________ <br/>
____/______/______/___|o;._    "      `".o|o_.--"    ;o;____/______/______/____ <br/>
/______/______/______/_"=._o--._        ; | ;        ; ;/______/______/______/_ <br/>
____/______/______/______/__"=._o--._   ;o|o;     _._;o;____/______/______/____ <br/>
/______/______/______/______/____"=._o._; | ;_.--"o.--"_/______/______/______/_ <br/>
____/______/______/______/______/_____"=.o|o_.--""___/______/______/______/____ <br/>
/______/______/______/______/______/______/______/______/______/______/_____ / <br/>
******************************************************************************* <br/>

Welcome to Treasure Island. <br/>
Your mission is to find the treasure. <br/>
You're at a cross road. Where do you want to go? Type "left" or "right"  <br/>
left <br/>
You've come to a lake. There is an island in the middle of the lake. Type "wait" to wait for a boat. Type "swim" to swim across.  <br/>
wait <br/>
You arrive at the island unharmed. There is a house with 3 doors. One red, one yellow and one blue. Which colour do you choose?  <br/>
red <br/>
It's a room full of fire. Game Over. <br/>

## **Day 4 Project 1: Heads or Tails**

**Instructions:**

You are going to write a virtual coin toss program. It will randomly tell the user "Heads" or "Tails". <br/>
There are many ways of doing this. But you should generate a random number, either 0 or 1. Then use that number to print out Heads or Tails. <br/>
e.g. 1 means Heads 0 means Tails

**Code:**

import random <br/>
random_side = random.randint(0, 1) <br/>
if random_side == 0: <br/>
&emsp;    print("Tails") <br/>
else: <br/>
&emsp;    print("Heads") <br/>

**Output:**

Tails

## **Day 4 Project 2: Who's Paying the Bill?**

**Instructions:**

You are going to write a program that will select a random name from a list of names. <br/>
The person selected will have to pay for everybody's food bill. <br/>

**Code:**

import random <br/>
names_string = input("Give me everybody's names, separated by a comma. ") <br/>
names = names_string.split(", ") <br/>
chosen = names[random.randint(0, len(names)-1)] <br/>
print(f"{chosen} is going to buy the meal today!") <br/>

**Output:**

Give me everybody's names, separated by a comma. Angela, Ben, Jenny, Michael, Chloe <br/>
Angela is going to buy the meal today!

## **Day 4 Project 3: **

**Instructions:**

 <br/>

**Code:**

import random <br/>
 <br/>

**Output:**

 <br/>

