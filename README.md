# OS-Linux-commands-Shell-scripting 
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
![Screenshot 2024-08-20 084108](https://github.com/user-attachments/assets/b73cf7c2-325c-4978-9c88-baad063ce74e)

cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/ba9a3007-d5ce-406e-adf1-b88bb1ee8502)

# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/df93ee81-48f6-4914-8113-88ef4db2972e)

comm file1 file2
 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/d029ef16-1ead-4f69-a412-6b6fbf0e5e6e)
 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/bef6da6f-498e-4e10-a04b-0d25f77ecbae)

#Filters
### Create the following files file11, file22 as follows:
cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```
cut -c1-3 file11
## OUTPUT
![image](https://github.com/user-attachments/assets/a5fc1124-f6c3-47a6-a4d4-f1f0ffc05ed0)

cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/3227c125-aefb-479d-a6c6-dcd577a604ed)

cut -d "|" -f 2 file22
## OUT![image](https://github.com/user-attachments/assets/ea43c91a-070a-4d18-8189-b6f4173112a4)
PUT
cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
grep Hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/6e9a43e7-dd1b-42a3-8d49-46760a9b8cfe)

grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/b2677f1c-613c-43b6-bbb5-b707cb7d6b67)

grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/5b6e60e3-50e4-4aff-9624-551cf49e98a0)

cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/443e934e-8f0e-49c4-a9b8-595c8449df54)

cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/a9d87d19-5aff-4f98-aeb3-52d8a24cf612)
grep -R ubuntu /etc
## OUTPUT
grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/a6aa4f67-e600-4c4c-891c-e15f37f2add6)

cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```
cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/6259a30b-aefb-441c-b58d-efcbc8adee34)

egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/2b90a0df-4d84-47ed-935c-67d507989efd)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/168dfa0f-86c8-4a00-9bcd-55f0147b09f4)

egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/f918a76f-018f-41ef-8a35-e913a9aa4986)

egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/7ff024cb-7857-4582-a1bc-3695d7cb13b8)

egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/8e077874-9d55-4da3-aadb-655087130814)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/46d33cbe-7e59-43ca-be10-04bdb70cfb57)

egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/37532a75-ecf5-492d-98d5-97bbd84864ec)

egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/1283ba85-1822-49e4-8b2e-20e96d23db5a)

egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/f8fe1814-2f95-402b-8c0f-165780b0361e)

egrep l{2} newfile
## OUTPUT
egrep 's{1,2}' newfile
## OUTPUT 
cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```
sed -n -e '3p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/957fa429-a9c5-40ea-9eb2-bd19e1917935)

sed -n -e '$p' file23
## OUTPUT

sed  -e 's/Ram/Sita/' file23
## OUTPUT

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/6fccb989-6a6f-48e2-ac18-5e33dcec0a9f)

sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/0bc54200-cb88-44ac-86e9-36763ec89fa5)

sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/f66b6e48-3468-43f2-92b2-e51de1c2d494)

sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/fbb3b197-d1dc-41c4-b1e2-bfe042e3d08e)

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/f701e4fe-ed77-4039-9ba5-4dedaf4ad7e4)

seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/ee64f482-300b-45ec-9802-72783eaab353)

seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/8e54c37d-1d12-4547-97bf-5b0b1feb38b5)

seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/eb5aae24-8195-473a-9cf4-ea0d39aa8318)

seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/26561e44-cd26-4b9b-85b2-e67c53ad1828)

seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/d9378e43-7ce4-47bd-90ee-f0baddba4e90)

seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/617531c9-b1df-4575-9108-245285ecb33c)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/a6b91238-9633-42dc-9a76-661e2214b1aa)

sed -n '2,4{s/$/*/;p}' file23
# output
![image](https://github.com/user-attachments/assets/14642bf4-0ed2-486a-b1ee-aad13742b167)

## Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![image](https://github.com/user-attachments/assets/4681ee0e-efca-4205-a841-784d8ce26e3d)

cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
![image](https://github.com/user-attachments/assets/c28d7921-a799-4406-8d6a-6b11275b7a7a)

# Using tr command
cat file23 | tr [:lower:] [:upper:]
## OUTPUT
![image](https://github.com/user-attachments/assets/76dea436-2d61-4f5f-a538-7ed5be4e4c76)

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![image](https://github.com/user-attachments/assets/2a4cccf7-94db-4693-87a3-e482154db073)

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/bc7c2c12-14ba-4c5d-bbf2-e48bf994afcf)

# Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/54440205-9f30-4c32-bfc5-bfd2def2a054)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
```
-rw-r--r-- user/group 0 2024-02-25 14:30:00 file1.txt
drwxr-xr-x user/group 0 2024-02-25 14:30:00 directory1/
-rw-r--r-- user/group 1024 2024-02-25 14:30:00 directory1/file2.txt
-rw-r--r-- user/group 2048 2024-02-25 14:30:00 directory1/file3.txt
```
tar -xvf backup.tar
## OUTPUT
```
x file1.txt
x directory1/
x directory1/file2.txt
x directory1/file3.txt
```
gzip backup.tar

ls .gz
## OUTPUT
 ```
backup.tar.gz
```
gunzip backup.tar.gz
## OUTPUT
```
 backup.tar
```
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/ef8645ef-4744-4d2d-99ca-c4140504063c)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```
cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/ab08e663-3357-4252-927c-3050069d49ba)

cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```
cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![image](https://github.com/user-attachments/assets/97932fbf-1679-4847-8645-90e3980ab65c)

ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/5876faba-049c-4c92-9d1f-a04c75bb57bd)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/8e91c520-fc37-4827-94e3-ac610934df1b)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/03785b66-3005-413d-93e3-9317a6b53257)

abcd
echo $?
 ## OUTPUT
![image](https://github.com/user-attachments/assets/067793c0-5f83-48b3-aa36-8e116563b773)

# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```
cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
## OUTPUT
![image](https://github.com/user-attachments/assets/4cc12ef6-8e4c-490f-b79f-356c4637b826)

chmod 755 strcomp.sh
 ./strcomp.sh 
## OUTPUT
```
baseball is less than hockey
```
# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```
cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
```
You are the owner of the /etc/passwd file
```
# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```
./ifnested.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/ea96e35f-0220-4a8e-b0fe-e1f0dd500c55)

# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```
cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```
$ chmod 755 iftest.sh
$ ./iftest.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/354b8ae3-5912-42a7-bd4c-f7447033dd77)

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/d5fb762a-1b23-48ce-a120-ef44436151cc)

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```
$ chmod 755 elifcheck.sh
$ ./elifcheck.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/b844d03c-fd07-46ae-b9ef-ca63ed422794)

# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
```
Welcome Ram/Rahim
Please enjoy your visit
Special testing account
gganesh, Do not forget to logout when you're done
Sorry, you are not allowed here
```
# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
$ ./casecheck.sh 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
## output
 ```
10
9
8
7
6
5
4
3
2
1
```
cat untiltest.sh 
## Output
```
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
```
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 ## output
 ```
100
75
50
25
```
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
## output
```
The next state is Alabama
The next state is Alaska
The next state is Arizona
The next state is Arkansas
The next state is California
The next state is Colorado
```
$ ./forin2.sh 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
```
The next state is Alabama
The next state is Alaska
The next state is Arizona
The next state is Arkansas
The next state is California
The next state is Colorado
```
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
```
Visit beautiful Hyderabad
Visit beautiful Alampur
Visit beautiful Basara
Visit beautiful Warangal
Visit beautiful Adilabad
Visit beautiful Bhadrachalam
Visit beautiful Khammam
```

cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
```
The value of i is 1
The value of i is 2
The value of i is 3
The value of i is 4
The value of i is 5
```
cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
```
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
```
1 - 5
2 - 4
3 - 3
4 - 2
5 - 1
```
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
```
Iteration number: 1
Iteration number: 2
The for loop is completed
```
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
$ chmod 755 forcontinue.sh
$ ./forcontinue.sh 
## OUTPUT
```
Iteration number: 1
Iteration number: 2
Iteration number: 4
Iteration number: 5
The for loop is completed
```
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
$ chmod 755 exread.sh 
$ ./exread.sh 
## OUTPUT
```
Enter your name: John
Hello John, welcome to my program.
```
cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
## OUTPUT
```
Enter your name: sanju
Hello sanju, welcome to my program.
```
$ ./exread1.sh 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
./funcex.sh 
./funcex.sh 1 2
## OUTPUT
```
 $ bash script.sh 1 2
The result is 2
```
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
## OUTPUT
```
1
2
3
```
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
```
1
2
3
```
$ ./argshift.sh 1 2 3
 cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
```
+ (( 0 ))
+ set +x
```
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 ```
total characters 75
Number of Lines are 10
No of Words count: 10
```
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
```
Enter the number
121
Number is palindrome
Enter the number
69
Number is NOT palindrome
```
# RESULT:
The Commands are executed successfully.
