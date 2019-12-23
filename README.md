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
