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
