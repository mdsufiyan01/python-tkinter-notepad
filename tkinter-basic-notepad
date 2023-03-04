#imports the libraries
from tkinter import *
from tkinter import filedialog



# function for save button
def save():
    fileh=open("file.txt",'a+')
    a=data.get("1.0","end-1c")
    fileh.write(a+'\n')
    fileh.close()
    
#  function for exit
def exit1():
    win.destroy()
    
# function for saving file
def newf():
    file5=filedialog.askopenfile(mode='r')  # filedialog function from tkinter lib
    if file5 is not None:
        values4=file5.read()
        data.insert(0.0,values4)
    else:
       print(" please close")
        
    
    
    
#opening up new file

fileh=open("file.txt",'w')
fileh.close()

# tk basic window syntex    
win = Tk()
win.title("NOTEPAD ")
mla=Label(win,text="NOTEPAD ",font=("Algerian",15))
mla.pack()
databox = Frame(win)

# scrollbar
scroll = Scrollbar(databox)
scroll.pack(side=RIGHT, fill=Y)
data =  Text(databox, width=50, height=20, yscrollcommand = scroll.set)
data.pack()
scroll.config(command=data.yview)
databox.pack()

# buttons (save and exit)
button1=Button(databox, text="SAVE ",font=("Algerian",14),command=save)
button1.pack(padx=5,pady=5,side=LEFT)
button2=Button(databox, text="Exit",font=("Algerian",14),command=exit1)
button2.pack(padx=5,pady=5,side=RIGHT)

# labels 
label=Label(win,text="Please ensure save before exit ",fg="red",font=("times",17))
label.pack

# open button
button3=Button(databox, text="open",font=("Algerian",14),command=newf)
button3.pack(padx=5,pady=5)


win.mainloop


