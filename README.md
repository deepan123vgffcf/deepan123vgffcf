import pandas as pd
import numpy  as np
from fractions import Fraction
  m=int(input('ENTER THE ORDER OF THE MATRIX'))
if m==3:
    print('\|/')
if m!=3:
    print('IT CANNOT ME PERFORMED TO THIS ORDER')
    exit('TRY AGAIN')
qq=int(input('ENTER THE  1*1 VALUE  OF THE MATRIX'))
ww=int(input('ENTER THE 1*2 VALUE OF THE MATRIX'))
rr=int(input('ENTER THE  1*3 VALUE OF THE MATRIX'))
tt=int(input('ENTER THE  2*1 VALUE OF THE MATRIX'))
uu=int(input('ENTER THE  2*2 VALUE OF THE MATRIX'))
aa=int(input('ENTER THE  2*3 VALUE OF THE MATRIX'))
dd=int(input('ENTER THE  3*1 VALUE OF THE MATRIX'))
ff=int(input('ENTER THE  3*2 VALUE OF THE MATRIX'))
hh=int(input('ENTER THE 3*3 VALUE OF THE MATRIX'))
a=[qq,ww,rr]
b=[tt,uu,aa]
q=[dd,ff,hh]
c=pd.DataFrame([a,b,q])
print('THIS IS THE FORMED MATRIX,WITH YOUR VALUE')
print(c)
x=b[1]*q[2]-b[2]*q[1]
w=a[0]*x
e=b[0]*q[2]-b[2]*q[0]
r=a[1]*e
d=b[0]*q[1]-b[1]*q[0]
f=a[2]*d
g=(w-r+f)
print('THIS IS YOUR DETERMINANT VALUE')
print(g)
qqq=b[1]*q[2]+b[2]*q[1]
qqq1=a[0]*qqq
aaa=b[0]*q[2]-b[2]*q[0]
aaa1=a[1]*aaa*(-1)
eee=b[0]*q[1]-b[1]*q[0]
eee1=a[2]*eee
rrr=a[1]*q[2]-a[2]*q[1]
rrr1=b[0]*rrr*(-1)
ttt= a[0]*q[2]-a[2]*q[0]
ttt1=b[1]*ttt
yyy=a[0]*q[1]-a[1]*q[0]
yyy1=b[2]*yyy*(-1)
uuu= a[1]*b[2]-a[1]*b[1]
uuu1=q[1]*uuu
ppp=a[0]*b[2]-a[2]*b[0]
ppp1=q[1]*ppp*(-1)
jjj=a[0]*b[1]-a[1]*b[0]
jjj1=q[1]*jjj
mid=[qqq1,aaa1,eee1]
deep=[rrr1,ttt1,yyy1]
suk=[uuu1,ppp1,jjj1]
bn=pd.DataFrame([mid,deep,suk])
bn1=bn.T
print('THIS IS THE adj(A)')
print(bn1)
print('\\\\\\\\\\\THIS IS YOUR REQUIRED A INVERSE//////////')
print(Fraction(1,g)*bn1)


