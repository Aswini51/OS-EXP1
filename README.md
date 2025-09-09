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
<img width="800" height="98" alt="image" src="https://github.com/user-attachments/assets/b27d35f0-a01d-4705-a108-9e88eafac241" />

cat < file2
## OUTPUT
<img width="800" height="98" alt="image" src="https://github.com/user-attachments/assets/449de41a-3979-4155-a2c5-85f596b455c0" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="834" height="37" alt="image" src="https://github.com/user-attachments/assets/a39f8da8-2dbd-4fb8-8440-aa22a63aa631" />

comm file1 file2
 ## OUTPUT
 <img width="833" height="171" alt="image" src="https://github.com/user-attachments/assets/a31d4b58-dfce-4922-82b9-82bbed0b1a9c" />

diff file1 file2
## OUTPUT
<img width="864" height="215" alt="image" src="https://github.com/user-attachments/assets/a0b7eb64-46f5-4d7a-b77c-e5be080ff1b1" />

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
<img width="855" height="60" alt="image" src="https://github.com/user-attachments/assets/c4fe7959-b2aa-4a81-b057-cf879a2bc62d" />

cut -d "|" -f 1 file22
## OUTPUT
<img width="895" height="76" alt="image" src="https://github.com/user-attachments/assets/f117a03c-b81d-4d3c-828d-37c7dc5c36d6" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="895" height="76" alt="image" src="https://github.com/user-attachments/assets/4206c68a-1344-4aa2-bcfa-133503c67180" />

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
<img width="822" height="36" alt="image" src="https://github.com/user-attachments/assets/1ef0f5bf-7657-4dc2-9bfa-43966bbc9208" />

grep hello newfile 
## OUTPUT
<img width="822" height="36" alt="image" src="https://github.com/user-attachments/assets/b7bcbdc4-6611-4ca6-922c-2a38e303bcba" />

grep -v hello newfile 
## OUTPUT
<img width="822" height="36" alt="image" src="https://github.com/user-attachments/assets/6b238c1b-a171-466e-8cdc-6011feee185b" />

cat newfile | grep -i "hello"
## OUTPUT
<img width="830" height="54" alt="image" src="https://github.com/user-attachments/assets/7c582bb7-ddb2-419b-8503-c484e916d1c0" />

cat newfile | grep -i -c "hello"
## OUTPUT
<img width="829" height="41" alt="image" src="https://github.com/user-attachments/assets/17799ae5-39cb-4a43-99ef-a00829f12c4d" />

grep -R ubuntu /etc
## OUTPUT
<img width="829" height="506" alt="image" src="https://github.com/user-attachments/assets/2645cf9c-e2b3-4858-81e4-0dc4da0c38a5" />

grep -w -n world newfile   
## OUTPUT
<img width="758" height="84" alt="image" src="https://github.com/user-attachments/assets/121a8bdb-80a7-4fdf-8388-b2ca60f2b64f" />

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
<img width="810" height="87" alt="image" src="https://github.com/user-attachments/assets/ae9d8c96-f11a-4248-8b4a-663f3d753cdb" />

egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="810" height="87" alt="image" src="https://github.com/user-attachments/assets/45c4a3bc-7f41-482d-a92a-2f9b4c37a3be" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="810" height="87" alt="image" src="https://github.com/user-attachments/assets/ffd6cd80-ea10-483f-8ecb-a325ea7017cc" />

egrep '(^hello)' newfile 
## OUTPUT
<img width="810" height="87" alt="image" src="https://github.com/user-attachments/assets/2779ab11-1b30-4f4f-9541-d7694f657fc0" />

egrep '(world$)' newfile 
## OUTPUT
<img width="810" height="87" alt="image" src="https://github.com/user-attachments/assets/ad409625-e076-4992-ace8-ecdf0bba0d3a" />

egrep '(World$)' newfile 
## OUTPUT
<img width="810" height="87" alt="image" src="https://github.com/user-attachments/assets/cbdea3c4-882a-455f-a289-3bc62abe47fe" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="810" height="87" alt="image" src="https://github.com/user-attachments/assets/24c515e7-8768-47c0-aeb9-5733323d0791" />

egrep '[1-9]' newfile 
## OUTPUT
<img width="810" height="87" alt="image" src="https://github.com/user-attachments/assets/4a5875ef-4ad7-47eb-b18e-161ca4e2871b" />

egrep 'Linux.*world' newfile 
## OUTPUT
<img width="810" height="87" alt="image" src="https://github.com/user-attachments/assets/51df68b2-320e-4e8a-b22a-40e37368ac78" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="810" height="87" alt="image" src="https://github.com/user-attachments/assets/2a70a75f-9902-4170-a97f-fd7950b4de80" />

egrep l{2} newfile
## OUTPUT
<img width="810" height="87" alt="image" src="https://github.com/user-attachments/assets/1b18dc60-2b0f-4e39-9867-4e89b7148e1f" />

egrep 's{1,2}' newfile
## OUTPUT 
<img width="823" height="98" alt="image" src="https://github.com/user-attachments/assets/03607f3b-cbb5-4650-bb4e-f0ffe9374806" />

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
<img width="823" height="98" alt="image" src="https://github.com/user-attachments/assets/5396fd16-1acd-4d18-943a-8457b83494f8" />

sed -n -e '$p' file23
## OUTPUT
<img width="823" height="98" alt="image" src="https://github.com/user-attachments/assets/d409a978-9b6c-4d15-af94-3eebbe4f5581" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="839" height="195" alt="image" src="https://github.com/user-attachments/assets/20f62fde-37c0-49c9-a460-f97fc7ca73bf" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="839" height="195" alt="image" src="https://github.com/user-attachments/assets/3851413b-22b5-4f37-9b96-a90299a8c278" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="839" height="195" alt="image" src="https://github.com/user-attachments/assets/ae883e03-2c38-4d58-9ead-9e4153a40813" />

sed -n -e '1,5p' file23
## OUTPUT
<img width="828" height="141" alt="image" src="https://github.com/user-attachments/assets/ef6ef590-08ae-459b-b973-8c542923bc40" />

sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="817" height="104" alt="image" src="https://github.com/user-attachments/assets/a5f72403-d669-458a-a691-e94f86724d60" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="817" height="104" alt="image" src="https://github.com/user-attachments/assets/218063a9-2051-410d-99cf-89b3a9c6f305" />

seq 10 
## OUTPUT
<img width="838" height="233" alt="image" src="https://github.com/user-attachments/assets/fc9f4cfd-d24c-4f69-89ad-f95720841626" />

seq 10 | sed -n '4,6p'
## OUTPUT
<img width="833" height="133" alt="image" src="https://github.com/user-attachments/assets/7dae501a-c93a-4a7f-a809-449af1746927" />

seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="833" height="133" alt="image" src="https://github.com/user-attachments/assets/57934465-e09d-4382-b66a-30fe91c9270a" />

seq 3 | sed '2a hello'
## OUTPUT
<img width="833" height="133" alt="image" src="https://github.com/user-attachments/assets/4dba14c7-1383-4f0c-b160-4d661b0c9c91" />

seq 2 | sed '2i hello'
## OUTPUT
<img width="833" height="133" alt="image" src="https://github.com/user-attachments/assets/44c3acc3-dadd-4b98-a150-74bf2bc6410d" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="833" height="133" alt="image" src="https://github.com/user-attachments/assets/da605c5f-30e3-494f-8733-7ca543a8161f" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="833" height="133" alt="image" src="https://github.com/user-attachments/assets/83cbb602-1243-4dda-9ce0-ea5d332d945f" />

sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="833" height="133" alt="image" src="https://github.com/user-attachments/assets/0559660f-4b6b-4fda-9ccd-6d51d89412d9" />

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
<img width="833" height="133" alt="image" src="https://github.com/user-attachments/assets/8a76aa6f-78ed-4b03-be36-eaef2e5a3bd2" />

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
<img width="832" height="189" alt="image" src="https://github.com/user-attachments/assets/96d96def-94d4-4f0e-a1f2-9c2610b99420" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
## OUTPUT
<img width="832" height="189" alt="image" src="https://github.com/user-attachments/assets/0b2e0ccf-04c2-4600-8d44-64ad52c4f163" />

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
<img width="822" height="105" alt="image" src="https://github.com/user-attachments/assets/15e219b8-5459-43c6-a2e2-3da2c305bbd2" />

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="822" height="105" alt="image" src="https://github.com/user-attachments/assets/17a49ea3-7b8f-4c26-8d9d-3e8a3130e69e" />

#Backup commands tar -cvf backup.tar *
## OUTPUT
<img width="834" height="630" alt="image" src="https://github.com/user-attachments/assets/7d0c41a7-e24a-4c48-add8-6d14a04fccb1" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="837" height="637" alt="image" src="https://github.com/user-attachments/assets/dd9bfa18-4c8f-4593-b4aa-bf0351ad2677" />

tar -xvf backup.tar
## OUTPUT
<img width="824" height="71" alt="image" src="https://github.com/user-attachments/assets/e5823b80-ff9b-424e-a884-d621baa20084" />

gzip backup.tar

ls .gz

gunzip backup.tar.gz
## OUTPUT
 <img width="835" height="108" alt="image" src="https://github.com/user-attachments/assets/9755742a-80d9-4cb5-8744-32e1668789a7" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="835" height="108" alt="image" src="https://github.com/user-attachments/assets/2e7aa4c1-bd2d-44a3-9249-fc2f6b714f0f" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="422" height="116" alt="image" src="https://github.com/user-attachments/assets/dceb295d-3f15-4573-894b-184ce1a279d3" />

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

<img width="811" height="645" alt="image" src="https://github.com/user-attachments/assets/3848ba74-da09-476a-9661-b770584cdfa3" />

ls file1
## OUTPUT
<img width="646" height="84" alt="image" src="https://github.com/user-attachments/assets/bedbccba-1f54-4fcb-b85a-84fb55b1dee6" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
<img width="628" height="63" alt="image" src="https://github.com/user-attachments/assets/cfb1f778-e998-4f16-b578-3855962c0ce0" />

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
<img width="487" height="331" alt="image" src="https://github.com/user-attachments/assets/d98edd26-786f-47e6-b1db-97a07e66ac9d" />

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="741" height="88" alt="image" src="https://github.com/user-attachments/assets/a556e682-3df0-4a23-8d07-2a9da3ac1b20" />

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
<img width="741" height="88" alt="image" src="https://github.com/user-attachments/assets/23cb659d-a39c-4416-8c97-115cda3029fa" />

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
<img width="746" height="133" alt="image" src="https://github.com/user-attachments/assets/cb52d413-d679-499f-89f0-a94fe289bc6e" />

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
<img width="746" height="133" alt="image" src="https://github.com/user-attachments/assets/073fec0a-756c-43f7-9a49-e4193cf06dbe" />

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
<img width="746" height="133" alt="image" src="https://github.com/user-attachments/assets/b54cde0d-e2d5-4ca9-87fd-707e94787ae6" />

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
<img width="746" height="133" alt="image" src="https://github.com/user-attachments/assets/9bb14c54-4450-471c-a29d-5ef97d939ca7" />

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
<img width="746" height="133" alt="image" src="https://github.com/user-attachments/assets/319e52b3-5e88-4ef6-97eb-6ab0461e04c4" />

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
<img width="777" height="172" alt="image" src="https://github.com/user-attachments/assets/c17f9ec5-2ec6-4eec-993d-c163f51a3c8b" />

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
<img width="771" height="180" alt="image" src="https://github.com/user-attachments/assets/5ffae6e5-308f-400a-bde5-0493b812e1bf" />

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
<img width="771" height="180" alt="image" src="https://github.com/user-attachments/assets/9891b24b-cff4-4d2f-8368-46c4d213b412" />

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
<img width="771" height="180" alt="image" src="https://github.com/user-attachments/assets/54d62678-5870-45ff-bab5-87f8019198f6" />

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
<img width="771" height="180" alt="image" src="https://github.com/user-attachments/assets/3726ac5c-d1dd-49a0-8214-382fd55ec3a1" />

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
<img width="771" height="180" alt="image" src="https://github.com/user-attachments/assets/b871ab33-40eb-412f-ba6e-484078598065" />

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
 <img width="767" height="155" alt="image" src="https://github.com/user-attachments/assets/51a00670-1f32-4efc-924d-67e6b4f78b54" />

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
<img width="759" height="119" alt="image" src="https://github.com/user-attachments/assets/93552cc0-6515-46b7-a7ef-3c8f17410cf0" />

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
<img width="759" height="119" alt="image" src="https://github.com/user-attachments/assets/e0cc81ee-e2b8-445d-b71f-a77977788128" />

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
<img width="759" height="119" alt="image" src="https://github.com/user-attachments/assets/350ac84c-d58c-47d3-9290-a9c0cb9842c7" />

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
 <img width="754" height="336" alt="image" src="https://github.com/user-attachments/assets/9f9d0d97-0e91-4730-90d2-d88d84816f9f" />

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
 <img width="761" height="288" alt="image" src="https://github.com/user-attachments/assets/aa599537-8049-467d-8613-f5f46600554b" />

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
<img width="751" height="119" alt="image" src="https://github.com/user-attachments/assets/c9892eec-a214-4a14-9293-9573bd0f538e" />

# RESULT:
The Commands are executed successfully.
