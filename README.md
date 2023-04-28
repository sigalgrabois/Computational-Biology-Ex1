# Computational-Biology-Ex1
This exercise has been writen by Sigal grabois and Roi Avraham.
# Description
In this exercise we have to write a cellular automaton in which we investigated how a rumor distribution network works.
For the sake of researching this style, we created a 100x100 grid where each cell can be occupied by one person.
We denoted the population density by the parameter P which we will change throughout the study.
Each person in the population has a level of skepticism that is one of {s_4,s_3,s_2,s_1}, 
where these indicate: a person who does not believe any rumor, a person whose basic probability of believing a rumor is 1/3,
a person whose basic probability of believing a rumor is 2/3 and a person who believes .
for each rumor respectively.
The level of skepticism of each person is fixed randomly, and the percentage of people from each group of level of 
skepticism was also a parameter that we investigated. We chose the percentage of each group from the population by
using parameters 1S, 2S, 3S and 4S when they are also in accordance with the different levels of skepticism defined.

Basic rules of the network
1. First, we will select one person from the entire population who will determine to be the one who starts the rumor (passes it to all his neighbors).
2. The person who receives a rumor decides according to his level of skepticism whether to pass on the rumor
    a. If you chose to transfer the rumor - the transfer is always carried out in the next generation immediately after receiving the rumor
    b. Otherwise, continue without spreading.
3. If in the same generation a person receives a rumor from at least 2 different neighbors - his level of skepticism will temporarily drop
   to that generation and will act in the form of one level of skepticism below.
4. If a person passed on the rumor, he will not pass it on for L generations (a learned parameter) and then only if he receives a rumor 
   again will he be able to pass it on.
  
# Installation
    You can download the code by git clone: https://github.com/sigalgrabois/Computational-Biology-Ex1.git.
    There are 2 options to run the code:
       1. In the folder there is an exe file for fast execution by double-clicking on: SpreadingRumor.exe.
       2. You can run the main.py file. in order to do so you will need the install by pip install the next libaries:
       * tkinter
       * numpy
       * random
       * matplotlib
    
# Usage
 The application has a configure bar for the purpose of studying the rate of spreading the rumor among the population<br>. The user can choose the following:<br>
 1)the values density percentage (P) - must be number between 0 to 1 <br>2) choose the probability of the diffrent levels of the Skeptisem (s1,s2,s3,s4) -must be numbers between 0 to 1 and must sum up to 1. <br>3)choose the number of generations the automat will run (Generation limit (Optional)) <br>4) choose the run mode: there are 3 options: R - regular mode (this is the code for סעיף א). S - slow mode (this is code for סעיף ב). F - fast mode(this is code for סעיף ב) 
    <br>While running, the user receives important information about the system, such as the total percentage of pepole who heard the rumor, the number of pepole who heard the rumor. At the end of the run, <br>when the user clicks on the 'Stop' button, a graph will appear.

note: When using the slow mode, the first strategy from the report been used.

# Dictionary
app.py - Document containing the app settings, windows, grid, entries and buttons.
<br>
automat.py - Document that containing the engine behind the simulator. Calculates the number and postion of the persons inside the grid,<br> their skeptisem and calculte the number of people who heard the rumor in each generation.
<br>
state.py - Document that represents automat's states
<br>
style.py - Document that represents a color palette for easy access to pre-defined colors.
<br>
main.py - main function.
