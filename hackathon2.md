---
layout: default
title: Elementary Programming Hackathon
---

## Elementary Programming Hackathon

Welcome to the **Elementary Programming Hackathon**! This is your chance to apply what you’ve learned, collaborate with classmates, and create something fun and meaningful. Let’s see how creative you can get with Python!

#### Outline:
* [Event Details](#details)
* [Resources](#resources)
* [Theme 1: Automate Your World and Everyday Tools](#theme1)
    * [Password Generator](password)
    * [Expense Tracker](expense)
    * [To-Do List Manager](todo)
    * [Grocery List Manager](grocery)
    * [Mileage Tracker](#mileage)
    * [Expense Splitter](#expense)
    * [Birthday Reminder](#birthday)
    * [Habit Tracker](#habit)
    * [Calculator](#calculator)
* [Theme 2: Game On](#theme2)
    * [Hangman Game](#hangman)
    * [Math Practice Game](#mathgame)
    * [Text-Based Adventure](#textadventure)
    * [Simple Trivia Game](#trivia)
    * [Rock, Paper, Scissors](#rockpaperscissors)
    * [Word Scramble](#wordscramble)
    * [Blackjack](#blackjack)
    * [Battleship](#battleship)
    * [Tic-Tac-Toe](#tictactoe)
    * [Text-Based Slot Machine](#slotmachine)
* [Theme 3: Data Exploration](#theme3)
    * [Movie Ratings](#movieratings)
    * [Groundhog Day Forecasts and Temperatures](#groundhog)
    * [80 Cereals](#cereals)
    * [UFO Sightings](#ufo)
    * [Starbucks Menu](#nutritionstarbucks)


### **Event Details** <a class="anchor" id="details"></a>
- **Three Themes**: 
    - Automate Your World and Everyday Tools: Build Python scripts to automate small tasks 
    - Game On: Create simple text-based games 
    - Data Exploration: Use Python to analyze and visualize a dataset
- **Student Tasks**:
    - Write one program for **each** of the three themes (3 total programs).
    - Provide code comments that document what the code does and how to run your program. 
    - Submit your code files on blackboard.


### Resources <a class="anchor" id="resources"></a>

#### Allowed
* The course web page
    * [Guides](/guides/index.md)
    * [Slides](schedule)
    * [Answers to labs](schedule)
* Your own code from this semester
* Web search for datasets
* Web search for Python reference information

#### Not allowed
* Absolutely **no AI or GPT** tools
* Web search for existing code


### **THEME 1:** Automate Your World and Everyday Tools <a class="anchor" id="theme1"></a>

Automate Your World and Everyday Tools theme combines the practicality of automation with the creativity of building everyday tools. It empowers students to develop Python programs that enhance productivity, streamline workflows, and tackle common challenges in daily life. From automating tedious tasks like reminders to creating functional utilities like budget trackers, to-do lists, and calculators, this theme encourages innovation with a focus on real-world applications. By blending automation and utility, students can explore how coding can transform repetitive or mundane tasks into efficient, enjoyable experiences, making technology an integral part of simplifying and improving their routines.

#### Password Generator <a class="anchor" id="password"></a>

A tool to generate strong, random passwords based on user-defined criteria (e.g., length, inclusion of special characters).

Key Features:
* Creates secure passwords.
* Option to save passwords to a file.
* Libraries: random, string


#### Expense Tracker <a class="anchor" id="expense"></a>

A tool to log daily expenses and generate a summary report.

Key Features:
* Calculates totals by category (e.g., food, transport).
* Logs expenses in a file.
* Charts expenses in a bar chart.
* Libraries: Matplotlib


#### To-Do List Manager <a class="anchor" id="todo"></a>

A simple script to manage a to-do list, adding, removing, and marking tasks as completed.

Key Features:
* Allows users to view, add, and delete tasks.
* Set task priorities, order by priority.
* Set task due dates.
* Saves tasks to a file.


#### Grocery List Manager <a class="anchor" id="grocery"></a>

Students build a program to manage a grocery shopping list.

Key Features:
* Add, remove, or view items in the list.
* Save the list to a file and load it when the program starts.
* Allow users to mark items as purchased.
* Include quantities for each item.

#### Mileage Tracker <a class="anchor" id="mileage"></a>

Calculate fuel efficiency based on miles driven and fuel used.

Key Features:
* Input: Distance driven and fuel consumed.
* Output: Miles per gallon (MPG).
* Save data for multiple trips.


#### Expense Splitter <a class="anchor" id="expense"></a>

A program to split bills among friends.

Key Features:
* Input: Total bill amount and list of friends.
* Output: Amount each person owes.
* Allow tracking of who has paid.


#### Birthday Reminder <a class="anchor" id="birthday"></a>

A program to store and remind users of upcoming birthdays.

Key Features:
* Add, view, and delete birthdays.
* Notify the user when a birthday is approaching.
* Sort birthdays by date.


#### Habit Tracker <a class="anchor" id="habit"></a>

Track daily habits and mark them as completed.

Key Features:
* Allow users to add, view, and mark habits.
* Display progress (e.g., percentage of completion for each habit).
* Save data to a file for persistence.


#### Calculator <a class="anchor" id="calculator"></a>

A utility that performs arithmetic operations.

Key Features:
* Allow users to input numbers and an operator.
* Display the result.
* Include advanced operations (e.g., square root, power).
* Libraries: math

### **THEME 2:** Game On <a class="anchor" id="theme2"></a>

The Game On theme invites students to unleash their creativity by designing and building text-based games that entertain, challenge, and engage. Whether crafting a thrilling adventure story, coding a classic guessing game, or simulating a competitive game like Rock, Paper, Scissors, this theme encourages problem-solving and interactive storytelling. By combining logic, user input, and Python programming fundamentals, students can create games that test skills, deliver fun experiences, and bring their unique ideas to life. “Game On” is all about making learning enjoyable while demonstrating the versatility and power of programming in an imaginative and playful way.

#### Hangman Game <a class="anchor" id="hangman"></a>

Create a text-based Hangman game.

Key Features:
* Randomly select a word from a predefined list.
* Display guessed letters and track remaining attempts.
* End with a win/lose message.


#### Math Practice Game <a class="anchor" id="mathgame"></a>

A program to generate random arithmetic problems (addition, subtraction, multiplication) for practice.

Key Features:
* Randomly generate problems.
* Evaluate the user’s answers and track their score.
* Display results (e.g., correct answers, total score) at the end.


#### Text-Based Adventure <a class="anchor" id="textadventure"></a>

An interactive story where players navigate a world by making choices (e.g., “Go north or south?”).

Key Features:
* Use conditionals and user input to create branching paths.
* Include win/lose conditions based on player choices.
* Add inventory management or simple combat mechanics.


#### Simple Trivia Game <a class="anchor" id="trivia"></a>

A quiz game with multiple-choice questions.

Key Features:
* Store questions and answers in a dictionary or list.
* Display the player’s score at the end.
* Randomize questions.
* Allow players to add their own questions for replay.


#### Rock, Paper, Scissors with Score Tracking <a class="anchor" id="rockpaperscissors"></a>

A more involved version of the classic game where the program keeps track of the score over multiple rounds.

Key Features:
* Use a loop to play multiple rounds.
* Add scoring logic: +1 for a win, 0 for a tie.
* Display the final score at the end.


#### Word Scramble <a class="anchor" id="wordscramble"></a>

A game where the player unscrambles a jumbled word.

Key Features:
* Randomly shuffle the letters of a word.
* Allow the player to guess until they get it right or give up.
* Include a hint or timer.
* Libraries: random


#### Blackjack <a class="anchor" id="blackjack"></a>

A simplified version of the card game Blackjack.

Key Features:
* Randomly deal cards.
* Allow the player to “hit” or “stand.”
* Calculate the winner based on Blackjack rules.
* Add simple betting mechanics.
* Libraries: random


#### Battleship <a class="anchor" id="battleship"></a>

A grid-based guessing game where the player tries to “hit” a hidden ship.

Key Features:
* Represent the grid as a list of lists.
* Use coordinates to track guesses and reveal hits.
* Add multiple ships and print the grid.


#### Tic-Tac-Toe <a class="anchor" id="tictactoe"></a>

A two-player game where users take turns marking spaces on a 3x3 grid.

Key Features:
* Use a list of lists to represent the board.
* Check for a win or draw after each turn.
* Add a single-player mode with basic AI.


#### Text-Based Slot Machine <a class="anchor" id="slotmachine"></a>

A game where players pull a lever to spin a slot machine and win based on matching symbols.

Key Features:
* Randomly generate symbols for the reels.
* Display winnings based on matching combinations.
* Include betting mechanics or multipliers for rare combinations.
* Libraries: random


### **THEME 3:** Data Exploration <a class="anchor" id="theme3"></a>

The Data Exploration theme empowers students to uncover insights and tell stories through data. By analyzing and visualizing datasets, students learn to transform raw information into meaningful patterns and trends. This theme combines programming fundamentals with critical thinking, as students explore topics ranging from movie ratings to weather patterns or sales data. Whether calculating statistics, identifying correlations, or creating visual representations like bar charts and line graphs, *Data Exploration* demonstrates the power of Python as a tool for understanding the world. It's an opportunity to blend creativity, curiosity, and technical skills to make data come alive.

#### Movie Ratings <a class="anchor" id="movieratings"></a>

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

**Potential Analysis**
1. **Genre Analysis**: Analyze the distribution of movies across genres.
2. **Rating Insights**: Explore high-rated movies and their genres.
3. **Visualization**: Create bar charts or pie charts to show the number of movies per genre or average rating by genre.
4. **Recommendations**: Identify top-rated movies within a specific genre.

**Data:**
[movie_ratings.csv](https://raw.githubusercontent.com/cmsc105-f24/code/refs/heads/main/movie_ratings.csv)


#### Groundhog Day Forecasts and Temperatures <a class="anchor" id="groundhog"></a>

**Context:**
Thousands gather at Gobbler’s Knob in Punxsutawney, Pennsylvania, on the second day of February to await the spring forecast from a groundhog known as *Punxsutawney Phil*. According to legend, if Phil sees his shadow the United States is in store for six more weeks of winter weather. But, if Phil doesn’t see his shadow, the country should expect warmer temperatures and the arrival of an early spring.

**Data:**
[groundhog_day_weather.csv](https://raw.githubusercontent.com/cmsc105-f24/code/refs/heads/main/groundhog_day_weather.csv)



#### 80 Cereals <a class="anchor" id="cereals"></a>

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



#### UFO Sightings <a class="anchor" id="ufo"></a>

**Context:**
This dataset contains over 80,000 reports of UFO sightings over the last century.

**Content:**
There are two versions of this dataset: scrubbed and complete. The complete data includes entries where the location of the sighting was not found or blank (0.8146%) or have an erroneous or blank time (8.0237%). Since the reports date back to the 20th century, some older data might be obscured. Data contains city, state, time, description, and duration of each sighting.

**Data:**
[ufo_sightings.csv](https://raw.githubusercontent.com/cmsc105-f24/code/refs/heads/main/ufo_sightings.csv)


#### Nutrition facts for Starbucks Menu <a class="anchor" id="nutritionstarbucks"></a>

**Context:**
Starbucks is an American coffee chain founded in Seattle. 

**Content:**
This dataset includes the nutritional information for Starbucks’ food menu items. 

**Data:**
[starbucks_menu_nutrition_facts.csv](https://raw.githubusercontent.com/cmsc105-f24/code/refs/heads/main/starbucks_menu_nutrition_facts.csv)




