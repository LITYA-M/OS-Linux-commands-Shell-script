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
<img width="287" height="146" alt="Screenshot from 2026-01-29 21-02-13" src="https://github.com/user-attachments/assets/a11137fe-59e1-4753-a8ef-ac3236e592f5" />



cat < file2
## OUTPUT
<img width="287" height="146" alt="Screenshot from 2026-01-29 21-06-33" src="https://github.com/user-attachments/assets/2b81ba03-1a45-4379-842e-e15334abd0c9" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="357" height="49" alt="Screenshot from 2026-01-29 21-07-26" src="https://github.com/user-attachments/assets/17f1ab96-c6b0-472d-b086-4b2d30b0526c" />

comm file1 file2
 ## OUTPUT
<img width="327" height="190" alt="Screenshot from 2026-01-29 21-08-05" src="https://github.com/user-attachments/assets/3b36b8fc-7669-4efb-b074-e3d66be32e20" />

 
diff file1 file2
## OUTPUT
<img width="315" height="231" alt="Screenshot from 2026-01-29 21-08-56" src="https://github.com/user-attachments/assets/432b3776-80e0-4b24-88a5-83b694dda1f8" />


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
<img width="345" height="69" alt="Screenshot from 2026-01-29 21-24-52" src="https://github.com/user-attachments/assets/d04f6904-5b8a-49ba-987a-b028e3d0f254" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="349" height="92" alt="Screenshot from 2026-01-29 21-25-34" src="https://github.com/user-attachments/assets/dea65289-61b0-413d-8a4c-2ae3ca2103bf" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="349" height="92" alt="Screenshot from 2026-01-29 21-25-43" src="https://github.com/user-attachments/assets/3738ddb6-91c1-4a94-97a0-159651c80249" />

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

<img width="340" height="67" alt="Screenshot from 2026-01-29 21-42-09" src="https://github.com/user-attachments/assets/a1b35051-4622-40d8-b0c2-7c62893a776f" />


grep hello newfile 
## OUTPUT
<img width="353" height="49" alt="Screenshot from 2026-01-29 21-44-17" src="https://github.com/user-attachments/assets/1f374414-e608-423d-af5f-6a78a7fde90d" />




grep -v hello newfile 
## OUTPUT



cat newfile | grep -i "hello"
## OUTPUT

<img width="477" height="71" alt="Screenshot from 2026-01-29 22-33-28" src="https://github.com/user-attachments/assets/5b89326f-1d45-4f55-bfe8-006ea7fd6df3" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="481" height="54" alt="Screenshot from 2026-01-29 22-34-00" src="https://github.com/user-attachments/assets/2bbf7d70-864a-4753-b451-180a81a36c2a" />



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="479" height="79" alt="Screenshot from 2026-01-29 22-36-37" src="https://github.com/user-attachments/assets/3bae1f52-849d-43da-941b-6217b7a4d015" />


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

<img width="479" height="79" alt="Screenshot from 2026-01-29 22-43-03" src="https://github.com/user-attachments/assets/612df8f4-9686-4e71-982e-c0f2b306c3fa" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="479" height="79" alt="Screenshot from 2026-01-29 22-44-10" src="https://github.com/user-attachments/assets/604dd59f-b42b-486a-80c7-1aaa6a743678" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="479" height="79" alt="Screenshot from 2026-01-29 22-44-52" src="https://github.com/user-attachments/assets/aa88b92e-c978-42eb-9f70-c9b43e8ef3fc" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="477" height="61" alt="Screenshot from 2026-01-29 22-46-23" src="https://github.com/user-attachments/assets/09171130-b593-452f-b58d-222d0d81efda" />



egrep '(world$)' newfile 
## OUTPUT



egrep '(World$)' newfile 
## OUTPUT


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="476" height="118" alt="Screenshot from 2026-01-29 22-54-06" src="https://github.com/user-attachments/assets/950fea96-e4f4-4462-b731-e7db0f281caf" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="468" height="51" alt="Screenshot from 2026-01-29 22-55-22" src="https://github.com/user-attachments/assets/a8747ff4-20ad-4ae7-8195-2515b42ce98d" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="468" height="51" alt="Screenshot from 2026-01-29 22-59-55" src="https://github.com/user-attachments/assets/5911ce3e-248c-4736-9de8-81c2958cb472" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="468" height="51" alt="Screenshot from 2026-01-29 23-00-03" src="https://github.com/user-attachments/assets/8b2124dd-c283-49bb-9386-44012f4de18a" />


egrep l{2} newfile
## OUTPUT
<img width="469" height="67" alt="Screenshot from 2026-01-29 23-02-18" src="https://github.com/user-attachments/assets/0fa518e3-48f3-4a7c-a45e-1351ab8d626a" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="464" height="90" alt="Screenshot from 2026-01-29 23-02-26" src="https://github.com/user-attachments/assets/7243a7a7-9872-4fb7-b202-7cd05a6aeda2" />


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
<img width="449" height="53" alt="Screenshot from 2026-01-29 23-11-48" src="https://github.com/user-attachments/assets/5677f128-c200-4433-a046-7b9b3d05267a" />



sed -n -e '$p' file23
## OUTPUT

<img width="449" height="53" alt="Screenshot from 2026-01-29 23-12-21" src="https://github.com/user-attachments/assets/50dbe0e9-bb97-47cf-8236-09d103f7f028" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="462" height="204" alt="Screenshot from 2026-01-29 23-13-35" src="https://github.com/user-attachments/assets/fecab6cc-b7b4-47d8-9101-92ab5e9feffa" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="462" height="204" alt="Screenshot from 2026-01-29 23-14-00" src="https://github.com/user-attachments/assets/426c1a00-e5bd-43c0-ac93-265f3c163fbf" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="484" height="206" alt="Screenshot from 2026-01-29 23-15-24" src="https://github.com/user-attachments/assets/1ca7d4a5-d2c0-42bc-9417-eebfe5b3dc56" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="495" height="140" alt="Screenshot from 2026-01-29 23-16-25" src="https://github.com/user-attachments/assets/1c017377-45a2-4b38-8cb2-6f46ccffd30d" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="498" height="157" alt="Screenshot from 2026-01-29 23-17-20" src="https://github.com/user-attachments/assets/e67377bc-43b1-4b6b-9c08-68c43abe4a7c" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="511" height="139" alt="Screenshot from 2026-01-29 23-18-29" src="https://github.com/user-attachments/assets/e6a40bc9-de37-46cb-80f2-6f07cbed61de" />


seq 10 
## OUTPUT
<img width="516" height="246" alt="Screenshot from 2026-01-29 23-18-54" src="https://github.com/user-attachments/assets/d87b1a03-aa17-4373-8df8-ae22e99c8270" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="547" height="97" alt="Screenshot from 2026-01-29 23-19-38" src="https://github.com/user-attachments/assets/252a55db-8ec4-4155-94f2-b708d413796d" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="547" height="97" alt="Screenshot from 2026-01-29 23-20-20" src="https://github.com/user-attachments/assets/d199dd1a-7e48-4983-83c9-58eb558f8559" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="556" height="115" alt="Screenshot from 2026-01-29 23-21-22" src="https://github.com/user-attachments/assets/e0e74053-a1c9-49c3-92bd-1df044b8e485" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="565" height="95" alt="Screenshot from 2026-01-29 23-21-57" src="https://github.com/user-attachments/assets/2e706636-cb0b-44f6-9d78-47c228a18fff" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="565" height="95" alt="Screenshot from 2026-01-29 23-22-54" src="https://github.com/user-attachments/assets/f899a280-078b-4f5d-a1d9-db379d4ce383" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="565" height="95" alt="Screenshot from 2026-01-29 23-31-19" src="https://github.com/user-attachments/assets/bc0da5ed-4df6-401f-83f1-0b8d78b186f0" />



sed -n '2,4{s/$/*/;p}' file23

<img width="565" height="95" alt="Screenshot from 2026-01-29 23-32-02" src="https://github.com/user-attachments/assets/7c9f8a12-4069-4866-ad99-c91f396ffe02" />


#Sorting File content
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
<img width="564" height="140" alt="Screenshot from 2026-01-29 23-34-40" src="https://github.com/user-attachments/assets/1ad2ad93-cdd4-4ff0-a320-0fe29074bac9" />


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
<img width="332" height="142" alt="Screenshot from 2026-02-01 19-56-10" src="https://github.com/user-attachments/assets/69fb5b69-d762-4cb0-ad23-c8bac31acb44" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="562" height="206" alt="Screenshot from 2026-01-29 23-40-35" src="https://github.com/user-attachments/assets/311c57ff-4544-4152-89df-61a8132ef3d2" />

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
<img width="426" height="100" alt="Screenshot from 2026-02-01 20-00-03" src="https://github.com/user-attachments/assets/323a3755-54c6-456b-a013-07ed9dee4993" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="589" height="97" alt="Screenshot from 2026-01-29 23-50-51" src="https://github.com/user-attachments/assets/e0254094-cdd5-4248-aa95-738fe283b026" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="617" height="545" alt="Screenshot from 2026-01-29 23-53-09" src="https://github.com/user-attachments/assets/8eb6385c-e458-4e32-b59c-aec767493a4a" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

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

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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

 
 ./funcex.sh 1 2

 
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


# RESULT:
The Commands are executed successfully.
