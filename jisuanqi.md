

```python
import tkinter
tk = tkinter.Tk()
#设置窗口标题
tk.title("BMI计算器")
#设置窗口代销
tk.geometry("400x400")

Bmi1 = tkinter.StringVar()
Bmi2 = tkinter.StringVar()
#添加Label和Entry
#1、设置升高标签和输入框
#1-1身高标签
label_height = tkinter.Label(tk,text = "身高")
label_height.place(x = 10,y = 10,width = 80,height = 40)

#1-2身高输入框
entry_height = tkinter.Entry(tk,textvariable = tkinter.StringVar())
entry_height.place(x = 90,y = 10,width = 80,height = 40)

#1-3身高单位
label_m = tkinter.Label(tk,text = "m")
label_m.place(x = 170,y = 10,width = 40,height = 40)

#2、设置体重标签和输入框
#2-1体重标签
label_weight = tkinter.Label(tk,text = "体重")
label_weight.place(x = 10,y = 60,width = 80,height = 40)

#2-2体重输入框
entry_weight = tkinter.Entry(tk,textvariable = tkinter.StringVar())
entry_weight.place(x = 90,y = 60,width = 80,height = 40)
#2-3体重单位kg
label_kg = tkinter.Label(tk,text = "kg")
label_kg.place(x = 170,y = 60,width = 40,height = 40)
#添加计算按钮Button
def bmi():
    bmi_set = round(float(entry_weight.get())/(float(entry_height.get())*float(entry_height.get())),2)
    if bmi_set < 18.5:
        result = ("您的BMI为：",bmi_set)
        abc = ("偏瘦")
    elif 18.5 <= bmi_set <= 24:
        result = ("您的BMI为：",bmi_set)
        abc = ("正常")
    elif 24 <= bmi_set <= 30:
        result = ("您的BMI为：",bmi_set)
        abc = ("偏胖")
    else:
        result = ("您的BMI为：",bmi_set)
        abc = ("肥胖")
    Bmi1.set(result)
    Bmi2.set(abc)

button_bmi = tkinter.Button(tk,text = "BMI",command = bmi)
button_bmi.place(x = 50,y = 110,width = 300,height = 40)
#添加显示结果的输入框
entry_bmi1=tkinter.Entry(tk,textvariable = Bmi1)
entry_bmi1.place(x = 30,y = 160,width = 340,height = 50)
entry_bmi2=tkinter.Entry(tk,textvariable = Bmi2)
entry_bmi2.place(x = 30,y = 210,width = 340,height = 50)

tkinter.mainloop()

```
