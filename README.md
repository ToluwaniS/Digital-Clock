# Digital-Clock
#(tkinter)

import time
from tkinter import *

window = Tk()
window.title("DIGITAL CLOCK")
window.geometry = ("400x300")
window.resizable(0,0)
label = Label(window, font =("Arial",70,'bold'), bg = "brown",fg = "white", bd = 50)
label.grid(row =0, column=1)

def digitalclock():
   text_input = time.strftime("%H:%M:%S")
   label.config(text=text_input)
   label.after(200, digitalclock)

digitalclock()
window.mainloop()




