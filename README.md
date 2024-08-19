import random
a=random.randint(1,100)
b=int(input("請輸入一個1~100的數字,你有6次機會"))
c=6
d=1
e=100
for i in range(6):
    if b>100 or b<0:
        print("輸入錯誤，請輸入一個1~100的數字")
    if b==a:
       print("猜中了!")
       break
    else :
        c = c-1
        if d<a & a<b :
            print("猜錯了，你還有",c,"次機會，請從",d,"到",b,"再猜一次",end="")
            print()
            e=b
            if c==0:
                print("你失敗了")
                break
        elif b<a and a<e:
            print("猜錯了，你還有",c,"次機會，請從",b,"到",e,"再猜一次",end="")
            print()
            d=b
            if c==0:
                print("你失敗了，答案是",a,end="")
                break
    b=int(input())
