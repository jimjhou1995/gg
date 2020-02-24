

```python
##### number 4

def count(A): 
    print('No. of Upper case characters : ' , sum(1 for c in A if c.isupper()))
    print('No. of Lower case characters : ', sum(1 for c in A if c.islower()))

count('Mark')
count('HellYa')

```

    No. of Upper case characters :  1
    No. of Lower case characters :  3
    No. of Upper case characters :  2
    No. of Lower case characters :  4
    


```python
####5

def speed(Birthday,speed):
    if Birthday=='Yes'and speed < 66:
            print("No Ticket")
    elif Birthday=='Yes' and speed > 65 and speed < 86:
            print("Small Ticket")
    elif Birthday=='Yes' and speed > 85:
            print("big Ticket")
    elif Birthday=='No' and speed < 61:
            print("No Ticket")
    elif Birthday=='No' and speed > 60 and speed < 81:
            print("Small Ticket")
    elif Birthday=='No' and speed > 80:
            print("big Ticket")
            
speed('Yes',70)
```

    Small Ticket
    


```python
#### 1 
### moss dictionary
CODE = {'A': '.-',     'B': '-...',   'C': '-.-.', 
        'D': '-..',    'E': '.',      'F': '..-.',
        'G': '--.',    'H': '....',   'I': '..',
        'J': '.---',   'K': '-.-',    'L': '.-..',
        'M': '--',     'N': '-.',     'O': '---',
        'P': '.--.',   'Q': '--.-',   'R': '.-.',
     	'S': '...',    'T': '-',      'U': '..-',
        'V': '...-',   'W': '.--',    'X': '-..-',
        'Y': '-.--',   'Z': '--..',
        
        '0': '-----',  '1': '.----',  '2': '..---',
        '3': '...--',  '4': '....-',  '5': '.....',
        '6': '-....',  '7': '--...',  '8': '---..',
        '9': '----.'
        }

def main(msg):
	for char in msg:
		print(CODE[char.upper()])
		        
main('Mark')
main('Hello World')
```

    --
    .-
    .-.
    -.-
    ....
    .
    .-..
    .-..
    ---
    


    ---------------------------------------------------------------------------

    KeyError                                  Traceback (most recent call last)

    <ipython-input-74-85d1f8595967> in <module>()
         22 
         23 main('Mark')
    ---> 24 main('Hello World')
    

    <ipython-input-74-85d1f8595967> in main(msg)
         19 def main(msg):
         20         for char in msg:
    ---> 21                 print(CODE[char.upper()])
         22 
         23 main('Mark')
    

    KeyError: ' '



```python
 ####13
## ZODIAC DICTIONARY
def getChineseZodiac(birthday):
    #### transfer the birthday into year
    from datetime import tzinfo, timedelta, datetime
    from pytz import timezone 
    from dateutil.parser import parse
    datetime = parse(birthday) 
    year= datetime.year
    index = (year - ZODIAC[0][0]) % 12
    return ZODIAC[index][1] 
    
getChineseZodiac('08/08/1995')

```




    'Pig'




```python
#### 8
item = ['The module is difficult']
words = ['the’,’of’,’and’,’a’,’to’, ‘in’, ‘is’, ‘you’,‘that’,‘it’,’he,‘was’,’for’,’on’,’are’,’as’,‘with','his’,’they’,’I'] 
item2 = [" ".join([w for w in t.split() if not w in words]) for t in item]
item2





```




    ['The module is difficult']




```python
####11 
def checkdate(todays_date, scheduled_date ):
    #### transfer the date into datetime
    from datetime import tzinfo, timedelta, datetime
    from pytz import timezone 
    from dateutil.parser import parse
    todays_date = parse(todays_date) 
    scheduled_date = parse(scheduled_date) 
    if todays_date > scheduled_date:
        print('Scheduled Date passed')
    elif todays_date < scheduled_date:
          print('Scheduled Date still active')

checkdate('21st February', '3rd March')
checkdate('4th April', '3rd March')


```

    Scheduled Date still active
    Scheduled Date passed
    


```python
####2
from collections import defaultdict

wordsFreq = defaultdict(int)
while True:
    word = 'Hello World'
    if not word:
        break
    wordsFreq[word] += 1
```
