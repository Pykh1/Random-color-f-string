# Random-color-f-string
3 methodes to generate random colors usinf F string 

METHOD 1:
   color_code="#"
    for i in range(0,6):
        color_code=f'#{randint(0,0xffffff):06x}'
    return color_code
my_window=Tk()
my_canvas=Canvas(my_window,width=400,height=400,background="white")
my_canvas.grid(row=0,column=0)
for i in range(0,100):
    x1=randint(0,400)
    y1=randint(0,400)
    x2=randint(0,400)
    y2=randint(0,400)
    random_width=randint(1,30)
    my_canvas.create_line(x1,y1,x2,y2,fill=random_color_code(),width=random_width)
    my_canvas.update()
my_window.mainloop()

METHOD2:
from random import*
from tkinter import*
def random_color_code():
    hex_chars=["0","1","2","3","4","5","6","7","8","9","a","b","c","d","e","f"]
    color_code="#"
    for i in range(0,6):
        return f'#{randint(0,0xffffff):06x}'

my_window=Tk()
my_canvas=Canvas(my_window,width=400,height=400,background="white")
my_canvas.grid(row=0,column=0)
for i in range(0,100):
    x1=randint(0,400)
    y1=randint(0,400)
    x2=randint(0,400)
    y2=randint(0,400)
    random_width=randint(1,30)
    my_canvas.create_line(x1,y1,x2,y2,fill=random_color_code(),width=random_width)
    my_canvas.update()
my_window.mainloop()

METHOD3:
from random import*
from tkinter import*
my_window=Tk()
my_canvas=Canvas(my_window,width=400,height=400,background="white")
my_canvas.grid(row=0,column=0)
for i in range(0,100):
    x1=randint(0,400)
    y1=randint(0,400)
    x2=randint(0,400)
    y2=randint(0,400)
    random_width=randint(1,30)
    my_canvas.create_line(x1,y1,x2,y2,fill=f'#{randint(0,0xffffff):06x}',width=random_width)
    my_canvas.update()
my_window.mainloop()

