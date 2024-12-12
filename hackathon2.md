---
layout: default
title: Elementary Programming Hackathon
---

# Elementary Programming Hackathon

Welcome to the **Elementary Programming Hackathon**! This is your chance to apply what you’ve learned, collaborate with classmates, and create something fun and meaningful. Let’s see how creative you can get with Python!

---

## **Event Details**
- **Themes**: 
    - Automate Your World: Build Python scripts to automate small tasks (e.g., file organization, data cleaning, or reminders).
    - Game On: Create simple text-based games (e.g., trivia, number guessing, or basic RPGs).
    - Data Exploration: Use Python to analyze and visualize a dataset.
    - Everyday Tools: Build small utilities like to-do lists, or calculators.

- **Tasks**:
    - Write one program for each theme.
    - Make sure that you provide test code for the program.
    - Make sure that your code is well documented.
    - Submit your code files on blackboard.


## Resources

* The course web page
    * Guides
    * Slides
    * Answers to labs

* Your own code from this semester

## Not allowed

* **No AI or GPT tools**
* **Web search for existing code**






### Automate Your World: Build Python scripts to automate small tasks

---

#### Password Generator

A tool to generate strong, random passwords based on user-defined criteria (e.g., length, inclusion of special characters).

Key Features:
* Creates secure passwords.
* Option to save passwords to a file.
* Libraries: random, string


#### Expense Tracker

A tool to log daily expenses and generate a summary report.

Key Features:
* Calculates totals by category (e.g., food, transport).
* Logs expenses in a file.
* Charts expenses in a bar chart.
* Libraries: Matplotlib


#### To-Do List Manager

A simple script to manage a to-do list, adding, removing, and marking tasks as completed.

Key Features:
* Allows users to view, add, and delete tasks.
* Set task priorities, order by priority.
* Set task due dates.
* Saves tasks to a file.


#### Grocery List Manager

Students build a program to manage a grocery shopping list.

Key Features:
* Add, remove, or view items in the list.
* Save the list to a file and load it when the program starts.
* Allow users to mark items as purchased.
* Include quantities for each item.



### Game On: Create simple text-based games (e.g., trivia, number guessing, or basic RPGs)

---

#### Hangman Game

Create a text-based Hangman game.

Key Features:
* Randomly select a word from a predefined list.
* Display guessed letters and track remaining attempts.
* End with a win/lose message.


#### Math Practice Game

A program to generate random arithmetic problems (addition, subtraction, multiplication) for practice.

Key Features:
* Randomly generate problems.
* Evaluate the user’s answers and track their score.
* Display results (e.g., correct answers, total score) at the end.


#### Text-Based Adventure

An interactive story where players navigate a world by making choices (e.g., “Go north or south?”).

Key Features:
* Use conditionals and user input to create branching paths.
* Include win/lose conditions based on player choices.
* Add inventory management or simple combat mechanics.


#### Simple Trivia Game

A quiz game with multiple-choice questions.

Key Features:
* Store questions and answers in a dictionary or list.
* Display the player’s score at the end.
* Randomize questions.
* Allow players to add their own questions for replay.


#### Rock, Paper, Scissors with Score Tracking

A more involved version of the classic game where the program keeps track of the score over multiple rounds.

Key Features:
* Use a loop to play multiple rounds.
* Add scoring logic: +1 for a win, 0 for a tie.
* Display the final score at the end.



#### Word Scramble

A game where the player unscrambles a jumbled word.

Key Features:
* Randomly shuffle the letters of a word.
* Allow the player to guess until they get it right or give up.
* Include a hint or timer.
* Libraries: random


#### Blackjack

A simplified version of the card game Blackjack.

Key Features:
* Randomly deal cards.
* Allow the player to “hit” or “stand.”
* Calculate the winner based on Blackjack rules.
* Add simple betting mechanics.
* Libraries: random


#### Battleship 

A grid-based guessing game where the player tries to “hit” a hidden ship.

Key Features:
* Represent the grid as a list of lists.
* Use coordinates to track guesses and reveal hits.
* Add multiple ships and print the grid.


#### Tic-Tac-Toe

A two-player game where users take turns marking spaces on a 3x3 grid.

Key Features:
* Use a list of lists to represent the board.
* Check for a win or draw after each turn.
* Add a single-player mode with basic AI.


#### Text-Based Slot Machine

A game where players pull a lever to spin a slot machine and win based on matching symbols.

Key Features:
* Randomly generate symbols for the reels.
* Display winnings based on matching combinations.
* Include betting mechanics or multipliers for rare combinations.
* Libraries: random




### Data Exploration: Use Python to analyze and visualize a dataset.

---

#### Movie 

**Overview:**
This dataset contains information about a collection of popular movies, including their titles, genres, and IMDb-style ratings. It can be used for data analysis, visualization, or building simple movie recommendation tools.

**Content:**
1. **Movie**
- **Description**: The title of the movie.
- **Type**: Text/String
- **Examples**:
  - "Inception"
  - "The Godfather"
  - "Frozen"

2. **Genre**
- **Description**: The genre or primary category of the movie.
- **Type**: Text/String
- **Examples**:
  - "Sci-Fi"
  - "Animation"
  - "Drama"

3. **Rating**
- **Description**: The IMDb-style rating for the movie (out of 10).
- **Type**: Numeric (Float)
- **Range**: 7.5 – 9.3
- **Examples**:
  - 8.8
  - 7.9
  - 9.2

---

**Example Rows**
| Movie                              | Genre       | Rating |
|------------------------------------|-------------|--------|
| Inception                          | Sci-Fi      | 8.8    |
| The Godfather                      | Crime       | 9.2    |
| Frozen                             | Animation   | 7.5    |
| The Shawshank Redemption           | Drama       | 9.3    |
| Spider-Man: Into the Spider-Verse  | Animation   | 8.4    |

---

**Potential Use Cases**
1. **Genre Analysis**: Analyze the distribution of movies across genres.
2. **Rating Insights**: Explore high-rated movies and their genres.
3. **Visualization**: Create bar charts or pie charts to show the number of movies per genre or average rating by genre.
4. **Recommendations**: Identify top-rated movies within a specific genre.

**Data:**
[movie_ratings.csv](https://raw.githubusercontent.com/cmsc105-f24/code/refs/heads/main/movie_ratings.csv)



#### Groundhog Day Forecasts and Temperatures

**Context:**
Thousands gather at Gobbler’s Knob in Punxsutawney, Pennsylvania, on the second day of February to await the spring forecast from a groundhog known as *Punxsutawney Phil*. According to legend, if Phil sees his shadow the United States is in store for six more weeks of winter weather. But, if Phil doesn’t see his shadow, the country should expect warmer temperatures and the arrival of an early spring.

**Data:**
[groundhog_day_weather.csv](https://raw.githubusercontent.com/cmsc105-f24/code/refs/heads/main/groundhog_day_weather.csv)



#### 80 Cereals

Nutrition data on 80 cereal products

**Context:**
If you like to eat cereal, do yourself a favor and avoid this dataset at all costs. After seeing these data it will never be the same for me to eat Fruity Pebbles again.


**Content:**
Fields in the dataset:

* Name: Name of cereal
* mfr: Manufacturer of cereal
    * A = American Home Food Products;
    * G = General Mills
    * K = Kelloggs
    * N = Nabisco
    * P = Post
    * Q = Quaker Oats
    * R = Ralston Purina
* type:
    * cold
    * hot
* calories: calories per serving
* protein: grams of protein
* fat: grams of fat
* sodium: milligrams of sodium
* fiber: grams of dietary fiber
* carbo: grams of complex carbohydrates
* sugars: grams of sugars
* potass: milligrams of potassium
* vitamins: vitamins and minerals - 0, 25, or 100, indicating the typical percentage of FDA recommended
* shelf: display shelf (1, 2, or 3, counting from the floor)
* weight: weight in ounces of one serving
* cups: number of cups in one serving
* rating: a rating of the cereals (Possibly from Consumer Reports?)

**Data:**
[cereal.csv](https://raw.githubusercontent.com/cmsc105-f24/code/refs/heads/main/cereal.csv)



#### UFO Sightings

**Context:**
This dataset contains over 80,000 reports of UFO sightings over the last century.

**Content:**
There are two versions of this dataset: scrubbed and complete. The complete data includes entries where the location of the sighting was not found or blank (0.8146%) or have an erroneous or blank time (8.0237%). Since the reports date back to the 20th century, some older data might be obscured. Data contains city, state, time, description, and duration of each sighting.

**Data:**
[ufo_sightings.csv](https://raw.githubusercontent.com/cmsc105-f24/code/refs/heads/main/ufo_sightings.csv)


#### Nutrition facts for Starbucks Menu

**Context:**
Starbucks is an American coffee chain founded in Seattle. 

**Content:**
This dataset includes the nutritional information for Starbucks’ food menu items. 

**Data:**
[starbucks_menu_nutrition_facts.csv](https://raw.githubusercontent.com/cmsc105-f24/code/refs/heads/main/starbucks_menu_nutrition_facts.csv)




### Everyday Tools: Build small utilities like to-do lists, or calculators.

---


#### Mileage Tracker

Calculate fuel efficiency based on miles driven and fuel used.

Key Features:
* Input: Distance driven and fuel consumed.
* Output: Miles per gallon (MPG).
* Save data for multiple trips.


#### Expense Splitter

A program to split bills among friends.

Key Features:
* Input: Total bill amount and list of friends.
* Output: Amount each person owes.
* Allow tracking of who has paid.


#### Birthday Reminder

A program to store and remind users of upcoming birthdays.

Key Features:
* Add, view, and delete birthdays.
* Notify the user when a birthday is approaching.
* Sort birthdays by date.



#### Habit Tracker

Track daily habits and mark them as completed.

Key Features:
* Allow users to add, view, and mark habits.
* Display progress (e.g., percentage of completion for each habit).
* Save data to a file for persistence.


#### Loan Payment Calculator

Calculate monthly loan payments based on the loan amount, interest rate, and term.

Key Features:
* Input: Principal amount, annual interest rate, and loan term (in years).
* Output: Monthly payment amount.
* Include total interest paid over the term.


#### Unit Converter

Convert units such as distance (miles to kilometers), weight (pounds to kilograms), and temperature (Celsius to Fahrenheit).

Key Features:
* Allow users to select the type of conversion.
* Input the value and display the converted result.
* Include additional units (e.g., time, volume).


#### Calculator

A utility that performs arithmetic operations.

Key Features:
* Allow users to input numbers and an operator.
* Display the result.
* Include advanced operations (e.g., square root, power).
* Libraries: math