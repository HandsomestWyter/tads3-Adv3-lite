# TADS 3.1 - ADV3 Lite Library Condensed Notes
Condensed notation on the TADS 3 library, Adv3lite. If you want, just got check out the Wiki for a much more organized version of this file. If you want a more organized version of this documentation, I suggest that you check out the [wiki](https://github.com/reneorionsalmon/tads3-Adv3-lite/wiki) for this project in the mean time. I will be working to condense this into a PDF for your use, so please be patient! 

## Chapter 1 - The Basics
### 1.1 What is Interactive Fiction and TADS?
So, according to [Wikipedia - Interactive Fiction](https://en.wikipedia.org/wiki/Interactive_fiction), Interactive Fiction or IF, is essentially "software simulating environments in which the player uses text commands to control characters and influence the environment. Now why would you want to write IF? Well, the short answer is that if you want to have your own DnD sessions with yourself, then picking up IF is the way to go. However, after a while, you kinda might want to start writing your own IF, which is what this tutorial series is about. Of course, I didn't write the book on TADS 3, but I'm making a video tutorial series (mainly for my own benefit, if I'm being honest with you) because there isn't youtube videos on the subject, and TADS 3 is honestly a really powerful program for developing IF. Of course, you have other programs like [Quest](http://textadventures.co.uk/quest/desktop) , [Twine 2](https://twinery.org/) and many others, but what I really like about TADS 3 is the fact that you can export your project to an excecutable file.

### 1.2 Installing TADS 3.1
Installing TADS 3 is pretty straight forth. Just go to the [TADS Website](http://www.tads.org/) and download the program and install as you normally would any other program.

### 1.3 Installing Adv3-Lite Library
1. This one is a little more complicated. Once TADS 3.1 is installed, go to [Eric Eve's Adv 3 Lite Library](https://github.com/EricEve/adv3lite) on github, and download the master file. 
2. In your "Documents" folder on your computer, there is a folder that should be called "TADS 3". In that folder, if one is not created, create a file called "Extenstions".
3. Export the "adv3lite-master.zip" file into this folder.
4. Now, open up TADS 3 and make a quick file. It doesn't matter what you use, becuase we're going to make another file after this.
5. Under the "Tools" tab, select the "Options" options. This will bring up the "Workbench Options" dialog box.
6. Scroll down, and under the "System" section, click on the "Extensions".
7. Click on "Browse..." and navigate to "Docments\TADS 3\Extensions", and select that file.
8. Restart TADS 3 and now make a new project, select a folder where you want to work from, select that "Adv 3 Lite", which now should be available to you, and create your new project, filling out the nessecery information as needed.

Now that you installed the Adv 3 Lite library, you can now move unto the next chapter of these notes.

## Chapter 2 - Map Making - Rooms
### 2.1 Rooms
#### 2.1.1 Your Very first room!
No game can take place without a room! Here's how to make a quick room

![pic](https://github.com/reneorionsalmon/tads3lite/blob/master/pics/2.1.1%20-%20your%20very%20first%20room.PNG "Your Very First Room")

In the code above, we define two properties to our object: 'roomTitle' (this sets the title for the object that we've just declared) and 'desc' (the description of the room). These are properties that we'ved assigned to this 'Room' object that we called 'bedroom'. The majority of TADS programming is based off defining objects and their properties.

#### 2.1.2 Room Template
The above mentioned properties are so common that we can use a template. Symbols for shorthand coding are '+' or '@' or '->' to tidenfity parts of the template. The Room template is very straightforth. Here's an example of what our 'bedroom' object will look like formated to this 

![pick](https://github.com/reneorionsalmon/tads3lite/blob/master/pics/2.1.2%20-%20room%20template.PNG "Room Template")

#### 2.1.3 Direction and Your Second Room
As we mentioned above, there is a way out towards the east in the 'bedroom' object, following the guide, we can make a 'landing' of some sort. 

![pick](https://github.com/reneorionsalmon/tads3lite/blob/master/pics/2.1.3%20-%20your%20very%20second%20room.PNG "Second Room Code")

Notice that we added a "direction" property to our 'landing' object. There are several acceptable directions.
##### 8 Compass Directions
* North	
* South
* East
* West
* Northwest
* Northeast
* Southwest
* Southeast

##### 4 Special Directions
* Up
* Down
* In
* Out

##### 4 Shipboard Directions
* Starboard
* Port
* Fore
* Aft

Now that we know mentioned that there is a direction coming out of the bedroom and into the landing, let’s go back to the ‘bedroom’ object and set the ‘east’ direction variable to ‘landing’, so that there is a connection between the two objects.

![pic](https://github.com/reneorionsalmon/tads3lite/blob/master/pics/2.1.3%20-%20your%20very%20second%20room%202.PNG "Updated Code")

#### 2.1.4 Excercise 1
Try to recreate your home or workplace for practice on developing your maps! If you're feeling adventerous, you can totally make something that's totally original and creative!

#### 2.1.5 – Source Code
This is what your source code in your TADS3 file should look like as of right now.
![pic](https://github.com/reneorionsalmon/tads3lite/blob/master/pics/2.1%20-%20source%20code.PNG "2.1 Source Code")

### 2.2 – Coding Excursus 1: Defining Objects

#### 2.2.1 – Object Definition

Here’s the overall look of what a typical object in TADS3 will look like:
![pic](https://github.com/reneorionsalmon/tads3lite/blob/master/pics/2.2%20-%20object%20definition.PNG "object definition")

Notice ‘objectName’ is simply the name of the object. We use this to identify it in throughout our code. The ‘ClassList’ is where our classes go. Classes essentially define the type of object and assign it certain behaviors and properties. Each class has it’s own properties, in this case, the class ‘Room’ has two properties that are called ‘name’ and ‘desc’ (short for description). Notice for the basic type of object, we also end it with a semicolon ‘;’. This is to tell TADS3 that we are ending the object declaration. Of course, objects and classes can contain methods, but we’ll talk about that later.

#### 2.2.2 – An Alternative Way of Writing an Object

Of course, with TADS3 flexibility you are given another way to write your code. You can also encase your properties with a pair of open and closed curly brackets, i.e. “{}”. Here’s an example of that. 

![pic](https://github.com/reneorionsalmon/tads3lite/blob/master/pics/2.2.2%20alternative%20way.PNG "Alternative Object Declaration")

#### 2.2.3 – Locating Templates
You can find templates for certain classes in the Adv3Lite Library Reference Manuel. Try to open it in a web browser. When you start the Reference Manuel, this should appear at the top, click on the templates link and it should take you a list titled Templates. 

![pic](https://github.com/reneorionsalmon/tads3lite/blob/master/pics/2.2.3%20-%20room%20template%20links.PNG "Links")

Scroll down until you find the ‘Room’ link, click on it, and it should take you to the Room Template.

![pic](https://github.com/reneorionsalmon/tads3lite/blob/master/pics/2.2.3%20-%20room%20template.PNG "Template")

Notice that there are question marks. This means that anything that is defined after the ‘roomTitle’, ‘vocab’, and “desc” is an option park of the template.  

![pic](https://github.com/reneorionsalmon/tads3lite/blob/master/pics/2.2.3%20-%20room%20template%202.PNG "Template Excecution")

#### 2.2.4 – Single and Double Quote Differentials

You may have noticed that there some of the strings (list of text). The ‘roomTitle’ will always be surrounded by single quotes because this type of string is used for displaying brief text, along with the ‘vocab’ declaration as well, whereas the double quotes are reserved for text that text to have a lot of text, more than two or more sentences. Essentially, strings in single quotes will be associated with properties and the double quotes will surround descriptions.
