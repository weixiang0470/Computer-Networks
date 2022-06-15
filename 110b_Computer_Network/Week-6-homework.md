## **output.png**
### _**On Ubuntu**_
### **Step 1**
* Download install stegsolve.jar
```
wget http://www.caesum.com/handbook/Stegsolve.jar -O stegsolve.jar
```
*  Install java
```
sudo apt install default-jdk
```
### **Step 2**
* Go to the file that contain stegsolve.jar and open with java
```
java -jar stegsolve.jar
```
### **Step 3**
* You will see the application like this:

![stegsolve](Images/output1.PNG)

_Now you can put your picture and try it out!!!_
![outputans](Images/output2.PNG)

## **a.zip**
### _**Method 1 On Ubuntu**_
### **Step 1**
* Install fcrackzip 
```
apt install fcrackzip
```
* After install you can check some arguments this tool offer
```
fcrackzip --help
```
![fcrackzip_help](Images/azip2.PNG)
### **Step 2**
* Go to the directory that contain the target zip file and crack it
```
fcrackzip -b -u -v -l 4 a.zip
```
_Then we get the password~_

![azipans](Images/azip1.PNG)

### _**Method 2 On Windows**_
### **Step 1**
* Download John-the-ripper at
[https://www.openwall.com/john/](https://www.openwall.com/john/)
* Next, extract the file at desktop and rename it to 'john'.
### **Step 2**
* Open the into the 'run' folder, and use `Ctrl + Shift + N` to create the new folder and name it crack.
* Open the crack folder and put the target file `a.zip` into the crack folder.
### **Step 3**
* Open cmd and type in the commands:
```
cd desktop/john/run
zip2john.exe crack/a.zip > crack/key.txt
John.exe crack/a.zip crack/key.txt
```
_Now be patient to get the password_

![azipand](Images/2azip2.PNG)