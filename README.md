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

![Screenshot 2024-08-22 203754](https://github.com/user-attachments/assets/0b67cafc-403b-405b-b173-ebccd7b93d0f)



cat < file2
## OUTPUT

![Screenshot 2024-08-22 203804](https://github.com/user-attachments/assets/380407ec-25ea-492c-b65d-430ff88f76b8)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot 2024-08-22 203815](https://github.com/user-attachments/assets/634dce5b-f151-416c-9af8-459d39fc1546)

comm file1 file2
 ## OUTPUT

 ![Screenshot 2024-08-22 203829](https://github.com/user-attachments/assets/262fda89-2565-4601-b505-b868b9bebdef)

diff file1 file2
## OUTPUT
![Screenshot 2024-08-22 213358](https://github.com/user-attachments/assets/672024fe-23ff-4b5f-bd7e-2adf2645cea1)

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

![Screenshot 2024-08-22 204739](https://github.com/user-attachments/assets/399564de-5947-4cd9-955b-f6ba125c355a)



cut -d "|" -f 1 file22
## OUTPUT

![Screenshot 2024-08-22 204745](https://github.com/user-attachments/assets/e9dc0042-5911-48a4-9437-c937df780c62)


cut -d "|" -f 2 file22
## OUTPUT

![Screenshot 2024-08-22 204752](https://github.com/user-attachments/assets/20e91f8c-e1b3-42fa-a5dd-6c2e33088a4a)

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


![Screenshot 2024-08-22 205107](https://github.com/user-attachments/assets/6e4914cf-5365-417a-8941-e5b631188168)

grep hello newfile 
## OUTPUT


![Screenshot 2024-08-22 205115](https://github.com/user-attachments/assets/1c2b5e73-191c-4b0f-aa88-1c315fe564a5)


grep -v hello newfile 
## OUTPUT

![Screenshot 2024-08-22 205121](https://github.com/user-attachments/assets/ae686295-70da-49cd-a2fb-3c0c8b97433d)


cat newfile | grep -i "hello"
## OUTPUT

![Screenshot 2024-08-22 205539](https://github.com/user-attachments/assets/c8ba634e-8dee-4dcd-93cb-c0fe1e3a7de1)



cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot 2024-08-22 205547](https://github.com/user-attachments/assets/531a5abb-3efb-4d3f-b7a1-698c00786f50)



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT

![Screenshot 2024-08-22 205553](https://github.com/user-attachments/assets/a5730ea8-08e5-483b-a275-a9fb07d15e49)

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
![Screenshot 2024-08-22 214829](https://github.com/user-attachments/assets/8a80d552-916e-418a-becf-d0d056eb6af4)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot 2024-08-22 214912](https://github.com/user-attachments/assets/9cea2efe-3a7d-4ba4-b39f-7eee73141971)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot 2024-08-22 215127](https://github.com/user-attachments/assets/b5768d65-e458-4a01-9e81-a30c2d12663f)




egrep '(^hello)' newfile 
## OUTPUT

![Screenshot 2024-08-22 214958](https://github.com/user-attachments/assets/997c57bc-4c78-41fa-8eb8-b54cf869e541)


egrep '(world$)' newfile 
## OUTPUT

![Screenshot 2024-08-22 215202](https://github.com/user-attachments/assets/5afd630e-e0ec-401c-9408-60e586c23aa3)


egrep '(World$)' newfile 
## OUTPUT

![Screenshot 2024-08-25 122157](https://github.com/user-attachments/assets/92550f49-2de9-4121-b0e9-6c8286435dac)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot 2024-08-22 215322](https://github.com/user-attachments/assets/e9cd53bc-67f6-4812-a0a8-7c96ae587207)


egrep '[1-9]' newfile 
## OUTPUT

![Screenshot 2024-08-22 215404](https://github.com/user-attachments/assets/568bb9c9-0aab-49f7-bc3d-d75de5902d21)


egrep 'Linux.*world' newfile 
## OUTPUT

![Screenshot 2024-08-22 215436](https://github.com/user-attachments/assets/7e9eaa42-0122-476d-94e8-f703464bf546)

egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot 2024-08-25 122759](https://github.com/user-attachments/assets/96723f42-041f-40c8-b231-941bfb686c61)


egrep l{2} newfile
## OUTPUT

![Screenshot 2024-08-25 160654](https://github.com/user-attachments/assets/93d948af-528a-4fe8-850d-1ea80778eb3d)


egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot 2024-08-25 122806](https://github.com/user-attachments/assets/92857485-5eb3-4bc1-8976-bdaa9a86f97a)


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

![Screenshot 2024-08-25 125009](https://github.com/user-attachments/assets/d25deb87-8c6d-48a5-a4eb-213ec0c2d1eb)


sed -n -e '$p' file23
## OUTPUT

![Screenshot 2024-08-25 125014](https://github.com/user-attachments/assets/3df91a92-85ce-4a98-bab1-f838252f3bbc)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot 2024-08-25 125025](https://github.com/user-attachments/assets/59270ae2-0cfd-4a01-a700-d7adbae1b31d)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot 2024-08-25 125045](https://github.com/user-attachments/assets/ada0b8cc-fe87-4768-9868-56d82231d760)



sed  '/tom/s/5000/6000/' file23
## OUTPUT


![Screenshot 2024-08-25 125053](https://github.com/user-attachments/assets/26549846-b219-4b84-a650-3f1f83221ccf)

sed -n -e '1,5p' file23
## OUTPUT

![Screenshot 2024-08-25 125059](https://github.com/user-attachments/assets/e43011d5-1da2-4cfc-b79a-e971640efb61)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot 2024-08-25 125110](https://github.com/user-attachments/assets/0e2d68fe-7cf5-4a91-b8e7-74535664636e)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


![Screenshot 2024-08-25 125122](https://github.com/user-attachments/assets/fe5b1c42-8f62-44c4-9bd0-5cc7735d1841)

seq 10 
## OUTPUT


![Screenshot 2024-08-25 125146](https://github.com/user-attachments/assets/01782d3b-7bba-410f-94fb-15097eb79506)

seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot 2024-08-25 125520](https://github.com/user-attachments/assets/8d52a121-2235-4aec-8298-6f2b1b441353)


seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot 2024-08-25 125616](https://github.com/user-attachments/assets/8e6b0968-0220-4544-9096-f7c6ff0345af)


seq 3 | sed '2a hello'
## OUTPUT

![Screenshot 2024-08-25 125645](https://github.com/user-attachments/assets/7b748a76-0565-4a2f-a07f-447de60d590a)


seq 2 | sed '2i hello'
## OUTPUT
![Screenshot 2024-08-25 125717](https://github.com/user-attachments/assets/8d0685fd-252d-451f-93bf-4214aabaee0a)


seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot 2024-08-25 125823](https://github.com/user-attachments/assets/e2bcdef2-2039-4a03-af6a-01e0904f7e14)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


![Screenshot 2024-08-25 131010](https://github.com/user-attachments/assets/8d3aa46b-ccb7-4dd4-bb6c-499779615c79)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT



![Screenshot 2024-08-25 125907](https://github.com/user-attachments/assets/836fd3d8-ad50-40fe-9534-a4fdfb94b631)



#Sorting File content!

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
![Screenshot 2024-08-25 123408](https://github.com/user-attachments/assets/3da43442-4652-432d-8203-20a904a14d5d)


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

![Screenshot 2024-08-25 123720](https://github.com/user-attachments/assets/98b66d55-6d92-4465-abf0-ac2ae6bdc313)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![Screenshot 2024-08-25 130813](https://github.com/user-attachments/assets/fdd6f051-db95-41fa-a31d-f41d6d4118f2)

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

![Screenshot 2024-08-25 144857](https://github.com/user-attachments/assets/b85862d5-f98c-4ef5-922c-4bd8d5552585)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot 2024-08-25 144904](https://github.com/user-attachments/assets/cd55acd6-943d-4b69-bc48-d0fcf515dce9)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![Screenshot 2024-08-25 155214](https://github.com/user-attachments/assets/823a3a52-0a68-4bdf-85bc-7aec659c2728)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot 2024-08-25 160112](https://github.com/user-attachments/assets/318769b6-675a-43b2-8c1e-e2f2575e092a)


tar -xvf backup.tar
## OUTPUT
![Screenshot 2024-08-25 160127](https://github.com/user-attachments/assets/89c952c5-559c-4b18-b81a-7b39491290e4)

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 ![Screenshot 2024-08-25 150944](https://github.com/user-attachments/assets/7c9bd5b3-ca87-4f7c-b36f-c5ae66db0b43)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot 2024-08-25 150955](https://github.com/user-attachments/assets/5f9bad4a-6f35-4528-8ee0-d8725fb576f3)


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
```./scriptest.sh: line 1: #!/bin/sh: No such file or directory
“File name is ./scriptest.sh ”
File name is  scriptest.sh
“First arg. is ” 1
“Second arg. is ” 2
“Third arg. is ” 3
“Fourth arg. is ”
The $@ is  1 2 3
The $\# is  1#
The $$ is  14337
    PID TTY          TIME CMD
  13614 pts/1    00:00:00 bash
  14337 pts/1    00:00:00 bash
  14340 pts/1    00:00:00 ps
```

 
ls file1
## OUTPUT
![Screenshot 2024-08-25 164426](https://github.com/user-attachments/assets/9efeb4cb-fd16-4254-9ba9-302957c179d0)

echo $?
## OUTPUT 
![Screenshot 2024-08-25 164025](https://github.com/user-attachments/assets/cff33863-a40b-47f3-921b-edaacdde49d7)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![Screenshot 2024-08-25 164037](https://github.com/user-attachments/assets/24689d39-c0dc-4580-9ae9-b5e3d45efeac)

abcd
 
echo $?
 ## OUTPUT


 ![Screenshot 2024-08-25 164037](https://github.com/user-attachments/assets/0ff1a259-1224-411b-9e49-c911f675932f)

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
##OUTPUT
```
baseball is less than hockey
```


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
```
You are the owner of the /etc/passwd file
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
```


“/home/sec The object exists, is it a file?”
“No,/home/sec it is not a file!”
“But /home/sec/.bash_history is a file!”

```
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
##OUTPUT
```
“The test value 10 is greater than 5”
“The values are different”


```
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
##OUTPUT
```
“/home/sec The object exists, is it a file?”
“No,/home/sec it is not a file!”
“But /home/sec/.bash_history is a file!”
```
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
```
./elifcheck.sh: line 1: #!/bin/bash: No such file or directory
Sorry, you are not allowed here
```

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
./ifcompound.sh: line 1: #!/bin/bash: No such file or directory
The file exists and you can write to it
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
##OUTPUT
```
Sorry, you are not allowed here
```
 
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
##OUTPUT
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
##OUTPUT
```
./untiltest.sh: line 1: #using: command not found
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
 
 ## OUTPUT
 ```
./forin1.sh: line 1: #!/bin/bash: No such file or directory
./forin1.sh: line 2: #basic: command not found
The next state is Alabama
The next state is Alaska
The next state is Arizona
The next state is Arkansas
The next state is California
The next state is Colorado
```
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
 
$ ./forin2.sh 
## OUTPUT
```
“word:I”
“word:dont know if thisll”
“word:work”
```
 
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
## OUTPUT
```
word:I
word:don't
word:know
word:if
word:this'll
word:work
```
 
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
##OUTPUT
```
Visit beautiful cities
Visit beautiful cities
Visit beautiful cities
Visit beautiful cities
Visit beautiful cities
Visit beautiful cities
Visit beautiful cities
```
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


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
The value is i is 1
The value is i is 2
The value is i is 3
The value is i is 4
The value is i is 5
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
1 - 5
2 - 4
3 - 3
4 - 2
5 - 1
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
Starting loop 1:
 Inside loop: 1
 Inside loop: 2
 Inside loop: 3
Starting Loop 2:
 Inside loop: 1
 Inside loop: 2
 Inside loop: 3
Starting Loop 3:
 Inside loop: 1
 Inside loop: 2
 Inside loop: 3
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
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
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
Enter your name: Haritharamesh
Hello Haritharamesh , welcome to my program. 
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
Enter your name: Haritharamesh
Hello Haritharamesh, welcome to my program.
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
## OUTPUT
 ./funcex.sh 
```
Usage: badtest1 a b
```
 
 ./funcex.sh 1 2

 ```
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
$ ./argshift.sh 1 2 3
```
1
2
3
```
 
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
$ ./argshift.sh 1 2 3
```
1
2
3
```
 
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
 ./argshift.sh 1 2 3
 ```
+ ((  3  ))
+ echo 1 
1
+ shift
+ ((  2  ))
+ echo 2
2
+ shift
+ ((  1  ))
+ echo 3
+ shift
+ ((  0  ))
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
7         bcdfghj
8	  abcdfghj
7	  bcdfghj
8  	  ebcdfghj
7	  bcdfghhj
8	  ibcdfghj
7	  bcdfghj
8	  obcdfghj
7	  bcdfghj
8 	  ubcdfghj
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
locathost:~# chmod 755 palindrome.sh
locathost:~# ./palindrome.sh
Enter the number
21
Number is NOT palindrome
locathost:~# chmod 755 palindrome.sh
locathost:~# ./palindrome.sh
Enter the number
33
Number is palindrome
locathost:~#

```


# RESULT:
The Commands are executed successfully.
