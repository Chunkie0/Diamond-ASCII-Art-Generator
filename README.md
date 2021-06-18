# Diamond-ASCII-Art-Generator
## This will generate a diamond based on your size and a symbol of your choosing

### Small descritption of how the code works:

Gets user input and converts it to integer:
```
user = int(input("Input size(no lower then 3 and has to be odd number): "))
```  
  
Checks if user input is no lower then 3 and will ask till the correct input is given, since diamonds ain't looking like this:  
*  
or whatever this is:  
 *  
**
```
while user < 3:
  print("Size can't be lower then 3")
  user = int(input("Input again: "))
```  
  
Adds 1 to the user input if its even because sometimes it can be to hard read:
```
if user % 2 == 0:
  print("+1 to your even number was inevitable")
  user += 1
```  
  
Loops through numbers starting from 1 to user input and skips by 2. If user input for example is 7 it will look something like this (1,3,5,7):  
```
for i in range(1, user, 2):
```  
  
Adds spacing for the first few loops up until we reach the actual center for example if input was 3:  
For the first line: 
3//2 = 1 and 1//2 = 0, 1-0 = 1, which means we need 1 space before 1 symbol because symbol * 1  
and after we skip 2 steps from upper code example it will look something like this:  
3//2 = 1 and 3//2 = 1, 1-1 = 0, which means we wont need space and just 3 symbols because symbol * 3  
```
print(" "*(user//2-i//2), symbol*i)
```  
Same idea as upper example but just in reverse order:
```
for i in range(user, 0, -2):
    print(" "*(user//2-i//2), symbol*i)
```
