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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/f4f441e8-fe45-42de-8533-2ee2164b92e7)



cat < file2
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/e31724cf-c52b-4265-af1c-73923d2bc6c5)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/6e58cecb-0e1c-4456-99c6-71e7b334e8f6)

comm file1 file2
 ## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/bdd44293-158c-4121-8a53-6dad7791510e)

 
diff file1 file2
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/adbf3693-e25d-46a9-9839-ae5d59643b4f)


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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/3df29b25-07b4-4165-bf26-b008b6891f01)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/54c13e2c-5301-4c68-b7c9-3c0dab95601a)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/54bd2634-6365-4940-9946-14c720c2dbcf)


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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/60e19045-3e3a-4f37-949e-bb5137436faf)



grep hello newfile 
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/410e90aa-c708-4bc5-a7f4-c36a9ec139f6)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/3e54cfcb-d84e-40ac-8a68-d1bec1e93459)



cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/6ba0cc67-5860-4aa6-b86c-2b2261930ba0)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/6ef2f832-9d93-4259-bfc1-feb8ec5fc848)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/76822dbe-ddcd-49a4-8eac-88047b42b6b6)

![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/db8e06bf-c822-4680-9f2b-ca2184b5bb18)


grep -w -n world newfile   
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/ac48b55c-bf7f-43e1-ad17-a25a2dfb3caf)


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

![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/9c9c633e-32af-49b0-9e88-e8dbc55315ea)


egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/44e9e4b1-1567-488f-821b-0000ef7bf753)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/4d8deceb-0a0c-4a65-b965-7403659510aa)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/825d7e90-6280-4af5-a1ab-07319d0d6db6)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/ffc51a7a-c262-4ba6-8ee8-eaf8b2df40ca)



egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/5c4619e4-f23c-4317-87ca-b48d46954205)



egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/4d0de49a-e3dd-41ac-8137-35efd2f0e559)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/87b19c8d-b38d-481c-8f40-941025f694d8)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/82656920-8b9d-4376-9812-ff7ed4b5010d)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/aa2b293d-6e8e-4554-b0f4-a53ea241790b)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/1534d504-9d5f-478b-8580-9a30ae3c6e80)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/1d443944-7d45-47b3-b292-9b4ddba20cf3)


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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/7ae416e5-5e7b-48bf-aa26-1036d723312b)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/a5c97e59-eb61-4a25-b6c7-5e22bbf2b5c9)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/9684f0cf-4ff4-40bd-9a74-d92ab3eb2f30)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/66efa27a-34b6-44b0-a2af-905234d8b31e)




sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/1ee8c82f-ba34-4002-bbef-6fd533332887)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/f3798308-4512-4059-8dca-4a59225b6626)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/1bd84bb3-fd63-449e-b334-a2112a7ed3f1)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/7d5e90a9-e4ca-413e-b8d9-5275c32d7784)



seq 10 
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/b464e10d-ca8c-466e-ba5b-f21be241ee63)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/fe5bda72-c18f-4c80-b471-cba4442fb245)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/73be1499-5b53-4bad-934b-cf5d174b4530)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/e2f0a55b-693f-46e8-a842-7a7ed48f8068)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/28ff7bd5-d371-45b7-80f6-0c5a53b13c51)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/00fdca1e-fe99-4498-893c-e86bcc9e69bf)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/b461de48-2863-4135-b1b6-b2ae9436b84e)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/f92a544f-99b1-4edc-8a8a-885bb0443c5b)


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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/246708cc-a9f7-42a2-8ff2-1d626852b30d)


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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/b98e79bc-675a-4edb-a343-21dc95f1f931)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/6e4680c2-b0d0-4835-9a3f-45e9547fa641)

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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/1ea214e0-cead-411e-a86a-cb8c51bdcced)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/9d9802bf-aec1-47b9-a467-4accbe7452b5)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/7e2452ef-50f1-401d-bfae-9c0a72bc18dd)




 
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

![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/a3e90980-2088-4306-bc0f-f4216d8d8f21)



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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/acee37fe-ed08-402d-99d1-d0e492252cc6)

 
ls file1
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/e05536ed-4c42-4535-8bcb-fed70283b52d)

echo $?
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/08d15691-aba6-4678-9d4f-b5d79fa41fc3)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/1569c2b6-643c-43c0-961e-e2c97da66705)

abcd
 
echo $?
 ## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/05eb1f0e-155f-4ab3-b2ea-5d4adcbcb293)


 
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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/8f8b7dea-2a43-4b7f-a7f5-d0605209684b)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/29a1a99e-f329-4d55-8b97-af368ae7e9a0)


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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/3aca89ba-c020-46a8-b744-747bc890cb47)

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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/3faeb79a-5e6a-4955-97c2-22d363afbb4f)



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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/a4e9f9f5-b27d-4a74-b0cd-a68e23859430)


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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/77a6b8c4-0440-4f78-9d36-402da50706f1)

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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/a058ed0a-3997-41a7-976a-9c97dd828c7d)


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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/63ec19b4-4f9d-4887-bb66-cb3e99c6b8c5)

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
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/c3c97f14-3afb-443f-ac98-88f056a6eada)

 
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
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/549fb614-3a69-453c-8f58-3304916b7e6e)

 
 
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
## OUTPUT 
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/753a229b-4b19-43d3-9311-08c785e06b05)
 
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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/b29ef446-b7cf-4d9c-bb20-dbdeed08c3f6)

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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/c4693339-e7ca-43bd-a28b-c0851da7957f)
 
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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/9c8194b3-663b-47df-bd43-ed5a25ddb4a3)
 
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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/19022ec9-2684-4bc5-ae26-2c4b7c435dfb)

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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/a84b37e4-6a49-4c78-9f09-0adf69c71570)


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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/95ab7f07-eb68-4a07-8431-9f7b963db62d)

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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/3b30f14f-1b65-4045-848a-54cb21690e56)

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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/009312d3-ccba-42df-9b02-c9441ba9a861)

 
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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/e5cf19da-7ec5-437e-9501-6774f2a04af5)


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
./funcex.sh 

 
./funcex.sh 1 2
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/a283ee5a-7dbc-453b-b8ab-8d0c8aa031e4)

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh


$ ./argshift.sh 1 2 3
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/bd16c986-14fb-479e-a36d-0657db72c771)

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

$ ./argshift.sh 1 2 3
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/3818bb5d-3033-4ca9-b4b4-2b2c1071f07a)
 
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
./argshift.sh 1 2 3
## OUTPUT
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/a6060bf0-ebc4-4459-bcec-61ae8eef5173)

 
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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/fb78dbc9-77e7-468a-8526-cf8de2c7f7d1)
 
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
![image](https://github.com/Kesavasai20/OS-Linux-commands-Shell-script/assets/138849303/06c274e2-2ca8-4873-b230-35de9be99e30)


# RESULT:
The Commands are executed successfully.
