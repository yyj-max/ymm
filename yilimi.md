

```python
# 创建一个字典students，key是学号，value是姓名
# 学生信息在students.csv文件里，从文件中读取并保存到字典

# 打开students.csv文件
file=open(r'C:\Users\meilidemeimei\Desktop\students.csv','r')

# 读取文件内容
lines=file.readlines()
# 抽取每行的学号和姓名，保存到字典
students={}
for line in lines:
    tmp_list=line.split(',')
    xuehao=tmp_list[0]
    xingming=tmp_list[1]
    students[xuehao]=xingming
    
# 从学号中随机抽取N个学号
import random

num=int(input("输入你要抽取的人数："))


```
