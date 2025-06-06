from tkinter import *
from tkinter.ttk import *
from ttkthemes import ThemedTk
import random

screen = ThemedTk(theme="equilux")
screen.configure(themebg="black")

screen.geometry('600x450')
screen.title('currency stuf')
screen.resizable(height=False, width=False)

check = BooleanVar()



choice = IntVar()

b1 = Radiobutton(screen, text="easy",value=1,variable=choice)
b2 = Radiobutton(screen, text="mid",value=2,variable=choice)
b3 = Radiobutton(screen, text="hard",value=3,variable=choice)

a = -1
imj = 0

def roll():
    global a,ent
    ent.delete(0,END)
    x = choice.get()

    if x == 1:
        a = random.randint(1, 100)

    elif x == 2:
        a=random.randint(1, 220)

    elif x == 3:

        a=random.randint(1, 500)




def kwuess(event):

    global a,img,tries

    e = int(ent.get())
    if e == a:
        img = Label(screen, image=corect)
        print("yes")
        tries += 1
        tr.configure(text=tries)
    elif e<a :
        img = Label(screen, image=up)
        print("up")
        tries += 1
        tr.configure(text=tries)
    elif e>a :
        img = Label(screen, image=down)
        print("down")
        tries += 1
        tr.configure(text=tries)

    img.grid(row=2, column=3)


def sxit():
    screen.destroy()

corect = PhotoImage(file="correct.png")
up = PhotoImage(file="uparrow.png")
down = PhotoImage(file="downarrow.png")
dise = PhotoImage(file="dice.png")
img = Label(screen,image=dise)
rol= Button(text="Roll",command=roll)
resolt=Label(screen)
exot=Button(text="EXIT",command=sxit)

ent = Entry(screen)
tr = Label(text=0)
tries = 0

b1.grid(row=0,column=0)
b2.grid(row=0,column=1)
b3.grid(row=0,column=2)


rol.grid(row=2,column=2)
exot.grid(row=3,column=2)
ent.grid(row=3,column=1)
img.grid(row=2, column=3)
tr.grid()

screen.bind('<Return>', kwuess)

screen.mainloop()
