# Mii Default Moment Checker
Hello! Do you want to improve at Mii-making? One of the first things you can do is play with all the different sliders in order to make unique characters. All too often, people barely use the sliders, resulting in very similar-looking and boring designs. Those of us in the Miitopia Discord server have affectionately referred to these kinds of designs as "Default Moments." This here is a program I have written that will tell you whether or not a mii is a "Default Moment."  

By Lewinham
_________________________________________
# What You Need & How to Use:
### 1. You need to download Python 3 and an IDE (PyCharm, Google Colaboratory, etc.)
### 2. Copy and paste the code below exactly as it is into the IDE.
### 3. Run the program and input the slider values for your mii.
###### The default position of any slider corresponds to a value of 0. 
###### The number of ticks away from the default position of the slider is the value you will input.
### 4. The program will return a Default Moment Index and tell you whether or not your mii is a "Default Moment."
###### An index of 0 corresponds to the default male/female mii.
###### The higher the index, the less of a default moment your mii is.
_________________________________________
# Program Code:
###### Code by Lewinham
###### Written in Python 3
###### Version 1.0
```
mii_slider_data = []
print("Welcome to my mii Default-Moment checker!\nFor each question if applicable, type the number of ticks the slider is from its default setting.\nIf the default slider setting is used, type '0'.")

print("___________________\nEyebrow Sliders\n___________________")
print("How many ticks are the eyebrows above/below the default position?")
eyebrow_vertical = input("Enter a non-negative number.\nIf the mii has no eyebrows, type N/A: ")
if eyebrow_vertical.isnumeric():
    mii_slider_data.append(2.1*float(eyebrow_vertical))

    print("How many ticks to either side are the eyebrows from the default position?")
    eyebrow_horizontal = input("Enter a non-negative number: ")
    try:
        mii_slider_data.append(1.7*float(eyebrow_horizontal))
    except ValueError as invalid0:
        print("Error\nNot a valid input\n________________")

    print("How many ticks from the default orientation are the eyebrows rotated?")
    eyebrow_rotation = input("Enter a non-negative number: ")
    try:
        mii_slider_data.append(1.75*float(eyebrow_rotation))
    except ValueError as invalid1:
        print("Error\nNot a valid input\n________________")

    print("How many ticks from the default size are the eyebrows?")
    eyebrow_size = input("Enter a non-negative number: ")
    try:
        mii_slider_data.append(1.75*float(eyebrow_size))
    except ValueError as invalid2:
        print("Error\nNot a valid input\n________________")

    print("How many ticks in either direction are the eyebrows squished?")
    eyebrow_squish = input("Enter a non-negative number.\nIf the mii was made on a Wii, type N/A: ")
    if eyebrow_squish.isnumeric():
        mii_slider_data.append(1.75*float(eyebrow_squish))
    else:
        print("This slider is non-applicable.")
else:
    print("Mii does not have eyebrows.")

mii_eye_data = []
print("___________________\nEye Sliders\n___________________")
mii_eye_type = input("Does the mii use the default eyes?\nType 'a' if yes.\nType 'b' if no.\n")
if mii_eye_type == "a":
    mii_eye_default = True
else:
    mii_eye_default = False

print("How many ticks are the eyes above/below the default position?")
eye_vertical = input("Enter a non-negative number: ")
try:
    mii_slider_data.append(2.5*float(eye_vertical))
    mii_eye_data.append(2.5*float(eye_vertical))
except ValueError as invalid3:
    print("Error\nNot a valid input\n________________")

print("How many ticks are the eyes to either side of the default position?")
eye_horizontal = input("Enter a non-negative number: ")
try:
    mii_slider_data.append(2.75*float(eye_horizontal))
    mii_eye_data.append(2.75*float(eye_horizontal))
except ValueError as invalid4:
    print("Error\nNot a valid input\n________________")

print("How many ticks are the eyes rotated from the default orientation?")
eye_rotation = input("Enter a non-negative number: ")
try:
    mii_slider_data.append(1.75*float(eye_rotation))
    mii_eye_data.append(1.75*float(eye_rotation))
except ValueError as invalid5:
    print("Error\nNot a valid input\n________________")

print("How many ticks are the eyes bigger/smaller than the default size?")
eye_size = input("Enter a non-negative number: ")
try:
    mii_slider_data.append(2.5*float(eye_size))
    mii_eye_data.append(2.5*float(eye_size))
except ValueError as invalid6:
    print("Error\nNot a valid input\n________________")

print("How many ticks in either direction are the eyes squished?")
eye_squish = input("Enter a non-negative number.\nIf the mii was made on the Wii, type N/A: ")
if eye_squish.isnumeric():
    mii_slider_data.append(2*float(eye_squish))
    mii_eye_data.append(2*float(eye_squish))
else:
    print("This slider is non-applicable")

if mii_eye_default == True and sum(mii_eye_data)/len(mii_eye_data) <= 1:
    mii_slider_data.append(0)
    mii_slider_data.append(0)

print("___________________\nNose Sliders\n___________________")
print("How many ticks is the nose above/below the default position?")
nose_position = input("Enter a non-negative number: ")
try:
    mii_slider_data.append(2.75*float(nose_position))
except ValueError as invalid7:
    print("Error\nNot a valid input\n________________")

print("How many ticks is the nose bigger/smaller than the default size?")
nose_size = input("Enter a non-negative number: ")
try:
    mii_slider_data.append(2.6*float(nose_size))
except ValueError as invalid8:
    print("Error\nNot a valid input\n________________")

mii_mouth_data = []
print("___________________\nMouth Sliders\n___________________")
mouth_type = input("Does the mii use the default mouth?\nType 'a' if yes.\nType 'b' if no.\n")
if mouth_type == "a":
    mouth_default = True
else:
    mouth_default = False
print("How many ticks is the mouth above/below the default position?")
mouth_position = input("Enter a non-negative number: ")
try:
    mii_slider_data.append(2.3*float(mouth_position))
    mii_mouth_data.append(float(mouth_position))
except ValueError as invalid9:
    print("Error\nNot a valid input\n________________")

print("How many ticks is the mouth bigger/smaller than the default size?")
mouth_size = input("Enter a non-negative number: ")
try:
    mii_slider_data.append(2.1*float(mouth_size))
    mii_mouth_data.append(float(mouth_size))
except ValueError as invalid10:
    print("Error\nNot a valid input\n________________")

print("How many ticks in either direction is the mouth squished?")
mouth_squish = input("Enter a non-negative number. If the mii was made on the Wii, type N/A: ")
if mouth_squish.isnumeric():
    mii_slider_data.append(1.9*float(mouth_squish))
    mii_mouth_data.append(float(mouth_squish))
else:
    print("This slider is non-applicable")

if mouth_default == True and sum(mii_mouth_data)/len(mii_mouth_data) == 0:
    mii_slider_data.append(0)

print("___________________\nFacial Hair Sliders\n___________________")
print("How many ticks is the mustache above/below the default position?")
mustache_position = input("Enter a non-negative number. If the mii has no mustache, type N/A: ")
if mustache_position.isnumeric():
    mii_slider_data.append(float(mustache_position))

    print("How many ticks bigger/smaller is the mustache from the default size?")
    mustache_size = input("Enter a non-negative number: ")
    try:
        mii_slider_data.append(float(mustache_size))
    except ValueError as invalid11:
        print("Error\nNot a valid input\n________________")
else:
    print("Mii has no mustache.")

print("___________________\nGlasses Sliders\n___________________")
print("How many ticks are the glasses above/below the default position?")
glasses_position = input("Enter a non-negative number. If the mii does not wear glasses, type N/A: ")
if glasses_position.isnumeric():
    mii_slider_data.append(float(glasses_position))

    print("How many ticks bigger/smaller are the glasses from the default size?")
    glasses_size = input("Enter a non-negative number: ")
    try:
        mii_slider_data.append(float(glasses_size))
    except ValueError as invalid12:
        print("Error\nNot a valid input\n________________")
else:
    print("Mii does not wear glasses.")

default_index = sum(mii_slider_data)/len(mii_slider_data)
print("_________________________________\nDefault-Moment Index = " + str(default_index))
if default_index < 0.75:
    print("Default moment smh.")
else:
    print("Nice! Your mii is not a default moment!")
```
