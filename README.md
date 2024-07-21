# program  for secret coding and decoding
a=input('enter the word')
reply = input('enter the reply for code or decode')
# for coding a paticular word
if reply == 'code':
    if len(a) >= 3:
        b=a[0]
        c= "".join([a,b])
        d=c.replace(c[0],'abc',1)
        e='xyz'
        f="".join([d,e])
        print(f)
    else:
        print("".join([a[-1],a[0]]))
# for decoding a particular word        
else:
        if len(a)>=3:
              g=a.replace('abc','',1)
              h=g.replace('xyz','',1) 
              i="".join([h[-1],h])
              j=i.replace(i[-1],'',2)
              k="".join([h[-1],j])
              print(k)
        else:
              print("".join([a[-1],a[0]]))
