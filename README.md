![Screenshot 2025-03-05 140813](https://github.com/user-attachments/assets/d6842e12-3320-4fba-a61d-7dffa8262bb1)Operating systems Lab exercise
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
![Screenshot 2025-03-05 140501](https://github.com/user-attachments/assets/67f5f3ca-4f19-4ca3-b7e1-ab2daddfc9c4)

cat < file2
## OUTPUT
![Screenshot 2025-03-05 140517](https://github.com/user-attachments/assets/41903d1f-9e17-4143-9818-21653597fb20)


# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot 2025-03-05 140527](https://github.com/user-attachments/assets/6813f36a-e514-4fa9-a21d-65014d4954e4)

comm file1 file2
 ## OUTPUT
 ![Screenshot 2025-03-05 140537](https://github.com/user-attachments/assets/7ef23786-2dc2-45f4-a301-031f683c9377)

diff file1 file2
## OUTPUT
![Screenshot 2025-03-05 140548](https://github.com/user-attachments/assets/2c9de9e7-9330-40ed-a35a-f5aac1a948ad)

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
![Screenshot 2025-03-05 140623](https://github.com/user-attachments/assets/fd29173b-1e9f-4c81-877d-1461f1c3ad90)

cut -d "|" -f 1 file22
## OUTPUT
![Screenshot 2025-03-05 140631](https://github.com/user-attachments/assets/e1283b68-5f60-4c20-8b63-ebc6cfccf887)

cut -d "|" -f 2 file22
## OUTPUT
![Screenshot 2025-03-05 140643](https://github.com/user-attachments/assets/764456e8-4c36-4129-8198-e46f7c6dc71d)



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
![Screenshot 2025-03-05 140653](https://github.com/user-attachments/assets/101ac4bf-c24b-44ef-ab5f-f74480a386b6)

grep hello newfile 
## OUTPUT
![Screenshot 2025-03-05 140701](https://github.com/user-attachments/assets/0b83bbe6-1284-4fa7-854e-13816e3de921)

grep -v hello newfile 
## OUTPUT
![Screenshot 2025-03-05 140711](https://github.com/user-attachments/assets/8e17ad2d-6015-4951-9305-c6e248c7b4b1)

cat newfile | grep -i "hello"
## OUTPUT
![Screenshot 2025-03-05 140725](https://github.com/user-attachments/assets/650addbc-f316-42fc-8194-c44783dde982)

cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot 2025-03-05 140739](https://github.com/user-attachments/assets/db50e75c-402b-4c93-93ce-a885270454d3)

grep -R ubuntu /etc
## OUTPUT
![Screenshot 2025-03-05 140752](https://github.com/user-attachments/assets/9475c465-0765-4f64-81bc-34bab45de4be)

grep -w -n world newfile   
## OUTPUT
![Screenshot 2025-03-05 140803](https://github.com/user-attachments/assets/d7897809-d7a3-4704-884f-05ec43e33639)


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
![Screenshot 2025-03-05 140813](https://github.com/user-attachments/assets/b166755b-fbb4-426a-a298-f0dab5c82c59)

egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot 2025-03-05 140821](https://github.com/user-attachments/assets/a3e62bac-0063-48e4-a7ef-c2e82ece93de)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot 2025-03-05 140831](https://github.com/user-attachments/assets/6dbbd7ba-9675-44ef-a998-dc2ec5d62d1c)

egrep '(^hello)' newfile 
## OUTPUT
![Screenshot 2025-03-05 140843](https://github.com/user-attachments/assets/c8d2c3cf-0f14-45e1-80ef-ac704dc23037)


egrep '(world$)' newfile 
## OUTPUT
![Screenshot 2025-03-05 140853](https://github.com/user-attachments/assets/f6136dad-ad5b-4c5d-aaf5-30690971bbcc)

egrep '(World$)' newfile 
## OUTPUT
![Screenshot 2025-03-05 140903](https://github.com/user-attachments/assets/7b2deabf-888a-42eb-ab8c-a021d7e1391d)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot 2025-03-05 140911](https://github.com/user-attachments/assets/d17196c9-47bd-43cd-8396-d95546594ce9)

egrep '[1-9]' newfile 
## OUTPUT
![Screenshot 2025-03-05 140921](https://github.com/user-attachments/assets/79e2b562-4bc4-499c-99dc-6664cdba7ad7)

egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot 2025-03-05 140931](https://github.com/user-attachments/assets/af58b230-c2a1-4805-98f8-764dadd370e4)

egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot 2025-03-05 140938](https://github.com/user-attachments/assets/eb16c5d7-8802-439b-adf7-455d8a626403)

egrep l{2} newfile
## OUTPUT
![Screenshot 2025-03-05 140946](https://github.com/user-attachments/assets/35ca75ed-9d8f-4e08-9fab-d3b8aec9562b)

egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot 2025-03-05 140955](https://github.com/user-attachments/assets/4aa3dc96-0726-43b1-93fd-3b8a15f598cf)


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
![Screenshot 2025-03-05 141003](https://github.com/user-attachments/assets/8a18dec8-f53f-44fb-8b22-6769300da2b9)



sed -n -e '$p' file23
## OUTPUT
![Screenshot 2025-03-05 141014](https://github.com/user-attachments/assets/fecdb9bf-9540-4775-8eca-e4a565650e5c)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot 2025-03-05 141023](https://github.com/user-attachments/assets/f78110f0-6ffb-47fb-a8bf-587a68854388)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot 2025-03-05 141030](https://github.com/user-attachments/assets/8783bdca-b3af-4cb4-81ca-47e927e08b4a)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot 2025-03-05 141038](https://github.com/user-attachments/assets/787123c6-84f1-45e1-ba56-11b2649ebfc9)

sed -n -e '1,5p' file23
## OUTPUT
![Screenshot 2025-03-05 141046](https://github.com/user-attachments/assets/725d81b4-436e-4844-924c-264af5444205)

sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot 2025-03-05 141053](https://github.com/user-attachments/assets/4cb44906-bbf9-40cb-86a5-1c8307fcf3b5)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot 2025-03-05 141105](https://github.com/user-attachments/assets/26ad498e-a988-443c-b12e-9d80a3aa990c)

seq 10 
## OUTPUT
![Screenshot 2025-03-05 141116](https://github.com/user-attachments/assets/d0cae2f1-a598-4ccc-8f01-b9ab044a1e76)

seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot 2025-03-05 141126](https://github.com/user-attachments/assets/dc4fbca0-5944-4396-934a-611ecbccf0c6)

seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot 2025-03-05 141136](https://github.com/user-attachments/assets/ae831013-900f-4270-ac8e-0b0f6e5afc6f)

seq 3 | sed '2a hello'
## OUTPUT
![Screenshot 2025-03-05 141145](https://github.com/user-attachments/assets/7dafa838-cc00-4dc0-b019-2bff7c870cc9)



seq 2 | sed '2i hello'
## OUTPUT

![Screenshot 2025-03-05 141153](https://github.com/user-attachments/assets/77ac0e07-06ef-4a6e-966e-09c1e53c7481)

seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot 2025-03-05 141202](https://github.com/user-attachments/assets/90aa73f8-3af8-425c-89d9-46a4b54124b7)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot 2025-03-05 141210](https://github.com/user-attachments/assets/53e7a535-7ba1-4e93-b112-3449a7ea5baf)



sed -n '2,4{s/$/*/;p}' file23


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
![Screenshot 2025-03-05 141219](https://github.com/user-attachments/assets/bd607a4a-88f3-4e85-9d6e-17c2fe26390d)


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
![Screenshot 2025-03-05 141231](https://github.com/user-attachments/assets/a90128be-fb0e-4599-a89a-8a5768126e54)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot 2025-03-05 141243](https://github.com/user-attachments/assets/47e49642-8088-40e6-ae90-922d9d1ae632)

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

![Screenshot 2025-03-05 141252](https://github.com/user-attachments/assets/81a3bebf-4f1d-4950-8962-171badf17d70)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


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
