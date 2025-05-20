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

<img width="595" alt="Screenshot 2025-05-20 at 10 26 15 AM" src="https://github.com/user-attachments/assets/9aae2695-3ab9-4343-b000-809e76b3c6c8" />


cat < file2
## OUTPUT
<img width="437" alt="Screenshot 2025-05-20 at 10 26 23 AM" src="https://github.com/user-attachments/assets/4486b379-9ee0-462f-a89d-faed239667cd" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="462" alt="Screenshot 2025-05-20 at 10 26 30 AM" src="https://github.com/user-attachments/assets/45fa51e7-8fe8-4e98-97e1-29f58e149970" />

comm file1 file2
 ## OUTPUT
<img width="461" alt="Screenshot 2025-05-20 at 10 26 37 AM" src="https://github.com/user-attachments/assets/1fc334a9-bff7-42ff-9f21-36de9d59b14d" />

 
diff file1 file2
## OUTPUT
<img width="456" alt="Screenshot 2025-05-20 at 10 26 44 AM" src="https://github.com/user-attachments/assets/3420257a-8801-4e98-94c6-79b9d7e09bed" />


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

<img width="454" alt="Screenshot 2025-05-20 at 10 26 51 AM" src="https://github.com/user-attachments/assets/1f8ac47d-87d6-46d8-b911-1ee90d34cfa6" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="515" alt="Screenshot 2025-05-20 at 10 27 08 AM" src="https://github.com/user-attachments/assets/2e391178-478b-4e58-9aad-537069062960" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="540" alt="Screenshot 2025-05-20 at 10 27 15 AM" src="https://github.com/user-attachments/assets/393165f8-3496-4e30-b638-e5edf9b5d96c" />


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

<img width="523" alt="Screenshot 2025-05-20 at 10 27 29 AM" src="https://github.com/user-attachments/assets/85c8be31-7761-43a9-adc8-c5eaaaa0cb25" />


grep hello newfile 
## OUTPUT
<img width="556" alt="Screenshot 2025-05-20 at 10 27 52 AM" src="https://github.com/user-attachments/assets/add6c7dd-2f9c-4397-9eb9-5e1efb26820e" />




grep -v hello newfile 
## OUTPUT

<img width="784" alt="Screenshot 2025-05-20 at 10 28 06 AM" src="https://github.com/user-attachments/assets/7991291c-1568-42e4-a722-c46e5f6eea16" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="566" alt="Screenshot 2025-05-20 at 10 28 16 AM" src="https://github.com/user-attachments/assets/b58de5f5-0076-463b-8a2c-ba44778a1dd4" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="561" alt="Screenshot 2025-05-20 at 10 28 25 AM" src="https://github.com/user-attachments/assets/5631cac9-fe52-478e-815a-c56e84b5a145" />



grep -R ubuntu /etc
## OUTPUT
<img width="556" alt="Screenshot 2025-05-20 at 10 28 36 AM" src="https://github.com/user-attachments/assets/e5aaa395-c9dd-40c3-af3c-fa281213a78b" />



grep -w -n world newfile   
## OUTPUT
<img width="558" alt="Screenshot 2025-05-20 at 10 28 48 AM" src="https://github.com/user-attachments/assets/1e410209-8913-4d9c-881c-b1f59bca3b66" />


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

<img width="557" alt="Screenshot 2025-05-20 at 10 28 57 AM" src="https://github.com/user-attachments/assets/cc84b994-af21-4718-bde5-6ae1f6840079" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="569" alt="Screenshot 2025-05-20 at 10 29 04 AM" src="https://github.com/user-attachments/assets/6c9bf7d2-d95a-42f2-a6ac-6e8f68f9d441" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="574" alt="Screenshot 2025-05-20 at 10 29 55 AM" src="https://github.com/user-attachments/assets/cfc8326d-2141-478d-b6b0-ecb596140946" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="575" alt="Screenshot 2025-05-20 at 10 30 01 AM" src="https://github.com/user-attachments/assets/084369e2-aeda-469b-b446-59d2a60cd89e" />


egrep '(world$)' newfile 
## OUTPUT

<img width="580" alt="Screenshot 2025-05-20 at 10 30 09 AM" src="https://github.com/user-attachments/assets/e72eb6a3-4247-4f37-88f2-2a6ca4c29fb7" />


egrep '(World$)' newfile 
## OUTPUT

<img width="583" alt="Screenshot 2025-05-20 at 10 30 43 AM" src="https://github.com/user-attachments/assets/e8ea6669-bf9a-48ee-9177-a48699f822f8" />

egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="581" alt="Screenshot 2025-05-20 at 10 30 50 AM" src="https://github.com/user-attachments/assets/eb0b152a-98d9-4be0-a47c-e072ce544755" />

egrep '[1-9]' newfile 
## OUTPUT

<img width="580" alt="Screenshot 2025-05-20 at 10 30 56 AM" src="https://github.com/user-attachments/assets/63bba74d-fca8-4c0c-a114-69063663af2d" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="594" alt="Screenshot 2025-05-20 at 10 31 02 AM" src="https://github.com/user-attachments/assets/ff106c2b-c266-4beb-975e-81f9f9bd7a6c" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="573" alt="Screenshot 2025-05-20 at 10 31 09 AM" src="https://github.com/user-attachments/assets/c2748737-4090-4506-8c34-4137dfa31047" />


egrep l{2} newfile
## OUTPUT

<img width="580" alt="Screenshot 2025-05-20 at 10 31 31 AM" src="https://github.com/user-attachments/assets/7bddb990-c567-4991-9085-c28fef6fb594" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="624" alt="Screenshot 2025-05-20 at 10 31 37 AM" src="https://github.com/user-attachments/assets/16b7aa3f-c0df-4e2d-8ac4-c630b7127c74" />


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
<img width="617" alt="Screenshot 2025-05-20 at 10 31 43 AM" src="https://github.com/user-attachments/assets/6fc850ec-c13c-41fe-b03a-1aaafd14e7a2" />



sed -n -e '$p' file23
## OUTPUT

<img width="618" alt="Screenshot 2025-05-20 at 10 31 49 AM" src="https://github.com/user-attachments/assets/bac020f5-1a56-48ed-bad6-d5301eff4660" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="628" alt="Screenshot 2025-05-20 at 10 31 55 AM" src="https://github.com/user-attachments/assets/84840706-41ef-46ca-b913-29c969d9182a" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="639" alt="Screenshot 2025-05-20 at 10 32 01 AM" src="https://github.com/user-attachments/assets/4dbc95e6-c808-4706-a365-28f86a171db8" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="634" alt="Screenshot 2025-05-20 at 10 32 07 AM" src="https://github.com/user-attachments/assets/b67a511f-d2a7-4c1e-8277-cae74a2b9089" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="626" alt="Screenshot 2025-05-20 at 10 32 14 AM" src="https://github.com/user-attachments/assets/51ec2151-ea5b-437f-bb5d-1d9dca51882b" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="639" alt="Screenshot 2025-05-20 at 10 32 20 AM" src="https://github.com/user-attachments/assets/6401ed85-33e5-41d8-aa87-b88d39501795" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="651" alt="Screenshot 2025-05-20 at 10 32 25 AM" src="https://github.com/user-attachments/assets/d5173f23-c466-4054-94b4-9b0754b7950f" />


seq 10 
## OUTPUT

<img width="638" alt="Screenshot 2025-05-20 at 10 32 31 AM" src="https://github.com/user-attachments/assets/071ef6ef-221b-42bc-88ea-359804651a45" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="649" alt="Screenshot 2025-05-20 at 10 32 36 AM" src="https://github.com/user-attachments/assets/05a54984-2008-4b42-a569-c94e33483963" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="647" alt="Screenshot 2025-05-20 at 10 32 41 AM" src="https://github.com/user-attachments/assets/7af3d465-a060-42e9-9d7b-b4614000c03c" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="632" alt="Screenshot 2025-05-20 at 10 32 49 AM" src="https://github.com/user-attachments/assets/a1c771f5-2f8e-431b-95dd-ef6dbeb2e975" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="649" alt="Screenshot 2025-05-20 at 10 33 12 AM" src="https://github.com/user-attachments/assets/b677dff9-3b26-4588-9cc9-eedb2d6a90ee" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="664" alt="Screenshot 2025-05-20 at 10 33 19 AM" src="https://github.com/user-attachments/assets/41f0cee7-b15d-4b5c-af1f-0ca38f712bc1" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="596" alt="Screenshot 2025-05-20 at 10 33 30 AM" src="https://github.com/user-attachments/assets/b46eb0ce-810d-40c2-a2cf-175dc565dbe8" />


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
<img width="600" alt="Screenshot 2025-05-20 at 10 33 36 AM" src="https://github.com/user-attachments/assets/abb47a71-9b85-4609-b7c8-a6981c366897" />


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
<img width="615" alt="Screenshot 2025-05-20 at 10 33 43 AM" src="https://github.com/user-attachments/assets/8555ead2-1cb5-4865-be2f-f44f94e4fdf1" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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

<img width="653" alt="Screenshot 2025-05-20 at 10 33 49 AM" src="https://github.com/user-attachments/assets/9998a730-394b-46ab-b1c9-108b01c912a3" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="801" alt="Screenshot 2025-05-20 at 10 34 02 AM" src="https://github.com/user-attachments/assets/95b2b16c-9f3c-49b4-b0a9-7733ba7acc04" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="798" alt="Screenshot 2025-05-20 at 10 34 11 AM" src="https://github.com/user-attachments/assets/916c899d-1723-4e90-8413-043cc92b2d5e" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="835" alt="Screenshot 2025-05-20 at 10 34 39 AM" src="https://github.com/user-attachments/assets/233b5993-852d-451b-9d59-0bc192e5b894" />


tar -xvf backup.tar
## OUTPUT
<img width="825" alt="Screenshot 2025-05-20 at 10 34 48 AM" src="https://github.com/user-attachments/assets/9861b31b-01f7-4a2c-80e6-ba83d633e0ff" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="827" alt="Screenshot 2025-05-20 at 10 34 55 AM" src="https://github.com/user-attachments/assets/5507750d-39f1-46bd-88e2-1e6ec73eb50a" />

gunzip backup.tar.gz
## OUTPUT
<img width="833" alt="Screenshot 2025-05-20 at 10 35 02 AM" src="https://github.com/user-attachments/assets/1348f911-becf-4c96-9802-67794a1eb5bf" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="826" alt="Screenshot 2025-05-20 at 10 35 09 AM" src="https://github.com/user-attachments/assets/2c6c1b8d-b426-4e9c-af25-3557349efe09" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="825" alt="Screenshot 2025-05-20 at 10 35 18 AM" src="https://github.com/user-attachments/assets/27267811-61e8-4ce4-a34a-49f1be93a33f" />


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
<img width="815" alt="Screenshot 2025-05-20 at 10 35 27 AM" src="https://github.com/user-attachments/assets/f865bae0-44cf-4f40-aac5-656ae0c9f516" />

 
ls file1
## OUTPUT
<img width="807" alt="Screenshot 2025-05-20 at 10 35 33 AM" src="https://github.com/user-attachments/assets/b57761bd-004e-499c-b3ca-f27905369c6f" />

echo $?
## OUTPUT 
<img width="817" alt="Screenshot 2025-05-20 at 10 35 40 AM" src="https://github.com/user-attachments/assets/390f55d1-b5d3-450c-b1d3-26aa6429e81a" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="825" alt="Screenshot 2025-05-20 at 10 35 48 AM" src="https://github.com/user-attachments/assets/0182e18a-3628-4427-b588-8a2a052726e8" />

abcd
 
echo $?
 ## OUTPUT
<img width="818" alt="Screenshot 2025-05-20 at 10 35 53 AM" src="https://github.com/user-attachments/assets/22af6425-3041-431f-a03d-c2f0a6510a7b" />


 
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
<img width="764" alt="Screenshot 2025-05-20 at 10 36 01 AM" src="https://github.com/user-attachments/assets/56bd166a-5215-481d-b8d3-ac6dc2cf6d01" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="818" alt="Screenshot 2025-05-20 at 10 36 11 AM" src="https://github.com/user-attachments/assets/62cf2996-d13b-4645-8124-dd7c522a5072" />


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
<img width="794" alt="Screenshot 2025-05-20 at 10 36 20 AM" src="https://github.com/user-attachments/assets/9df14452-70f1-49a7-b192-bc5322659cf7" />

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
<img width="809" alt="Screenshot 2025-05-20 at 10 36 27 AM" src="https://github.com/user-attachments/assets/2b9abac8-546e-4cd7-9d81-5b51d68cb16f" />



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
<img width="790" alt="Screenshot 2025-05-20 at 10 36 36 AM" src="https://github.com/user-attachments/assets/c80d36c2-75b0-4d3e-91e0-08e9f128ea6d" />

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
<img width="835" alt="Screenshot 2025-05-20 at 10 36 42 AM" src="https://github.com/user-attachments/assets/19952e90-42f5-4a69-934d-3a8d99efc793" />

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
<img width="809" alt="Screenshot 2025-05-20 at 10 36 48 AM" src="https://github.com/user-attachments/assets/885ea782-12b9-4f46-9f31-06be6f242e78" />


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
<img width="819" alt="Screenshot 2025-05-20 at 10 36 54 AM" src="https://github.com/user-attachments/assets/92ac2381-1f1f-4c9a-8e08-963a8e98e198" />

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
<img width="622" alt="Screenshot 2025-05-20 at 10 37 01 AM" src="https://github.com/user-attachments/assets/a8ef7848-e89c-42db-9f4e-cb47dae35605" />

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
<img width="656" alt="Screenshot 2025-05-20 at 10 37 08 AM" src="https://github.com/user-attachments/assets/e477a3b2-abf7-4dca-8ee7-ce7660af25d2" />


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
<img width="694" alt="Screenshot 2025-05-20 at 10 37 14 AM" src="https://github.com/user-attachments/assets/37f1f860-693b-4a0d-8b4f-7b6c6f809eb4" />

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
<img width="703" alt="Screenshot 2025-05-20 at 10 37 20 AM" src="https://github.com/user-attachments/assets/81a88c95-3847-4ef1-bf53-8c54eb2cc365" />

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
<img width="718" alt="Screenshot 2025-05-20 at 10 37 27 AM" src="https://github.com/user-attachments/assets/87328e5f-1862-49a4-9e41-b8adb517ef2e" />

 
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
<img width="712" alt="Screenshot 2025-05-20 at 10 37 33 AM" src="https://github.com/user-attachments/assets/00993a4e-ea1a-4739-9aa6-934270ff39c6" />

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
 <img width="752" alt="Screenshot 2025-05-20 at 10 37 41 AM" src="https://github.com/user-attachments/assets/1fdd559b-d090-4602-9298-c6bcf768c93a" />

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
<img width="724" alt="Screenshot 2025-05-20 at 10 37 48 AM" src="https://github.com/user-attachments/assets/ccac2e9e-4ba4-40d6-9bc1-ff95c29d8176" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="655" alt="Screenshot 2025-05-20 at 10 37 55 AM" src="https://github.com/user-attachments/assets/db919952-c7e6-43f5-b189-821f05622bac" />



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
<img width="436" alt="Screenshot 2025-05-20 at 10 38 02 AM" src="https://github.com/user-attachments/assets/2d005038-d72d-4555-80b5-3c734d8be6fc" />

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
<img width="437" alt="Screenshot 2025-05-20 at 10 38 08 AM" src="https://github.com/user-attachments/assets/609cf810-6fba-4c07-bbd9-3c1bbe91d268" />

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
 <img width="510" alt="Screenshot 2025-05-20 at 10 38 16 AM" src="https://github.com/user-attachments/assets/fe952516-6443-4a46-b9d1-fded945718b3" />

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
 <img width="525" alt="Screenshot 2025-05-20 at 10 38 22 AM" src="https://github.com/user-attachments/assets/f8736ec7-3f29-4759-a925-c27209cbe68c" />

 
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
 <img width="583" alt="Screenshot 2025-05-20 at 10 38 28 AM" src="https://github.com/user-attachments/assets/163c0e68-7c76-47a5-9edb-cb011249577e" />

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
<img width="576" alt="Screenshot 2025-05-20 at 10 38 54 AM" src="https://github.com/user-attachments/assets/6a0ee9c6-e98e-449d-a868-982998b9f15e" />


# RESULT:
The Commands are executed successfully.
