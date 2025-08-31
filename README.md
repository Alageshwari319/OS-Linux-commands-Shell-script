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

<img width="499" height="113" alt="image" src="https://github.com/user-attachments/assets/cfd3d94e-071d-43ec-b5ef-4d7a8999c61b" />




cat < file2
## OUTPUT

<img width="503" height="129" alt="image" src="https://github.com/user-attachments/assets/aa8fa28f-128a-4e9a-b352-d99519235d40" />



# Comparing Files
cmp file1 file2
## OUTPUT

<img width="559" height="43" alt="image" src="https://github.com/user-attachments/assets/65713c39-2c62-4136-a8f8-0f88cdd1f7d0" />

 
comm file1 file2
 ## OUTPUT

 <img width="567" height="240" alt="image" src="https://github.com/user-attachments/assets/44ce5aeb-714b-4366-9e8d-b06826316e8c" />


 
diff file1 file2
## OUTPUT
<img width="567" height="186" alt="image" src="https://github.com/user-attachments/assets/a0ebd376-dc01-4b7c-9e7f-c8550f44ea83" />


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

<img width="563" height="77" alt="image" src="https://github.com/user-attachments/assets/8224d5e0-6927-488f-9e76-5fc870c367a7" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="624" height="99" alt="image" src="https://github.com/user-attachments/assets/5e0abb6a-d3ce-49f1-8e62-b94413f8893e" />




cut -d "|" -f 2 file22
## OUTPUT

<img width="617" height="94" alt="image" src="https://github.com/user-attachments/assets/c368afa3-28b1-45a0-bca0-5ec7b86337c0" />



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

<img width="507" height="43" alt="image" src="https://github.com/user-attachments/assets/32e19566-8a2c-43d7-ac47-c3e6ed613390" />


grep hello newfile 
## OUTPUT

<img width="505" height="43" alt="image" src="https://github.com/user-attachments/assets/5e3e56b1-7240-4504-958f-0d419bd21a24" />



grep -v hello newfile 
## OUTPUT

<img width="535" height="41" alt="image" src="https://github.com/user-attachments/assets/325da536-ff0a-41db-a850-e5f10d22c992" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="606" height="62" alt="image" src="https://github.com/user-attachments/assets/2e78b7b3-31ce-4e9d-8919-8dbbc8ee279c" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="635" height="43" alt="image" src="https://github.com/user-attachments/assets/a2658104-df2b-4ad9-9b14-7a04f4248579" />


grep -R ubuntu /etc
## OUTPUT

<img width="1859" height="743" alt="image" src="https://github.com/user-attachments/assets/8fb62f75-a264-44e1-a5f1-c24aa11d630a" />


grep -w -n world newfile   
## OUTPUT
<img width="567" height="57" alt="image" src="https://github.com/user-attachments/assets/ad9eb24e-829e-4349-9c54-5167f56b0a6d" />


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

<img width="620" height="60" alt="image" src="https://github.com/user-attachments/assets/32a64763-aaf5-46bb-8e76-1684f897034f" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="604" height="60" alt="image" src="https://github.com/user-attachments/assets/98688175-bfc5-4d47-bf7a-f941a6282a2a" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="640" height="61" alt="image" src="https://github.com/user-attachments/assets/01864ba1-88c6-4a59-97ca-4d64f6c74cdb" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="592" height="42" alt="image" src="https://github.com/user-attachments/assets/9fbcb8d7-b611-4151-84a0-109b70e39ac9" />


egrep '(world$)' newfile 
## OUTPUT

<img width="567" height="59" alt="image" src="https://github.com/user-attachments/assets/4791c7c5-9244-4870-ad3e-0bb70af5c105" />


egrep '(World$)' newfile 
## OUTPUT

<img width="566" height="45" alt="image" src="https://github.com/user-attachments/assets/3eb58f50-5dc2-49f6-a7b8-9631d5c1fa03" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="601" height="58" alt="image" src="https://github.com/user-attachments/assets/dd8a055e-3760-484a-a3e8-a2d5fe0ee820" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="540" height="40" alt="image" src="https://github.com/user-attachments/assets/2e327eba-3032-4cc9-b536-bd0adb9a6e42" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="604" height="42" alt="image" src="https://github.com/user-attachments/assets/034ac410-942e-4183-9916-ea81350c6576" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="604" height="42" alt="image" src="https://github.com/user-attachments/assets/99f2b5e1-4496-42fb-9d06-360ce857a8f0" />


egrep l{2} newfile
## OUTPUT

<img width="515" height="57" alt="image" src="https://github.com/user-attachments/assets/5b14733a-e09a-4fe9-a971-fdf11d8ab19c" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="551" height="79" alt="image" src="https://github.com/user-attachments/assets/b3ef4db6-a719-4c0e-97ee-7307b5dfd998" />


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

<img width="540" height="40" alt="image" src="https://github.com/user-attachments/assets/15cdbfdf-9e3e-468b-b5ab-694e22a2a854" />


sed -n -e '$p' file23
## OUTPUT

<img width="533" height="39" alt="image" src="https://github.com/user-attachments/assets/6503ef93-6d40-4ce3-9b55-2a292cfa7105" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="590" height="187" alt="image" src="https://github.com/user-attachments/assets/c2eae6a6-de73-437b-890b-ea4a0a521bd8" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="599" height="183" alt="image" src="https://github.com/user-attachments/assets/2fc9e969-4911-47af-81b9-51dbfb9b4f70" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="619" height="186" alt="image" src="https://github.com/user-attachments/assets/deddaad9-c7b9-4857-b74e-b793095f8c9f" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="556" height="113" alt="image" src="https://github.com/user-attachments/assets/99e93fc0-bb29-4c50-9b28-4ea82d735e4b" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="591" height="81" alt="image" src="https://github.com/user-attachments/assets/98eb9925-2e62-4c87-9fcb-99b7f37185b8" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="619" height="60" alt="image" src="https://github.com/user-attachments/assets/68c47777-00e1-40b6-a607-1cd15eb32767" />


seq 10 
## OUTPUT

<img width="402" height="200" alt="image" src="https://github.com/user-attachments/assets/909cfc42-ede2-411d-92a2-29e361768885" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="542" height="82" alt="image" src="https://github.com/user-attachments/assets/e859e0a4-4010-4561-9a5c-6a1a6089c4e9" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="544" height="76" alt="image" src="https://github.com/user-attachments/assets/4028d8aa-8a2f-49ab-abfe-e3199b99664b" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="544" height="98" alt="image" src="https://github.com/user-attachments/assets/264d0e37-23fb-45d1-a3b0-219b36076cfa" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="545" height="80" alt="image" src="https://github.com/user-attachments/assets/2549cfd8-5ef7-4c0a-a4ec-a1f262ea3a19" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="571" height="80" alt="image" src="https://github.com/user-attachments/assets/1f2e25a0-439d-4074-9fc6-332f42465673" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="608" height="80" alt="image" src="https://github.com/user-attachments/assets/c78e9d3b-d9c1-4dfa-a3e2-48d9ac256137" />


sed -n '2,4{s/$/*/;p}' file23

<img width="604" height="77" alt="image" src="https://github.com/user-attachments/assets/fd5ff0c7-adc1-4aa1-8854-af8abcda2ad5" />


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

<img width="445" height="116" alt="image" src="https://github.com/user-attachments/assets/28dbe2e7-d0cf-47ad-9fb7-a7e236c18fd9" />


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

<img width="445" height="115" alt="image" src="https://github.com/user-attachments/assets/a372ed7a-b34e-4600-a763-3d02347fd0c7" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="656" height="184" alt="image" src="https://github.com/user-attachments/assets/ce9d3038-be10-4b42-a3c3-699a9dda0597" />


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
