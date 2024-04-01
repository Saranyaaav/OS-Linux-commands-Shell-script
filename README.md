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
![Screenshot from 2024-02-20 18-47-29](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/10cfea8e-8a08-4be2-93ec-906dbbc03a37)


cat < file2
## OUTPUT
![Screenshot from 2024-02-20 18-49-28](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/a737e624-6167-4ec7-992a-5208a975c384)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot from 2024-02-20 18-53-23](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/3a5f1033-7a70-4ce2-9219-363611ce3417)

comm file1 file2
 ## OUTPUT
![Screenshot from 2024-02-20 18-53-54](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/32706083-02c3-4639-beb6-a549fba55dc8)

 
diff file1 file2
## OUTPUT
![Screenshot from 2024-02-20 18-54-29](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/208403ee-ead1-42e0-9361-f6853a67e80c)


## Filters

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
![Screenshot from 2024-02-20 19-00-24](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/37e78c4f-80e3-4c26-b033-d3ccc5c6361b)




cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2024-02-20 19-02-46](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/17c244e9-ed7f-4239-bc18-e5324e8e80c7)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2024-02-20 19-03-22](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/0728f245-cadf-4d2a-8f69-f3d3a045b3eb)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
```
Hello world
hello world
```

grep Hello newfile 
## OUTPUT
![Screenshot from 2024-02-20 19-08-43](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/c3b97c60-e771-44e2-ae34-933f769abaaa)



grep hello newfile 
## OUTPUT
![Screenshot from 2024-02-20 19-09-12](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/b04ef432-3ed8-44a7-a56f-aa470a6e7187)




grep -v hello newfile 
## OUTPUT
![Screenshot from 2024-02-20 19-11-22](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/8fecdc9c-4d30-4fe3-baa7-201c2584660d)



cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2024-02-20 19-13-27](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/ba930ce0-ae4a-4f7d-95fa-478af3cafae5)




cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2024-02-20 19-14-13](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/8ccfe88e-f350-4d30-90cd-aa5a87f54ea7)




grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2024-02-21 23-23-37](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/6a67c53b-6f70-4f82-981e-19d6652aa73b)



grep -w -n world newfile   
## OUTPUT
![Screenshot from 2024-02-22 08-25-08](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/295bcf6d-7c89-4069-91ce-2f8570b59182)


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
![Screenshot from 2024-02-25 17-21-51](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/7a72c17a-4844-4c39-9ba6-59071368d7a2)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2024-02-25 17-22-05](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/73ac6ea3-0a1b-448b-9439-8e5c4c4b10b9)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot from 2024-02-25 17-24-48](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/7f779eef-0e62-480d-b213-c174632a962c)




egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2024-02-25 17-26-03](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/c5beaec2-ff6f-4a2a-812e-7de649ed009e)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2024-02-25 17-26-46](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/2e068810-c34c-41a3-a7f9-0211ebc5b0ed)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2024-02-25 17-27-45](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/78551565-34c1-4881-ac52-2ee7d543e2f5)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2024-02-25 17-28-27](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/d1b5cc4f-5d25-4361-b36b-db6be4665c25)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2024-02-25 18-17-08](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/19e5db67-5f57-4a08-aff8-5085f2a8c1ff)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2024-02-25 18-18-28](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/dde95baa-793a-4b35-9f51-e5c438f184e2)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2024-02-25 18-19-25](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/997fa573-3528-48b6-84d5-76f4a6f3d237)


egrep l{2} newfile
## OUTPUT
![Screenshot from 2024-02-25 18-20-15](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/c5bae390-c8f0-4c0a-bb5d-bc6d3e11f7a1)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2024-02-25 18-21-23](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/b2a328d6-3d47-49e6-9800-d2b6f1059f4b)


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
![Screenshot from 2024-02-25 18-30-07](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/f79f8db4-4124-48d0-b28f-baa67487298c)



sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2024-02-25 18-31-10](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/bcb17e17-3618-42b3-85f1-8a890d17191e)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2024-02-25 18-32-19](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/3f2a8b67-4fb3-4b7a-8014-2072d19e8977)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2024-02-25 18-33-03](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/c058fe38-ff2b-4872-b904-d5bb769ee255)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2024-02-25 18-34-13](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/4ce896bc-a826-492a-9d7c-145c1a04b784)



sed -n -e '1,5p' file23
## OUTPUT
![Screenshot from 2024-02-25 18-36-28](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/417e01b5-f04c-46e2-b39b-6235c9e2ca1d)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot from 2024-02-25 18-37-14](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/ef2d483d-ce1f-4a41-abb4-063c94bbe404)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2024-02-25 18-38-00](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/a5320b8b-26a1-413f-b2f5-5a2a25022a55)



seq 10 
## OUTPUT
![Screenshot from 2024-02-25 18-38-59](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/0aa005e3-95c8-4e59-b037-26350afac1d0)



seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2024-02-25 18-40-01](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/d04807ca-3734-41a8-bf0c-796b4a3c271a)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2024-02-25 18-54-37](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/2b02dca1-6679-49e1-8547-b6e0d740a947)



seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2024-02-25 19-02-10](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/960feef8-5c94-4727-8770-4b8b149f9251)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2024-02-25 19-02-44](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/8e20f3aa-0045-4624-b91b-6b814b49f6a1)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2024-02-25 19-03-17](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/d139a455-f356-4146-8645-d870944417dc)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2024-02-25 19-04-13](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/a53c0709-6860-453d-ba4a-eb3f3d3c1bfc)


## Sorting File content
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
![Screenshot from 2024-02-25 19-09-07](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/e682f51a-f38b-480f-9640-3d1cadfadf76)


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
![Screenshot from 2024-02-25 19-11-39](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/78e4d98e-c30d-44c6-808f-3aaaf5288bdb)



## Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2024-02-25 19-15-20](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/eafacb18-2f26-4d6c-b1b3-46b6ee5e05c0)

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
![Screenshot from 2024-02-25 19-17-13](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/bee9db5f-a06f-4d70-b58a-9fed01a79050)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot from 2024-02-25 19-18-22](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/cd898673-61d6-4e9c-af4e-33646580d46d)



## Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2024-02-25 19-19-55](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/e8c3766b-d3f1-40be-97ec-d691d72f145a)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot from 2024-02-27 13-26-34](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/a565b543-cdfd-4d7f-9ae7-93454c2c46b7)


tar -xvf backup.tar
## OUTPUT
![Screenshot from 2024-02-27 13-27-09](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/cb97f710-5e43-44b7-9e41-9423f632d706)

gzip backup.tar

ls .gz
## OUTPUT
 ![Screenshot from 2024-02-27 14-14-33](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/8e4d9e5c-8fbb-4a16-808a-2cedd5335151)

gunzip backup.tar.gz
## OUTPUT
![Screenshot from 2024-02-27 14-16-05](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/434c88fe-4868-4711-97d1-3ca4adc05a50)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot from 2024-02-27 19-23-29](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/705743aa-da56-468d-8cb0-64bb80fc0854)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot from 2024-02-27 14-14-33](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/577dc710-e2f5-47ca-a18c-2235256d029a)


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
![Screenshot from 2024-02-27 19-48-25](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/0458be6e-6018-4e62-9013-25688c61807a)

 
ls file1
## OUTPUT
![Screenshot from 2024-02-27 19-51-23](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/c214767b-fdae-4cc4-8281-59b0c333839c)

echo $?
## OUTPUT 
![Screenshot from 2024-02-27 19-51-45](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/9df8671b-1ea3-46ba-8e1b-bd0ac99fe637)

 
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
![Screenshot from 2024-02-28 22-06-26](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/5957a1be-48a0-41ca-b58b-457777eb0b62)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot from 2024-02-28 22-10-00](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/0a59ee23-676b-4ff2-b647-1a0ef94e9621)


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

## OUTPUT

./psswdperm.sh
## OUTPUT
![Screenshot from 2024-02-28 22-23-41](https://github.com/Saranyaaav/OS-Linux-commands-Shell-script/assets/144870813/868cc5b2-4edc-4fdb-9152-a99936bb4b97)


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
