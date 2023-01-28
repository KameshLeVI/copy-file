# copy-file
## AIM:
To write a python program for copying the contents from one file to another file.
## EQUIPEMENT'S REQUIRED: 
PC
Anaconda - Python 3.7
## ALGORITHM: 
### Step 1:
Use open function to open the file in which we want to copy from and access it in read mode

### Step 2:
Read the file and store in a variable

### Step 3:
Now create a new file in which we want to paste the content using write access mode

### Step 4:
Use write function to copy the read file that has been stored in the variable

### Step 5:
The content in the original file will be copied in the new file

### Step 6:
End the program

## PROGRAM:
```
# python program for copying the contents from one file to another file.
# Developed by: Kamesh
#RegisterNumber: 22005358

from shutil import copyfile
from sys import exit
source = input("Enter source file with full path: ")
target = input("Enter target file with full path: ")

try:
    copyfile(source, target)
except IOError as e:
    print("Unable to copy file. %s" % e)
    exit(1)
except:
    print("Unexpected error:", sys.exc_info())
    exit(1)

print("\nFile copy done!\n")

while True:
    print("Do you like to print the file ? (y/n): ")
    check = input()
    if check == 'n':
        break
    elif check == 'y':
        file = open(target, "r")
        print("\nHere follows the file content:\n")
        print(file.read())
        file.close()
        print()
        break
    else:
        continue
```

### OUTPUT:
![](/Screenshot%202023-01-29%20001301.png)
![](/Screenshot%202023-01-29%20001322.png)



## RESULT:
Thus the program is written to copy the contents from one file to another file.