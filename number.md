

```
import tkinter
from tkinter import messagebox
import random

shuzi = tkinter.Tk()                    
shuzi.title('猜数字游戏')               
shuzi.geometry('400x300')               
number = random.randint(1,100)

label1 = tkinter.Label(shuzi,fg='black',text="猜数字小游戏",font=('楷体',35,'bold'))      
label1.grid(padx=75)                                    #

label2 = tkinter.Label(shuzi,fg='black',text="游戏规则：\n从1到100中猜数字！！！",font=('楷体',15,'bold'))    
label2.grid(padx=10,pady=10)

label3 = tkinter.Label(shuzi,fg='black',text="请输入你所猜测的数字：",font=('楷体',15,'bold'))
label3.grid(padx=10,pady=10)

text = tkinter.Entry(shuzi,width=30)
text.grid(padx=100)

def compare():
    use = int(text.get())
    if use == '':
        tkinter.messagebox.showerror('警告','输入不能让为空！！！')

    elif use > number:
        tkinter.messagebox.showinfo('不正确', '大，大了！加油！')

    elif use < number:
        tkinter.messagebox.showinfo('不正确', '小，小了！不错呦！')

    elif use == number:
        tkinter.messagebox.showinfo('正确')

    else :
        tkinter.messagebox.showerror('警告', '输入不正确！！！')


button1 = tkinter.Button(shuzi, text='确定',command=compare, width=10, font=('微软雅黑', 10,))          
button1.grid(padx=10,pady=10)

button2 = tkinter.Button(shuzi, text='退出游戏',command=shuzi.quit, width=10, bg='yellow', font=('微软雅黑', 10,))
button2.grid(padx=10,pady=10)

shuzi.mainloop()

```
