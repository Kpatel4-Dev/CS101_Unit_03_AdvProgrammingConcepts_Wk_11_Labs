# Lab 05: GUI implementation

## Introduction

In this lab I have given you a function that you will probably need to use again in your programming career. The function is called binary(), it asks for the user to input a number and then it outputs the binary string of that number. Go ahead and click run to see how it works. 

## Directions

### Step 1

binary() is a pretty useful function and I know I will be using it again. But one thing has been bugging me...We are in the 2020's and programming languages have gotten a lot more advanced and accessible, so why have all of the programs that we have created so far look like they are from 1975? 

Our programs have only been interacting with the user through the console, which is often harder to read or understand when not accompanied with visuals, and it is a lot more boring to read! What we need is a more visual way to interact with our user, we can do this by implementing a **GUI** with **tkinter**. 

**I highly recommend you visit the [Tkinter documentation](https://tkdocs.com/tutorial/widgets.html)**
*Here you can find all of the widgets you can use, as well as what ways you can modify the widgets with their parameters.*

 **GUI** is short for graphical user interface and every serious application in modern times is using some sort of GUI. One way I like to think of a GUI is as if you are turning your program into an *APP*

 **tkinter** (The "t" is silent and it is pronounced "kinter") is the standard Python GUI library and one of the easiest tools we can use to make a basic GUI program. It includes many different utilities and objects (called *"widgets"*) for us to work with. We won't cover everything tkinter can do within this lab but we are hopefully going to give you a basic understanding of what is possible! Feel free to explore the documentation, watch youtube videos, and try out your own programs.

 **Widget** Can be a button, or a label, an entry, there are 15 built in widgets in Tkinter. They are built in to tkinter and are placed on windows.
---
### Step 2

**First, make sure to delete the binary() function call at the bottom of the program on line ~30**
*If you do not delete binary() on line ~30 you will receive an error later on saying your widgets are not found*

In the import section, we need to import **everything from tkinter**. The * after the import statement means we are going to use everything that is included in the package. 
   
  from tkinter import *

Once we have imported tkinter it is time to start our work of art. Much like art we need a *canvas* to work on. When we are using **tkinter** we must always start by creating our **root** window (You may think of it as a canvas that we are going to put things on). Every GUI requires **root.mainloop()** at the end of the program. Everything in between your creation of the root window and the end of the root.mainloop() will continue to run and receive commands until it is terminated in some way, much like a loop.

In the main section of your program create your root window and designate the end of the mainloop by typing: 
   
  root = Tk()
  # Everything you add must go here! Make sure root.mainloop() is on the bottom line of the program
  root.mainloop()

It is important to note that all of our code must to go in-between the two lines we just created. Now we can start putting things on our **root** window, we can start with something simple to test how everything looks so far. 
---
### Step 3 

We are going to be using two *widget*'s for this next step. The first widget we are going to use is called a **Label**. A **Label** acts exactly as it sounds, it is a section that displays text. It is typically used to display a result or interact with the user and is not typically used for input. And the next widget is called an **Entry**. An entry can also display text but it is primarily used to get input from the user to use in a function.

Let's start by creating one Label that displays "Enter your number:" and an Entry section next to it: 

label_1 = Label(root, text = "Enter your number: ")
entry_1 = Entry(root, width = 5)

These statements just create the widgets and tell them which window they will belong to, they are not placed anywhere yet. One thing you may notice is the parameters are not empty. the *root* portion just means that this widget is going to go on our root window. In the parameters we can do a bunch of things, like in our label_1 we set the text equal to the string we want it to display, and in our entry_1 we made the width of the input 5 spaces, neither are those statements are required, they can be changed to different values or omitted.

Next thing we need to do is tell tkinter where each widget will be placed, the best way to do this is by telling tkinter exactly which row and column we want our widget to be in.

Rows go in this direction:

0
1
2
3
Columns go in this direction:
0 1 2 3

Place the label and entry by calling our **widget** and using the **grid()** function and defining the row and column in the parameters. You can also determine how many columns each widget will span in the parameters here with "columnspan = number".

label_1.grid(row = 0, column = 0)
entry_1.grid(row = 0, column = 1)

The code above will place the label on the left and then the entry to the right of the label. We placed them on the same row but on different columns.
Click run to see your creation and make sure you have done everything correctly up to this step!
---
### Step 4

The program is looking great but it doesn't do anything yet! We need our program to perform the binary function and display the result and we need a button to tell our program to run the function. One thing we can do to make our GUI easier on the eyes is we can make the result yellow while it is waiting for a calculation:

   label_2 = Label(root, text = "Waiting", bg = "yellow")
   button_1 = Button(root, text = "Calculate", command = binary)

One thing that you must notice in the parameters of our Button is **command = binary**. This will tell our GUI to run binary() every time we click the button. **Make sure to NOT include the '()' in your function name within the button parameters, if you do the function will not work correctly.**
It is also a great practice to include text on the buttons as well as labels that are waiting for a result.

With your group place the button_1 and label_2 on your root window using the grid() function. One should go above the other if they are both spanning 2 columns. If you wanted them to be next to eachother then you should get rid of the columnspan in the parameters. An important part of creating GUI's is creating a layout that makes sense to the user, so please keep this in mind when placing your widgets.
---
### Step 5 

One last thing we must do is somehow get the inputs from the entry widgets so we can use it in our function. There are a couple ways to do this, one way is by assigning a variable to the widget in its parameters and then passing the value to the function. Another way that can be a lot easier to write is by simply using get() on the widget you want to receive the value from. We can then config(), which stands for configure, our label that we want to be the change with the answwer and update it to display the result. This may be confusing to understand at first so I am going to show you how you can rewrite the function:

  def binary():
 user_input = int(entry_1.get()) #retrieves input from user
 answer = bin(user_input)[2:] #converts to binary
 label_2.config(text = answer, bg = "light green") #updates the label and changes the color to green to visualize success
If you are curious what colors you can use then you can [click here](http://www.science.smith.edu/dftwiki/images/3/3d/TkInterColorCharts.png).
---
### Step 6

That is everything I can teach you, now it is your turn for you and your group to come up with another function! 

You will need to create another label to ask for user input, at least one entry area for your inputs. You will also need another label to display the answer, and another button! You can put everything on the existing root window. This is your time to get creative! You may use a function from an older homework or lab that you thought was interesting.

*If you need any help feel free to ask your teacher for tips!*
