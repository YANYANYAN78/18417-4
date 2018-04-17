# 18417-4
重复数字求和


求s=a+aa+aaa+aaaa+aa...a的值，其中a是一个数字。例如2+22+222+2222+22222(此时共有5个数相加)，几个数相加由键盘控制。

Tn = 0
Sn = []
n = int(raw_input('n = '))
a = int(raw_input('a = '))
for count in range(n):
    Tn = Tn + a
    a = a * 10
    Sn.append(Tn)
    print Tn
 
Sn = reduce(lambda x,y : x + y,Sn)
print "计算和为：",Sn




a = int(raw_input("a:"))
n = int(raw_input("n:"))
list=[]
for i in range(1,n+1):
    list.append(int("{}".format(a)*i))
s = reduce(lambda x,y:x+y, list)
print list
print "计算和为：",s




def calculate(a,n):
    sum = 0
    for i in range(1,n+1):
        x = int(str(a)*i)
        sum+=x
    print sum
calculate(4,4)
