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
*Important*: You are not allowed to use the choice() function.

**Code:**

import random <br/>
names_string = input("Give me everybody's names, separated by a comma. ") <br/>
names = names_string.split(", ") <br/>
chosen = names[random.randint(0, len(names)-1)] <br/>
print(f"{chosen} is going to buy the meal today!") <br/>

**Output:**

Give me everybody's names, separated by a comma. Angela, Ben, Jenny, Michael, Chloe <br/>
Angela is going to buy the meal today!

## **Day 4 Project 3: Treasure Map Game**

**Instructions:**

You are going to write a program that will mark a spot with an X. <br/>
Your job is to write a program that allows you to mark a square on the map using a two-digit system. <br/>
The first digit is the vertical column number and the second digit is the horizontal row number. <br/>
First, your program must take the user input and convert it to a usable format. <br/>
Next, you need to use it to update your nested list with an "x".

**Code:**

row1 = ["⬜️","⬜️","⬜️"] <br/>
row2 = ["⬜️","⬜️","⬜️"] <br/>
row3 = ["⬜️","⬜️","⬜️"] <br/>
map = [row1, row2, row3] <br/>
print(f"{row1}\n{row2}\n{row3}") <br/>
position = input("Where do you want to put the treasure? ") <br/>

map[int(position[1]) - 1][int(position[0]) - 1] = "x" <br/>

print(f"{row1}\n{row2}\n{row3}") <br/>

**Output:**

['⬜️', '⬜️', '⬜️'] <br/>
['⬜️', '⬜️', '⬜️'] <br/>
['⬜️', '⬜️', '⬜️'] <br/>
Where do you want to put the treasure? 32 <br/>
['⬜️', '⬜️', '⬜️'] <br/>
['⬜️', '⬜️', 'x'] <br/>
['⬜️', '⬜️', '⬜️'] <br/>

## **Day 4 Final Project: Rock, Paper, Scissors**

**Instructions:**

Make a rock, paper, scissors game. <br/>

Start the game by asking the player: <br/>
"What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors." <br/>

From there you will need to figure out:
* How you will store the user's input.
* How you will generate a random choice for the computer.
* How you will compare the user's and the computer's choice to determine the winner (or a draw).
* And also how you will give feedback to the player.

**Code:**

rock = ''' <br/>
✊ <br/>
''' <br/>

paper = ''' <br/>
✋ <br/>
''' <br/>

scissors = ''' <br/>
✌️ <br/>
''' <br/>

import random <br/>

player = input("What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors. \n") <br/>
computer = random.randint(0, 2) <br/>
options = [rock, paper, scissors] <br/>

if not 0 <= int(player) <= 2: <br/>
&emsp;  print("You typed an invalid number. Try again!") <br/>
else: <br/>
&emsp;  print(f"You chose {options[int(player)]}") <br/>
&emsp;  print(f"Computer chose {options[int(computer)]}") <br/>
&emsp;  if int(player) == 0 and int(computer) == 2: <br/>
&emsp;&emsp;    print("You win!") <br/>
&emsp;  elif int(player) == 1 and int(computer) == 0: <br/>
&emsp;&emsp;    print("You win!") <br/>
&emsp;  elif int(player) == 2 and int(computer) == 1: <br/>
&emsp;&emsp;    print("You win!") <br/>
&emsp;  elif int(player) == int(computer): <br/>
&emsp;&emsp;    print("It's a draw") <br/>
&emsp;  else: <br/>
&emsp;&emsp;    print("You lose!") <br/>

**Output:**

What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors.  <br/>
0 <br/>
You chose <br/>
✊ <br/>

Computer chose  <br/>
✌️ <br/>

You win! <br/>

## **Day 5 Project 1: Average Height**

**Instructions:**

You are going to write a program that calculates the average student height, rounded to the nearest whole number, from a List of heights. <br/>
*Important* You should not use the sum() or len() functions in your answer. <br/>
You should try to replicate their functionality using what you have learnt about for loops. <br/>

**Code:**

student_heights = input("Input a list of student heights:  \n").split() <br/>
for n in range(0, len(student_heights)): <br/>
&emsp;  student_heights[n] = int(student_heights[n]) <br/>
  
sum_heights = 0 <br/>
students = 0 <br/>
for height in student_heights: <br/>
&emsp;    sum_heights += height <br/>
&emsp;    students += 1 <br/>

average_height = round(sum_heights / students , 0) <br/>

print(f"The average student height is {average_height:.0f}") <br/>

**Output:**

Input a list of student heights: <br/>
156 178 165 171 187 <br/>
The average student height is 171 <br/>

## **Day 5 Project 2: High Score**

**Instructions:**

You are going to write a program that calculates the highest score from a List of scores. <br/>
*Important* you are not allowed to use the max or min functions. <br/>
Think about the logic before writing code. How can you compare numbers against each other to see which one is larger? <br/>

**Code:**

student_scores = input("Input a list of student scores: ").split() <br/>
for n in range(0, len(student_scores)): <br/>
&emsp;  student_scores[n] = int(student_scores[n]) <br/>
print(student_scores) <br/>

high_score = 0 <br/>

for score in student_scores: <br/>
&emsp;    if score > high_score: <br/>
&emsp;&emsp;        high_score = score <br/>

print(f"The highest score in the class is: {high_score}") <br/>

**Output:**

Input a list of student scores: 78 65 89 86 55 91 64 89 <br/>
[78, 65, 89, 86, 55, 91, 64, 89] <br/>
The highest score in the class is: 91 <br/>

## **Day 5 Project 3: Adding Even Numbers**

**Instructions:**

You are going to write a program that calculates the sum of all the even numbers from 1 to 100. <br/>
Thus, the first even number would be 2 and the last one is 100: <br/>
i.e. 2 + 4 + 6 + 8 +10 ... + 98 + 100 <br/>
*Important*, there should only be 1 print statement in your console output. It should just print the final total and not every step of the calculation. <br/>

**Code:**

total = 0 <br/>
for number in range(2, 101, 2): <br/>
&emsp;    total += number <br/>
print(total) <br/>

**Output:**

2550 <br/>

## **Day 5 Project 4: FizzBuzz**

**Instructions:**

You are going to write a program that automatically prints the solution to the FizzBuzz game. <br/>
Your program should print each number from 1 to 100 in turn. <br/>
* When the number is divisible by 3 then instead of printing the number it should print "Fizz".
* When the number is divisible by 5, then instead of printing the number it should print "Buzz".
* And if the number is divisible by both 3 and 5 e.g. 15 then instead of the number it should print "FizzBuzz"

**Code:**

for i in range(1, 101): <br/>
&emsp;    if i % 15 == 0: <br/>
&emsp;&emsp;        print("FizzBuzz") <br/>
&emsp;    elif i % 3 == 0: <br/>
&emsp;&emsp;        print("Fizz") <br/>
&emsp;    elif i % 5 == 0: <br/>
&emsp;&emsp;        print("Buzz") <br/>
&emsp;    else: <br/>
&emsp;&emsp;        print(i) <br/>

**Output:**

1 <br/>
2 <br/>
Fizz <br/>
4 <br/>
Buzz <br/>
Fizz <br/>
7 <br/>
8 <br/>
Fizz <br/>
Buzz <br/>
11 <br/>
Fizz <br/>
13 <br/>
14 <br/>
FizzBuzz <br/>
16 <br/>
17 <br/>
Fizz <br/>
19 <br/>
Buzz <br/>
Fizz <br/>
22 <br/>
23 <br/>
Fizz <br/>
Buzz <br/>
26 <br/>
Fizz <br/>
28 <br/>
29 <br/>
FizzBuzz <br/>
31 <br/>
32 <br/>
Fizz <br/>
34 <br/>
Buzz <br/>
Fizz <br/>
37 <br/>
38 <br/>
Fizz <br/>
Buzz <br/>
41 <br/>
Fizz <br/>
43 <br/>
44 <br/>
FizzBuzz <br/>
46 <br/>
47 <br/>
Fizz <br/>
49 <br/>
Buzz <br/>
Fizz <br/>
52 <br/>
53 <br/>
Fizz <br/>
Buzz <br/>
56 <br/>
Fizz <br/>
58 <br/>
59 <br/>
FizzBuzz <br/>
61 <br/>
62 <br/>
Fizz <br/>
64 <br/>
Buzz <br/>
Fizz <br/>
67 <br/>
68 <br/>
Fizz <br/>
Buzz <br/>
71 <br/>
Fizz <br/>
73 <br/>
74 <br/>
FizzBuzz <br/>
76 <br/>
77 <br/>
Fizz <br/>
79 <br/>
Buzz <br/>
Fizz <br/>
82 <br/>
83 <br/>
Fizz <br/>
Buzz <br/>
86 <br/>
Fizz <br/>
88 <br/>
89 <br/>
FizzBuzz <br/>
91 <br/>
92 <br/>
Fizz <br/>
94 <br/>
Buzz <br/>
Fizz <br/>
97 <br/>
98 <br/>
Fizz <br/>
Buzz <br/>

## **Day 5 Final Project: Safe Password Generator**

**Instructions:**

You are going to write a program that generates a random password based on how many characters the user wishes to have of the following types:
* Lowercase Letters: a-z
* Capital Letters: A-Z
* Numbers: 0-9
* Symbols: !, #, $, %, &, (, ), *, +

**Code:**

import random <br/>

lowercase_letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z'] <br/>
capital_letters = ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z'] <br/>
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9'] <br/>
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+'] <br/>

print("Welcome to the PyPassword Generator! \n") <br/>
nr_lowercase_letters = int(input("How many lowercase letters would you like in your password?\n")) <br/>
nr_capital_letters = int(input("How many capital letters would you like in your password?\n")) <br/>
nr_symbols = int(input(f"How many symbols would you like?\n")) <br/>
nr_numbers = int(input(f"How many numbers would you like?\n")) <br/>

character_types = [lowercase_letters, capital_letters, numbers, symbols] <br/>

if not 1 <= nr_lowercase_letters <= 5 or not 1 <= nr_capital_letters <= 5 or not 1 <= nr_symbols <= 5 or not 1 <= nr_numbers <= 5: <br/>
&emsp;  print("\nPlease chose between 1 and 5 for each character type! \n") <br/>
else: <br/>
&emsp;  total_characters = nr_lowercase_letters + nr_capital_letters + nr_symbols + nr_numbers <br/>
  
&emsp;  password = "" <br/>
  
&emsp;  for password_character in range(1, total_characters + 1): <br/>
&emsp;&emsp;    type = random.randint(0, 3) <br/>
&emsp;&emsp;    character_position = random.randint(0, len(character_types[type]) - 1) <br/>
&emsp;&emsp;    character = character_types[type][character_position] <br/>
&emsp;&emsp;    password = password + character <br/>
  
&emsp;  print(f"\nYour password is:\n{password}") <br/>

**Output:**

Welcome to the PyPassword Generator! <br/>

How many lowercase letters would you like in your password? <br/>
5 <br/>
How many capital letters would you like in your password? <br/>
4 <br/>
How many symbols would you like? <br/>
3 <br/>
How many numbers would you like? <br/>
2 <br/>

Your password is: <br/>
i+M%98Wwwub+LS <br/>

## **Day 7 Final Project: Hangman**

**Instructions:**

You are going to write a program that replicates the game Hangman

**Code:**

import random <br/>
from hangman_words import word_list <br/>
from hangman_art import logo <br/>

chosen_word = random.choice(word_list) <br/>
word_length = len(chosen_word) <br/>
end_of_game = False <br/>
lives = 6 <br/>
print(logo) <br/>

display = [] <br/>
for _ in range(word_length): <br/>
&emsp;    display += "_" <br/>

guess_list = [] <br/>
while not end_of_game: <br/>
&emsp;    guess = input("Guess a letter: ").lower() <br/>
&emsp;    if guess == "answer": <br/>
&emsp;&emsp;      print(f'Pssst, the solution is: "{chosen_word}".') <br/>
&emsp;    else: <br/>
&emsp;&emsp;      if guess in display: <br/>
&emsp;&emsp;&emsp;          print(f"You've already guessed {guess}") <br/>
&emsp;&emsp;      for position in range(word_length): <br/>
&emsp;&emsp;&emsp;          letter = chosen_word[position] <br/>
&emsp;&emsp;&emsp;          if letter == guess: <br/>
&emsp;&emsp;&emsp;&emsp;              display[position] = letter <br/>
&emsp;&emsp;      if guess in guess_list: <br/>
&emsp;&emsp;&emsp;        print(f"'{guess}' was already guessed!") <br/>
&emsp;&emsp;      else: <br/>
&emsp;&emsp;&emsp;        guess_list.append(guess) <br/>
&emsp;&emsp;      if guess not in chosen_word: <br/>
&emsp;&emsp;&emsp;          print(f"You guessed {guess}, that's not in the word. You lose a life.") <br/>
&emsp;&emsp;&emsp;          lives -= 1 <br/>
&emsp;&emsp;&emsp;          if lives == 0: <br/>
&emsp;&emsp;&emsp;&emsp;              end_of_game = True <br/>
&emsp;&emsp;&emsp;&emsp;              print("You lose.") <br/>
&emsp;&emsp;      print(f"{' '.join(display)}") <br/>
&emsp;&emsp;      print(f"Guesses: {guess_list}") <br/>
&emsp;&emsp;      if "_" not in display: <br/>
&emsp;&emsp;&emsp;          end_of_game = True <br/>
&emsp;&emsp;&emsp;          print("You win.") <br/>
&emsp;&emsp;      from hangman_art import stages <br/>
&emsp;&emsp;      print(stages[lives]) <br/>

**Output:**

 _                                              <br/>
| |                                             <br/>
| |__   __ _ _ __   __ _ _ __ ___   __ _ _ __   <br/>
| '_ \ / _` | '_ \ / _` | '_ ` _ \ / _` | '_ \  <br/>
| | | | (_| | | | | (_| | | | | | | (_| | | | | <br/>
|_| |_|\__,_|_| |_|\__, |_| |_| |_|\__,_|_| |_| <br/>
                    __/ |                       <br/>
                   |___/                        <br/>

Guess a letter: m <br/>
a x i o m <br/>
Guesses: ['a', 'e', 'i', 'o', 'u', 'd', 'n', 'l', 'x', 'm'] <br/>
You win. <br/>

--+===+ <br/>
--|---| <br/>
--O---| <br/>
-/|\--| <br/>
-/----| <br/>
------| <br/>
========= <br/>

