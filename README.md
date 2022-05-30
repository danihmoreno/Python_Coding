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

#If the bill was $150.00, split between 5 people, with 12% tip. 
#Each person should pay (150.00 / 5) * 1.12 = 33.6
#Format the result to 2 decimal places = 33.60
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
