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
<img width="565" height="133" alt="image" src="https://github.com/user-attachments/assets/96279a69-58f8-4f92-b09a-c45d9858ed7e" />



cat < file2
## OUTPUT
<img width="563" height="135" alt="image" src="https://github.com/user-attachments/assets/82cbd698-431c-4e3a-bcdb-0c810152c8af" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="597" height="47" alt="image" src="https://github.com/user-attachments/assets/4771c01b-9886-4d0c-b514-74e93ab2d67c" />


comm file1 file2
 ## OUTPUT
<img width="598" height="243" alt="image" src="https://github.com/user-attachments/assets/8e548b26-b93d-4662-9518-c64516396553" />

 
diff file1 file2
## OUTPUT
<img width="596" height="242" alt="image" src="https://github.com/user-attachments/assets/7a65f92b-9bb4-4528-94f4-a11085fcb0fb" />


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
<img width="617" height="65" alt="image" src="https://github.com/user-attachments/assets/e1740fb3-d03e-48b0-8d2f-4f3abc84a576" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="657" height="92" alt="image" src="https://github.com/user-attachments/assets/cfbd39e0-edff-4bc7-b012-1859906869d2" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="657" height="83" alt="image" src="https://github.com/user-attachments/assets/548650b6-df7b-4d66-a1ae-9041ce4fd06f" />

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
<img width="661" height="43" alt="image" src="https://github.com/user-attachments/assets/86b79232-48fa-4f5a-9ec6-1202834d1958" />



grep hello newfile 
## OUTPUT
<img width="656" height="50" alt="image" src="https://github.com/user-attachments/assets/da087678-0c63-4c4b-add8-6ad3df66e0bd" />




grep -v hello newfile 
## OUTPUT
<img width="662" height="46" alt="image" src="https://github.com/user-attachments/assets/a1583148-6db8-43a4-a87c-b12db11b9a0a" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="743" height="67" alt="image" src="https://github.com/user-attachments/assets/8423351f-58f3-4bb5-b201-b7549a079094" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="781" height="42" alt="image" src="https://github.com/user-attachments/assets/7ae00792-b6a6-4057-bb70-e244d7302d77" />



grep -R ubuntu /etc
## OUTPUT
<img width="785" height="183" alt="image" src="https://github.com/user-attachments/assets/57174dee-4459-4f73-84c8-6df988897d54" />



grep -w -n world newfile   
## OUTPUT
<img width="785" height="70" alt="image" src="https://github.com/user-attachments/assets/f54770b4-d568-496e-a435-3464c84d2602" />


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
<img width="780" height="72" alt="image" src="https://github.com/user-attachments/assets/a61b9591-870e-4037-8e37-5749650462a1" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="785" height="73" alt="image" src="https://github.com/user-attachments/assets/155a2500-0c04-4434-be8e-73177f3bb2b4" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="781" height="72" alt="image" src="https://github.com/user-attachments/assets/6881bd93-51e5-4ac4-a742-cdf201dad0d2" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="769" height="40" alt="image" src="https://github.com/user-attachments/assets/2ac6a824-b153-4f02-b2d6-ca92cde7a5f1" />


egrep '(world$)' newfile 
## OUTPUT
<img width="780" height="70" alt="image" src="https://github.com/user-attachments/assets/2695f520-6d21-4dfa-a640-371fd21f4799" />


egrep '(World$)' newfile 
## OUTPUT
<img width="779" height="48" alt="image" src="https://github.com/user-attachments/assets/084af0b1-472f-4d01-8ea2-e2cbb2af0700" />



egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="775" height="90" alt="image" src="https://github.com/user-attachments/assets/178af9fc-9cd4-44fe-a757-ad56cdff7775" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="771" height="47" alt="image" src="https://github.com/user-attachments/assets/70b88559-e7ea-4676-91bd-e9ce48e47208" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="780" height="47" alt="image" src="https://github.com/user-attachments/assets/e2428164-3d62-40ee-9802-b635c9e93815" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="780" height="46" alt="image" src="https://github.com/user-attachments/assets/43d209a3-143e-4e83-8b5e-a7089690b553" />


egrep l{2} newfile
## OUTPUT

<img width="778" height="62" alt="image" src="https://github.com/user-attachments/assets/a3b31c3b-45e7-455d-9fe5-855ca7988b88" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="782" height="93" alt="image" src="https://github.com/user-attachments/assets/f305b44a-e72f-4cee-9277-31e07e167767" />

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
<img width="816" height="28" alt="image" src="https://github.com/user-attachments/assets/861531a7-bb2a-46cc-b084-30fd4bf2cb3b" />



sed -n -e '$p' file23
## OUTPUT
<img width="813" height="33" alt="image" src="https://github.com/user-attachments/assets/cc69e635-be7a-41ad-9dac-14e2076f82ad" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="808" height="142" alt="image" src="https://github.com/user-attachments/assets/1064b00a-dff2-4d6d-8b91-922f3ce459a6" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="812" height="137" alt="image" src="https://github.com/user-attachments/assets/ac1209aa-da8d-45a3-80b2-b60f18b2be0c" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="950" height="169" alt="image" src="https://github.com/user-attachments/assets/2dfa91cb-0d6f-498f-a83d-8a51de5a896a" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="952" height="117" alt="image" src="https://github.com/user-attachments/assets/2362ce86-c33b-418a-89ff-f3a4570a40b0" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="951" height="78" alt="image" src="https://github.com/user-attachments/assets/4a9079ff-2f91-4353-91fb-5f54ab989b62" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="969" height="62" alt="image" src="https://github.com/user-attachments/assets/c1d7747e-234e-4a97-bffa-e823228b6a20" />


seq 10 
## OUTPUT
<img width="754" height="198" alt="image" src="https://github.com/user-attachments/assets/246d0ad9-df9d-45ff-bd20-ef23957f86ef" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="811" height="66" alt="image" src="https://github.com/user-attachments/assets/ee3f05d5-98ed-4321-9d47-a9c081beb019" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="892" height="76" alt="image" src="https://github.com/user-attachments/assets/25c492c2-8d93-46b7-a0c9-49fc778e5a1e" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="891" height="94" alt="image" src="https://github.com/user-attachments/assets/88395d8c-6852-4486-a39b-bcb56f559af6" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="890" height="82" alt="image" src="https://github.com/user-attachments/assets/ee94bbc1-689c-4d43-8d24-c4ae2561e239" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="910" height="80" alt="image" src="https://github.com/user-attachments/assets/da6b481e-e71d-4211-9e74-1e530c5bea6f" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="954" height="76" alt="image" src="https://github.com/user-attachments/assets/3c2ccbd1-8e81-462d-a899-c1bf30b1af37" />


sed -n '2,4{s/$/*/;p}' file23
<img width="954" height="76" alt="image" src="https://github.com/user-attachments/assets/9b0a8064-c399-4591-b46c-e1d0cf0a2555" />


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
<img width="796" height="112" alt="image" src="https://github.com/user-attachments/assets/0c6acb7b-1177-450d-922d-8e928b93b058" />


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
<img width="796" height="112" alt="image" src="https://github.com/user-attachments/assets/1614eb22-1769-4c90-bdee-f5ec48b0de21" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1006" height="169" alt="image" src="https://github.com/user-attachments/assets/f7f61a55-d400-4a15-afca-d87084db6383" />


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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


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
