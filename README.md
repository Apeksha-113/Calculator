from tkinter import *

from tkinter import colorchooser
root=Tk()
root.title("Simple Calculator")
e=Entry(root, width=50, borderwidth=5)
e.grid(row=0,column=0,columnspan=3,padx=10,pady=40)

def button_click(number):
    #e.delete(0,END)
    current=e.get()
    e.delete(0,END)
    e.insert(0,str(current) + str(number))

def button_clear():
    e.delete(0,END)

def button_add():
    first_number= e.get()
    global f_num
    global math
    math="addition"
    f_num=int(first_number)
    e.delete(0,END)
    #return

def button_sub():
    first_number=e.get()
    global f_num
    global math
    math="subtraction"
    f_num=int(first_number)
    e.delete(0,END )

def button_mul():
    first_number=e.get()
    global f_num
    global math
    math="multiplication"
    f_num=int(first_number)
    e.delete(0,END)

def button_div():
    first_number=e.get()
    global f_num
    global math
    math="division"
    f_num=int(first_number)
    e.delete(0,END)

def button_equal():
    second_number= e.get()
    e.delete(0,END)

    if math=="addition":
        e.insert(0,f_num+int(second_number))

    if math=="subtraction":
        e.insert(0,f_num-int(second_number))

    if math=="multiplication" :
        e.insert(0,f_num*int(second_number))

    if math=="division":
        e.insert(0,f_num/int(second_number))

#def color():
   # my_color=colorchooser.askcolor()
    #my_label=Label(root,text=my_color).grid()

#my_button=Button(root,text="pick a color", command=color).grid()
button1=Button(root,text="1",padx=20, pady=20,command=lambda: button_click(1) ,fg="blue",bg="yellow")
button2=Button(root,text="2",padx=20, pady=20,command=lambda: button_click(2),fg="blue",bg="yellow")
button3=Button(root,text="3",padx=20, pady=20,command=lambda: button_click(3),fg="blue",bg="yellow")
button4=Button(root,text="4",padx=20, pady=20,command=lambda: button_click(4),fg="blue",bg="yellow")
button5=Button(root,text="5",padx=20, pady=20,command=lambda: button_click(5),fg="blue",bg="yellow")
button6=Button(root,text="6",padx=20, pady=20,command=lambda: button_click(6),fg="blue",bg="yellow")
button7=Button(root,text="7",padx=20, pady=20,command=lambda: button_click(7),fg="blue",bg="yellow")
button8=Button(root,text="8",padx=20, pady=20,command=lambda: button_click(8),fg="blue",bg="yellow")
button9=Button(root,text="9",padx=20, pady=20,command=lambda: button_click(9),fg="blue",bg="yellow")
button0=Button(root,text="0",padx=20, pady=20,command=lambda: button_click(0),fg="blue",bg="yellow")

button_ad=Button(root,text="+",padx=25,pady=21,command=button_add,fg="blue",bg="yellow")
button_subtract=Button(root,text="-",padx=25,pady=21,command=button_sub,fg="blue",bg="yellow")
button_multiply=Button(root,text="*",padx=25,pady=55,command=button_mul,fg="blue",bg="yellow")
button_divide=Button(root,text="/",padx=25,pady=21,command=button_div,fg="blue",bg="yellow")
button_equal=Button(root,text="=",padx=25,pady=55,command=button_equal,fg="blue",bg="yellow")
button_clear=Button(root,text="clear",padx=20,pady=20,command=button_clear,fg="blue",bg="yellow")


button1.grid(row=3,column=0)
button2.grid(row=3,column=1)
button3.grid(row=3,column=2)

button4.grid(row=2,column=0)
button5.grid(row=2,column=1)
button6.grid(row=2,column=2)

button7.grid(row=1,column=0)
button8.grid(row=1,column=1)
button9.grid(row=1,column=2)

button0.grid(row=4,column=0)

button_ad.grid(row=5,column=0)
button_subtract.grid(row=6,column=0)
button_multiply.grid(row=4,column=1,rowspan=2)
button_divide.grid(row=6,column=1)

button_equal.grid(row=5,column=2,rowspan=2)
button_clear.grid(row=4,column=2,columnspan=2)



root.mainloop()
