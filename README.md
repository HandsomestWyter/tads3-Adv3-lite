# TADS 3.1 - ADV3 Lite Library Condensed Notes
Condensed notation on the TADS 3 library, Adv3lite


## Chapter 1 (In Progress)
There is nothing to see here just yet

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
