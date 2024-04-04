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
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat < file2
## OUTPUT
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
# Comparing Files
cmp file1 file2

## OUTPUT
![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/c32cdd90-73b6-483b-97b0-e4a6f3a4d0d5)


comm file1 file2

## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/abaef6fd-061e-4dae-a56d-fc68594c50d3)


 
diff file1 file2
![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/c6422844-1c6d-44f2-a662-c425b4761f63)

## OUTPUT


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


![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/3577e78c-4545-46cc-ad26-64d91c1822dd)


cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/cfa346f8-5a6f-4e68-8f27-6105c37c2a1d)


cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/1da5c5db-94db-4918-a9b6-a9508d92ead7)

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

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/494ce177-74b5-4085-86e4-b5ee2945d303)


grep hello newfile 
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/7be5efcc-b491-4ca1-ae8f-434215482af6)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/18d7b544-b956-4bab-8600-369c81506c56)


cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/c6f6b88b-6609-46f8-a8d4-e67aacadc0c3)




cat newfile | grep -i -c "hello"
## OUTPUT


![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/83980eae-3d90-4472-8b9a-c9bc6ae07a7e)


grep -R ubuntu /etc
## OUTPUT
grep -w -n world newfile   
## OUTPUT
![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/50c33527-9796-466b-9470-62514f11df66)


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

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/dd54be63-dd92-4ee9-a45e-1558af1328d1)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/af75726c-1861-44ce-9f7a-4b54c6ce87ac)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/1240e8f3-e63f-430d-ba22-e09405aa892a)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/7ec755a6-9aa9-4efa-8935-4682f0def7a3)


egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/59b3d8fb-90db-4fc6-aafb-bb80f5fda3b7)



egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/45e6c984-ccf7-4b15-af0d-0890127b22e5)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/a42eb899-27f7-4933-9492-b6f42973a2c8)



egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/e543658d-8b97-43e8-a0a7-c3906dd57749)


egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/c8098d1e-7083-409d-9a4e-b768546e4432)


egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/ba306c7d-f3bd-48ac-83e7-e40f1e52b9a8)

egrep l{2} newfile
## OUTPUT
![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/e5eb2379-f701-42fc-8b0c-3e69adf4639c)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/dc356ab9-dbcf-440b-a43e-d1e3c27f0e71)


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


![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/0ba5c6c9-b48e-460e-863a-9b7628ef5880)

sed -n -e '$p' file23
## OUTPUT



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/1e7e826d-0d2a-4545-9848-b2cc7842a413)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/11205bf4-a91e-4c0a-98fe-ad13d7ab78e3)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/8a55d44c-5486-4bc1-b4f0-09c599c1dbe8)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/96a705ea-5055-4926-8560-83f4ba0a9804)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/7fca69f5-210c-417d-8e06-d4c2b7e3d554)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/67e6fed3-6dcc-4460-bab1-a8cd0c151c29)


seq 10 
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/1db8a1bd-6246-46c9-bcca-952ac987ec30)


seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/1924b0fe-9a42-45fc-9479-89485624460a)


seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/de67f42d-87b8-43b3-8e02-9c1c8c601f72)



seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/52ef05f6-0658-4094-b793-0b190b4c9035)


seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/b092b1f8-0a65-4bee-842c-7a146c2b4a9c)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/61d03687-ea20-47f3-a694-dca99fad066e)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/9d890293-fadc-49f1-9217-42028528345b)


sed -n '2,4{s/$/*/;p}' file23

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/704aec87-30fa-46cd-b5df-315f79722b57)

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

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/cb724935-a403-4f41-a7ce-eb5aa5589cf2)

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
![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/72010175-fc60-4eda-bae3-4236adbb7daf)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/98eebb42-faca-4dab-94b3-e06be4f1abce)

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

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/8896a5b8-d074-44a6-b82c-6bd76874432a)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/9d710d38-4e3e-4562-bf65-df6bd2c4465a)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/23013753/OS-Linux-commands-Shell-script/assets/145634121/d1e757ac-0332-4cef-97ed-5c0f3546436f)


mkdir backupdir
 
mv backup.tar backupdir
 
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
```
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
