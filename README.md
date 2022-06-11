# Mii Default Moment Checker
Hello! Do you want to improve at Mii-making? One of the first things you can do is play with all the different sliders in order to make unique characters. All too often, people barely use the sliders, resulting in very similar-looking and boring designs. Those of us in the Miitopia Discord server have affectionately referred to these kinds of designs as "Default Moments." This here is a program I have written that will tell you whether or not a mii is a "Default Moment."  
_________________________________________
# What You Need & How to Use:
### 1. You need to download the executable file, Mii_default_checker.exe.
### 2. Run the executable file and input the slider values for your mii.
###### The default position of any slider corresponds to a value of 0. 
###### The number of ticks away from the default position of the slider is the value you will input.
### 3. The program will return a Default Moment Index and tell you whether or not your mii is a "Default Moment."
###### An index of 0 corresponds to the default male/female mii.
###### The higher the index, the less of a default moment your mii is.
_________________________________________
# How the Program Works:
###### Code by Lewinham
###### Written in Python 3
###### Version 1.0
The program works by taking a weighted average of all of the inputs. The weights were determined based on the relative importance of each slider in preventing miis from having the "default" aesthetic.
#### Special thanks to BH for helping with determining weights for the different sliders.
