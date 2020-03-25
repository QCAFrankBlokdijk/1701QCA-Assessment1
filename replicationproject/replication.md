# Assessment 1: Replication project

*Fill out the following workbook with information relevant to your project.*

*Markdown reference:* [https://guides.github.com/features/mastering-markdown/](http://guides.github.com/features/mastering-markdown/)

## Temperature Gauge: The Engaugening of Morse ##
The link to the original version of this project can be found here: https://www.hackster.io/anish78/how-to-create-temperature-gauge-using-micro-bit-a601cc

## Related projects ##

### Related project 1 ###
Temperature

https://makecode.microbit.org/reference/input/temperature

![Image](RP1.png)

This project is related to mine because it shows directly how the temperature function in the Micro Bit works.

### Related project 2 ###
Max-min thermometer

https://microbit.org/projects/make-it-code-it/max-min-thermometer/

![Image](RP2.png)

This project is related to mine because it shows how to use the temperature feature in practical and useful ways + reinforces the uyse of temperature based variables.

### Related project 3 ###
Indoor Outdoor Thermometer

https://microbit.org/projects/make-it-code-it/indoor-outdoor-thermometer/

![Image](RP3.png)

This project is related to mine because it uses one microbit to show multiple variables in different ways.

### Related project 4 ###
Micro Morse Phone

https://make.techwillsaveus.com/microbit/activities/micro-morse-phone

![Image](RP4.png)

This project is related to mine because it gave me the overall idea for my project with micro bit + morse code.

### Related project 5 ###
Morse Code (On Screen)

https://makecode.microbit.org/courses/csintro/radio/activity

![Image](RP5.png)

This project is related to mine because it showed how to show morse code on the screen of the micro bit - which I was using at the start of the process to prototype my idea.

### Related project 6 ###
Morse Code Beacon

https://microbit.hackster.io/snap-bit/snap-bit-morse-code-beacon-25fec3

![Image](RP6.png)

This project is related to mine because it shows how to translate morse code into a light pattern with the Micro Bit.

## Reading reflections ##
*Reflective reading is an important part of actually making your reading worthwhile. Don't just read the words to understand what they say: read to see how the ideas in the text fit with and potentially change your existing knowledge and maybe even conceptual frameworks. We assume you can basically figure out what the readings mean, but the more important process is to understand how that changes what you think, particularly in the context of your project.*

*For each of the assigned readings, answer the questions below.*

### Reading: Don Norman, The Design of Everyday Things, Chapter 1 (The Psychopathology of Everyday Things) ###

*What I thought before: Describe something that you thought or believed before you read the source that was challenged by the reading.*

*What I learned: Describe what you now know or believe as a result of the reading. Don't just describe the reading: write about what changed in YOUR knowledge.*

*What I would like to know more about: Describe or write a question about something that you would be interested in knowing more about.*

*How this relates to the project I am working on: Describe the connection between the ideas in the reading and one of your current projects or how ideas in the reading could be used to improve your project.*

### Reading: Chapter 1 of Dan Saffer, Microinteractions: Designing with Details, Chapter 1 ###

*What I thought before: Describe something that you thought or believed before you read the source that was challenged by the reading.*

*What I learned: Describe what you now know or believe as a result of the reading. Don't just describe the reading: write about what changed in YOUR knowledge.*

*What I would like to know more about: Describe or write a question about something that you would be interested in knowing more about.*

*How this relates to the project I am working on: Describe the connection between the ideas in the reading and one of your current projects or how ideas in the reading could be used to improve your project.*

### Reading: Scott Sullivan, Prototyping Interactive Objects ###

*What I thought before: Describe something that you thought or believed before you read the source that was challenged by the reading.*

*What I learned: Describe what you now know or believe as a result of the reading. Don't just describe the reading: write about what changed in YOUR knowledge.*

*What I would like to know more about: Describe or write a question about something that you would be interested in knowing more about.*

*How this relates to the project I am working on: Describe the connection between the ideas in the reading and one of your current projects or how ideas in the reading could be used to improve your project.*


## Interaction flowchart ##


![Image](flowchart.png)

## Process documentation

Starting with the general idea, I knew that I wanted to have the temperature display on the screen. I tested how this would work first by making it appear on the screen of my microbit in the simulator like this: 

![Image](PD1.png)

This was now displaying the temperature of the microbit on the simulator, I imported this code onto the physical microbit by pairing it to my device and having them connected. Through testing I found that the micro bits temperature never went below 28 degrees, and higher than 35. This gave me my baseline for the temperatures I would be using for the remainder of the project.

I then continued with the project, following the tutorial on microbit, I managed to have the microbit display the temperature on the display abnd (instead of using a servo motor to turn a gauge, as I lacked these materials) I had it turn on a green light when it was below 30 degrees, a yellow light when it was above 30 but below 34 + a fan, and a red light + the fan continues when its over 35. Unfortunately the code for this was lost, however, photos and videos of the project can be found below:

![Image](PD4.jpeg)

Video of it working: https://photos.app.goo.gl/e9KHD2anZB9oBSSZ6

This is the point where I wanted to start making the project my own. I felt I had a solid understanding of the code + microbit as well as how the microbits temperature gauge worked. So I set out to make my own temperature gauge project.

My immediate plan was to have the microbit display the temperature in an impractical manner, mostly because I think it would be a challenge + make for an interesting final product. This is how I settled on showing the temperature in morse code. I had the lights + the coding knowledge to pull it off, so I set right off!

Now I started writing the code - I found that I could do it one of two ways. The short way or the long way. The short way looked like this (this is the code from related project 6 that I brought across): 

![Image](PD2.png)

While this works - I wanted to have more individual control over the pauses between the dots and lines that the code produces. So I ended up making my own (much longer) version. Which looks like this:

![Image](PD3.png)

This code is so long that I can't fit even half of it into the screenshot. The reason I made the code this way, is that if something goes wrong I can change every minor detail, rather than trying to fix an overlying issue. I made sure to write all the pins to P0 (as this is where my light will go) and found the 500 ms gaps makes effective dots, and a 1000 ms gap makes good lines. There is also a 2000 ms gap between the two numbers. Once the two numbers are displayed in morse, a 3000 ms gap is placed to breakup the timing and allows the viewer to mentally 'reset'. For an idea of how long this code is, here is the code fully zoomed out, in multiple screenshots:


![Image](PD5.png)

![Image](PD6.png)

![Image](PD7.png)

![Image](PD8.png)

I also added a failsafe to check the temperature is working correctly, by pressing any of the two buttons on the microbit, the microbit itself shows the temperature on the screen. As well as this, in the code I added an on start check that makes sure the light is turned off. This is to ensure no false readings. The main section of this code can be found below:

![Image](PD9.png)


## Project outcome ##

*Complete the following information.*

### Project title ###

### Project description ###

*In a few sentences, describe what the project is and does, who it is for, and a typical use case.*

### Showcase image ###

*Try to capture the image as if it were in a portfolio, sales material, or project proposal. The project isn't likely to be something that finished, but practice making images that capture the project in that style.*

![Image](missingimage.png)

### Additional view ###

*Provide some other image that gives a viewer a different perspective on the project such as more about how it functions, the project in use, or something else.*

![Image](missingimage.png)

### Reflection ###

*Describe the parts of your project you felt were most successful and the parts that could have done with improvement, whether in terms of outcome, process, or understanding.*


*What techniques, approaches, skills, or information did you find useful from other sources (such as the related projects you identified earlier)?*


*What ideas have you read, heard, or seen that informed your thinking on this project? (Provide references.)*


*What might be an interesting extension of this project? In what other contexts might this project be used?*
