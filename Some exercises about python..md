# 1.打印100之内的素数


```python
for i in range(2,101):
    shu = True      #(标志位)
    for j in range(2,i):
        if i % j == 0:
            shu = False
    if shu == True:
        print(i)
```


```python

```




# 2.打印三角形


```python
for i in range(9):
    print('*'*i)

for sichu in range(10):
    x = int(input('请输入一个奇数：'))
    if x % 2 != 0:
        y = (x + 1)/2
        for i in range(x+1):
            if i <= y :
                print('*'*i)
            else:
                print('*'*(2*int(y)-i))
        print('画图完成')
    else:
        print('无法画出三角形，请重新输入奇数：')
```

# 3.算本金利息


```python
#benjin = 10000
#利息 = 0.0325
benjin = 10000
for year in range(1,1000):
    new = benjin*(1+0.0325)
    benjin = new
    print(year, benjin)
    if benjin >=20000:

        break
```

# 4.计算小球十次弹跳的总路程


```python
#6.计算小球十次弹跳的总路程
#小球从100米落下
#每次弹回一半的高度

gaodu = 100
distance = 0
count = 1
while count < 11:
    distance += gaodu
    gaodu = gaodu * 0.5  #计算弹起的高度
    distance += gaodu    #把弹起的高度加上
    count += 1           #弹回次数加一
    print(distance)
zong = distance + gaodu  #最后再加一次才完整
print('总高度为：',zong)
```

# 5.猴子吃桃子 每天吃一半另多吃一个，11天时，就剩一个桃子了，问总共有多少桃子。


```python
taozi = 1
day = 11
for day in range(10,0,-1):
    taozi = (taozi + 1) * 2
    print(day,taozi)
```

# 6.用whil循环猜年龄

# 要求：只有三次机会，三次之后询问是否继续。使用whlie语句


```python
count = 0
my_age =24  #我的真实年龄是24岁
while count <3:
    your_anser = input('请输入我的年龄：')
    if your_anser.isdigit():
        your_anser = int(your_anser)
    else:
        print('输入格式不对，请输入整数')
        continue
    if your_anser > my_age:
        print('猜大了，小点')
    elif your_anser < my_age:
        print('猜小了，大点')
    else:
        print('You are right.')
        break
    count += 1
    if count == 3 :
        cmd = input('三次机会用完了，要不要再试一次？（y/n）')
        if cmd in ['y','Y','yes','YES']:
            count = 0
        else:
            print('See you.')
```


```python

```
