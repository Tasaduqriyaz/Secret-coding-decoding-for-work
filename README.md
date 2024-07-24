# program  for secret coding and decoding language
import string
import random

message=input('enter the word')
words=message.split(' ')
newwords=[]
reply = input('enter the reply for code or decode')
# for coding a paticular message
if reply == 'code':
    for word in words:
         if len(word) >= 3:
             first=''.join(random.choices(string.ascii_lowercase ,k=3))
             last=''.join(random.choices(string.ascii_lowercase ,k=3))
             message=first+word[1:]+word[0]+last
             newwords.append(message)

         else:
             message=word[::-1]
             newwords.append(message)
    print(' '.join(newwords))        
        
# for decoding a particular message      
else:
    
    for word in words:
         if len(word) >= 3:
             message=word[3:-3]
             message=message[-1]+message[:-1]
             newwords.append(message)
         else:
             message=word[::-1]
             newwords.append(message)
    print(' '.join(newwords))   
