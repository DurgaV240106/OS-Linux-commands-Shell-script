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

![Screenshot 2025-04-29 225110](https://github.com/user-attachments/assets/12762a98-046c-4af7-9e7a-c59efdf2c8cf)




cat < file2
## OUTPUT

![image](https://github.com/user-attachments/assets/11d113b9-b4ad-41fc-91ea-5e43cf1dba89)


# Comparing Files
cmp file1 file2
## OUTPUT

 ![image](https://github.com/user-attachments/assets/5e2ec1cc-0cee-451a-8cd7-ca1e44b26a7d)

comm file1 file2
 ## OUTPUT

![image](https://github.com/user-attachments/assets/2c9e2255-6446-4fc7-b6ee-e1a76b4ab8c9)

 
diff file1 file2
## OUTPUT

![image](https://github.com/user-attachments/assets/157643cd-7ecd-48fc-a972-c3a7cc62a233)


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

![image](https://github.com/user-attachments/assets/7496f541-2c5e-4e0b-83cd-04fcb0b9dc6b)




cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/17d13d28-f78a-4f55-9cc5-9bb732af8006)



cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/d941260a-d553-4f9f-a543-c7998d384b84)


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

![image](https://github.com/user-attachments/assets/a9e01650-db7a-4d16-8cea-f58391d0b6d6)



grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/c386468d-f860-47ce-bc4c-6af7ddb98808)




grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/5906b56a-152d-4ce3-af01-8bdbff1f7f5e)



cat newfile | grep -i "hello"
## OUTPUT



![image](https://github.com/user-attachments/assets/7122b5e0-9911-41f2-bd7a-3ad4fff7a579)


cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/5de1f522-688d-41ee-893f-9dcb0a67f2a5)




grep -R ubuntu /etc
## OUTPUT


![image](https://github.com/user-attachments/assets/30faddd1-c0e4-45b8-be14-ef03ce8f018c)


grep -w -n world newfile   
## OUTPUT

![image](https://github.com/user-attachments/assets/d4ce4b16-f576-4739-98d2-5b7bd3d5461f)


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

![image](https://github.com/user-attachments/assets/74e4aacf-0ff9-4203-8f87-17c8dd14d45e)



egrep -w '(H|h)ello' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/4dc347d9-7a60-4a24-a679-d02582a07682)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/ca0ee9c2-f5ef-4d05-a89e-618de74a22cb)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/a78db45f-d2ac-40d7-b015-0360c40b4de5)



egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/d710522f-3743-4b88-ad24-37e4d4767920)



egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/1e1318f8-f5ca-4a39-a7d8-f66a45323cbe)


egrep '((W|w)orld$)' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/e6d2e531-ce69-4407-99e0-ae3364a0fdf6)


egrep '[1-9]' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/d365b404-251d-434c-b251-7abcb0bb7264)


egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/8fc430bd-4b95-4f01-9432-ed3d89a6c1d0)


egrep 'Linux.*World' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/b0de5419-238f-4f5b-8b48-ffd04d0c0f97)

egrep l{2} newfile
## OUTPUT


![image](https://github.com/user-attachments/assets/11f5a6ed-75ef-41cb-8cbc-7b9f046caf41)


egrep 's{1,2}' newfile
## OUTPUT 


![image](https://github.com/user-attachments/assets/c65e3491-da84-4cc4-bab6-cbcb8e79e7ed)

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

![image](https://github.com/user-attachments/assets/06de5f86-269f-4525-b35b-337ce26b788c)



sed -n -e '$p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/6188db3f-7688-47ad-9f4c-a958c4dbf410)


sed  -e 's/Ram/Sita/' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/6d3ddac3-63aa-42ff-8b4e-a9966855a05a)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/d32c2d96-e2e1-46a5-bb4a-03b2aca726ca)



sed  '/tom/s/5000/6000/' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/10299ac3-fcef-4774-8910-6ed596dcbe19)


sed -n -e '1,5p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/5128b058-6317-47b9-8e9d-4954b1906879)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/d4028180-bfed-41ec-8f7c-c446a9b2df85)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/c9a233b4-cfe6-49b0-8da1-7080bc99850e)


seq 10 
## OUTPUT


![image](https://github.com/user-attachments/assets/a6fe6af2-e08e-4222-b890-038b1a89fb31)


seq 10 | sed -n '4,6p'
## OUTPUT


![image](https://github.com/user-attachments/assets/b0efcfbf-a095-4afe-8124-aad79ae284f1)


seq 10 | sed -n '2,~4p'
## OUTPUT


![image](https://github.com/user-attachments/assets/f18a17d5-13fc-4a89-9b8a-ee8c2d6e8fd4)


seq 3 | sed '2a hello'
## OUTPUT


![image](https://github.com/user-attachments/assets/6f09b9bd-3a97-4a00-b82f-a74787d5eb9b)


seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/34ebfcba-4aab-4a78-82b8-21f3082e381d)


seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/c98b26a1-3300-4014-9abf-89a56429a8e8)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/ab939b87-de21-4cf0-b8f8-05754fdd4171)



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

![image](https://github.com/user-attachments/assets/894d6be0-133e-495e-87bb-83e536582a7f)


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


![image](https://github.com/user-attachments/assets/39c29b97-eb90-4ae9-b8d8-2c2e2a3df189)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![image](https://github.com/user-attachments/assets/10386328-e8b5-4094-a706-907a1e830790)

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

![image](https://github.com/user-attachments/assets/b3621dd1-82e4-402a-a738-263e5c76bef1)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


![image](https://github.com/user-attachments/assets/fef1edb4-05d5-4372-b845-fad1f50f91a3)


#Backup commands
tar -cvf backup.tar *
## OUTPUT


![image](https://github.com/user-attachments/assets/5f34d549-5082-4f09-ac67-1fe17712b5bb)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/6d0d1504-c434-4e31-9a73-c4b344261824)


tar -xvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/e19bc244-388d-44dc-9ede-cb550464b490)

gzip backup.tar

ls .gz
## OUTPUT

 ![image](https://github.com/user-attachments/assets/0e5bcf10-ff8e-467b-b519-f1ff60386653)

gunzip backup.tar.gz
## OUTPUT

![image](https://github.com/user-attachments/assets/b05ecf96-cf82-4f7b-9461-df66b4257c36)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![image](https://github.com/user-attachments/assets/756a8616-c3b8-4102-baa5-b3900070f858)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/user-attachments/assets/d8371e29-304f-4a80-930e-c6ea2ddb9abe)


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

![image](https://github.com/user-attachments/assets/2eec0e15-d8f0-4a79-9946-315b5610a613)

 
ls file1
## OUTPUT

![image](https://github.com/user-attachments/assets/67a18a28-ef36-4824-93c2-4eb4414dd429)

echo $?
## OUTPUT 


![image](https://github.com/user-attachments/assets/1ed75581-4621-45a2-86c5-890c61cdcb27)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 ![image](https://github.com/user-attachments/assets/a0e9914c-6d08-45c3-bc8a-e7e4dfa12f40)

abcd
 
echo $?
 ## OUTPUT

![image](https://github.com/user-attachments/assets/7131c821-4802-40be-94d5-38c75b521222)


 
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


![image](https://github.com/user-attachments/assets/bc605c54-3e18-482c-8495-8e9562e7a2a9)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/30ab082c-a4d9-4d4f-b62c-0bef87c1d69e)


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

![image](https://github.com/user-attachments/assets/f9da1f82-aac8-4b5a-afbe-fd6c47ebb75b)

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

![image](https://github.com/user-attachments/assets/5da6329c-1a0e-4818-8ce5-6b8eadf3b03f)


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

![image](https://github.com/user-attachments/assets/3521b063-20fa-41e5-bf65-c7c0f1adb4c2)


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

![image](https://github.com/user-attachments/assets/7d9697f8-a09d-4fee-b8b0-3e2f1b5c9936)


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

![image](https://github.com/user-attachments/assets/70f1e36c-8bb0-4813-a6d7-f134ea45d389)

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

![image](https://github.com/user-attachments/assets/b14d06a6-d627-43a2-a728-dc8b6595d4a5)

 
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

![image](https://github.com/user-attachments/assets/735e5300-fb6b-4707-a8cd-279b5fde7239)

 
 
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
 

 ![image](https://github.com/user-attachments/assets/a90054e5-f7c9-411e-8f6b-352f2a75f0eb)

 
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
 

 ![image](https://github.com/user-attachments/assets/75bde3a5-c616-4c45-8a98-86bc34032993)

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

 ![image](https://github.com/user-attachments/assets/1e4832f7-7e35-4f0b-9ecf-48166fa6f0c9)

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

 ![image](https://github.com/user-attachments/assets/2b8c1273-4e15-46c3-82ea-d634ba5a5249)

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

![image](https://github.com/user-attachments/assets/eefee671-e679-43d6-a59a-9b3813c7f74d)

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
$ chmod 777 forinfile.


![image](https://github.com/user-attachments/assets/09e2d2b6-3728-4e1f-a673-88903feda1d4)


## OUTPUT


![image](https://github.com/user-attachments/assets/684d30e8-b853-4a83-aed7-dc8460d215a9)



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


![image](https://github.com/user-attachments/assets/4f51d204-7f6e-4ff6-af42-ec36bcb45eaf)

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


![image](https://github.com/user-attachments/assets/5c885e5b-06b0-4899-bad0-987dd77f3430)

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

![image](https://github.com/user-attachments/assets/8bbf4df6-58f1-4563-b157-e1550f89035d)

 
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


![image](https://github.com/user-attachments/assets/68d8b6ab-c7c5-427a-a461-0fda29c3c1e8)

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


 ![image](https://github.com/user-attachments/assets/7d1c1ec7-ba5a-4d35-885e-bf7e7afa76a7)

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



 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 





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


![image](https://github.com/user-attachments/assets/092882a1-0fda-407c-aa5e-8c0cd4ecbb5d)

 
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


![image](https://github.com/user-attachments/assets/c6303459-e8e4-49a5-855c-a84b4927e99d)

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

![image](https://github.com/user-attachments/assets/6937960b-62b2-4689-877f-a0924b8522be)

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


![image](https://github.com/user-attachments/assets/2e996fe8-77a4-4a4a-bcee-5d34a42f43ea)

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

 ![image](https://github.com/user-attachments/assets/cc9799c5-805c-4ec7-b7e5-8141d51ee1ad)

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

![image](https://github.com/user-attachments/assets/455eb1b9-069d-4959-99e2-55fdfcc26e39)


# RESULT:
The Commands are executed successfully.
