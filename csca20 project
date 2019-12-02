#You will need to install both tkintker and pillow in your own computer
#You will have to put every single image in the same folder as where you store the code
'''Welcome to the hottest actor code!'''

'''For this code we will be using the PIL library and Tkinter to isplay images in a new window.'''

#importing Tkinter and PIL library.

import tkinter
from PIL import ImageTk, Image

#defining the window big enough to display images after.

master = tkinter.Tk()
master.geometry('1000x1000')
master.configure(bg = 'azure')

#welcome page with text introducing to the game

label_welcome_text = 'Welcome to the hottest actor game'
label_welcome = tkinter.Label (master, text = 'Welcome to the hottest actor game', bg ='light blue', fg='white')
label_welcome.place(x=80, y=400)
label_welcome.config(font=('Courier', 44))

#function thats open every images under tkinter so we can use them in the windows.

image_filenames = ['Brad_Pitt.jpg', 'Tom_Cruise.jpg', 'Justin_Bieber.jpg', 'George_Clooney.jpg', 'Al_Pacino.jpg', 'Bradley_Cooper.jpg', 'Chris_Hemsworth.jpg', 'Daniel_Radcliffe.jpg', 'Dev_Patel.jpg', 'James_Dean.jpg', 'Jamie_Fox.jpg', 'John_Travolta.jpg', 'Johnny_Depp.jpg', 'Kit_Harrington.jpg', 'Leonardo_Dicaprio.jpg', 'Omar_Sy.jpg', 'Ryan_Gosling.jpg', 'Ryan_Reynolds.jpg', 'Stephen_Chow.jpg', 'White.jpg']

images = []
for item in image_filenames:
    images.append(ImageTk.PhotoImage(Image.open(item)))

#Setting the indexes that we are going to use to count which images from the list is already passed.

index = 0
index_left = 0
index_right = 1

#Index function, that set up the general index to the sum of both index so we can have the total number of pictures already past in the list.

def index_function(): 
    index = max(index_left, index_right) + 1

#When we click on the left button the left_choice function is runned. This function set the left image to our TOP1 actor. The picture on the right is changed by the next picture in the list. This function call the index function to change the value of the index for next picture.

def left_choice():
    
    global index_left
    global index_right

    b2 = tkinter.Button(master,image=images[max(index_left, index_right) + 1], text="This one!", command = right_choice, height=600, width=400)
    b2.place(x = 500, y = 20)
    index_right = max(index_left, index_right) + 1
    index_function()

#When we click on the right button the right_choice function is runned. This function set the right image to our TOP1 actor. The picture on the left is changed by the next picture in the list. This function call the index function to change the value of the index for next picture.

def right_choice():
    
    global index_left
    global index_right

    b1 = tkinter.Button(master,image=images[max(index_left, index_right) + 1], text="This one!", command = left_choice, height=600, width=400)
    b1.place(x = 20, y = 20)
    index_left = max(index_left, index_right) + 1
    index_function()

#the main function destroy the welcome page and initialize the first 2 buttons and set up the end game button if the user is willing to quit the game he can do it at any moment. 

def main_function():
    b_start.destroy ()
    label_welcome.destroy()
    
    b1 = tkinter.Button(master,image=images[index_left], text="This one!", command = left_choice, height=600, width=400)
    b1.place(x = 20, y = 20)
    
    b2 = tkinter.Button(master,image=images[index_right], text="This one!", command = right_choice, height=600, width=400)
    b2.place(x = 500, y = 20)
    
    b_end = tkinter.Button(text= 'End the game', command = master.destroy)
    b_end.place (x = 400, y = 650)

#master destroy is the button click to exit the window called by the end function

#end function is called when the user wants to quit the game. It will destroy both image buttons to show him his TOP1. A button to quit the game is displayed.

    


#this is how the game begins thanks to the button start on the welcome page which is gonna call the main_function.

b_start = tkinter.Button(master, text= 'START!', command = main_function)
b_start.place (x=80, y=500)

#run the window

master.mainloop()   
