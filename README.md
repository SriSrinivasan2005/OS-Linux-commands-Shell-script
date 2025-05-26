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

![output1_1](https://github.com/user-attachments/assets/fe25af33-fffb-4cee-92bb-d313a9c9caf4)


cat < file2
## OUTPUT
![output1_2](https://github.com/user-attachments/assets/d00a956d-0206-40e0-8bd4-b342a64b63bf)


# Comparing Files
cmp file1 file2
## OUTPUT
![output1_3](https://github.com/user-attachments/assets/057cf882-0152-4633-b819-47b4503634df)

comm file1 file2
 ## OUTPUT
![output1_4](https://github.com/user-attachments/assets/4fe2214c-2a1f-4cbe-9629-5ec72c6f49fa)

 
diff file1 file2
## OUTPUT

![output1_5](https://github.com/user-attachments/assets/03b921cd-1ecc-4c82-8574-0dc8108b6cc9)

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
![output1_6](https://github.com/user-attachments/assets/d79c5f48-4e18-4e5e-be3c-c3eac1785839)




cut -d "|" -f 1 file22
## OUTPUT
![output](./output1_7.png)

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
![output1_9](https://github.com/user-attachments/assets/be6389aa-fb38-4aad-aee6-519fc9c7d884)


grep hello newfile 
## OUTPUT

![output1_10](https://github.com/user-attachments/assets/9b455871-73f9-4111-85c0-650c15f655c4)



grep -v hello newfile 
## OUTPUT
![output1_11](https://github.com/user-attachments/assets/434c2237-05f7-420f-a4e5-b69ffe494fce)



cat newfile | grep -i "hello"
## OUTPUT

![output1_12](https://github.com/user-attachments/assets/590ba78c-a6c5-4191-82c9-b684d3104304)



cat newfile | grep -i -c "hello"
## OUTPUT
![output1_13](https://github.com/user-attachments/assets/befeaf58-59ad-4bfe-86b2-732b385e0530)




grep -R ubuntu /etc
## OUTPUT
![output1_14](https://github.com/user-attachments/assets/820c6f85-82cb-49c7-b1d8-346422646961)



grep -w -n world newfile   
## OUTPUT

![output1_15](https://github.com/user-attachments/assets/46893fa5-1339-40b3-aed6-0b740dd8eac4)

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
![output1_16](https://github.com/user-attachments/assets/1a366346-757d-41ca-8ce0-35d5899b7465)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![output1_17](https://github.com/user-attachments/assets/25d92ca5-764a-4200-87ac-792a076cf78c)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![output1_17](https://github.com/user-attachments/assets/74d033df-0413-4d94-b415-c40b48ff83a2)


egrep '(^hello)' newfile 
## OUTPUT
![output1_19](https://github.com/user-attachments/assets/d7e251c8-6dc0-4f5d-a63b-1000cbe804af)



egrep '(world$)' newfile 
## OUTPUT

![output1_20](https://github.com/user-attachments/assets/4256de38-c306-43f5-bc64-2406b5a0a485)

egrep '(World$)' newfile 
## OUTPUT
![output1_21](https://github.com/user-attachments/assets/39eb0317-4477-4a18-b80f-ac183ba75464)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![output1_22](https://github.com/user-attachments/assets/b8aa0566-b160-45ac-8f8c-a7e77ca5fd6e)


egrep '[1-9]' newfile 
## OUTPUT

![output1_23](https://github.com/user-attachments/assets/ced1f962-061e-441b-9e86-575541d4688f)


egrep 'Linux.*world' newfile 
## OUTPUT
![output1_24](https://github.com/user-attachments/assets/79b4f1ac-3d88-4d8a-88d1-c6e1a671a621)


egrep 'Linux.*World' newfile 
## OUTPUT
![output1_25](https://github.com/user-attachments/assets/68fd9eca-ed72-405a-93c6-f0d88638e3a4)


egrep l{2} newfile
## OUTPUT

![output1_26](https://github.com/user-attachments/assets/113ec83d-f565-48eb-b7d6-144accc56df6)


egrep 's{1,2}' newfile
## OUTPUT 
![output1_27](https://github.com/user-attachments/assets/2fe2cee5-6c96-403b-8047-00e4525ef4dd)


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

![output1_28](https://github.com/user-attachments/assets/566752ff-9697-414d-bfb9-0228fc3505fc)

sed -n -e '$p' file23
## OUTPUT
![output1_29](https://github.com/user-attachments/assets/95a676b6-e776-4b40-a960-ddf6d9f55d41)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![output1_30](https://github.com/user-attachments/assets/360b05a1-9640-43e8-9905-a14f1e08c017)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![output1_31](https://github.com/user-attachments/assets/12c5ccfb-eba0-44d6-bf7b-e569582fa200)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![output1_32](https://github.com/user-attachments/assets/653d3818-9fae-4ec3-aed9-baf65659c561)


sed -n -e '1,5p' file23
## OUTPUT
![output1_33](https://github.com/user-attachments/assets/170a7444-819f-41cd-b985-35cc5608edc2)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![output1_34](https://github.com/user-attachments/assets/9b8b0bef-415a-45f0-80d4-ed4c8b2e40e7)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![output1_35](https://github.com/user-attachments/assets/04807731-07cf-43e3-82df-aacde4c984f5)


seq 10 
## OUTPUT

![output1_36](https://github.com/user-attachments/assets/65070c15-6a1c-4817-af95-0cce890f3086)


seq 10 | sed -n '4,6p'
## OUTPUT

![output1_37](https://github.com/user-attachments/assets/130e4e2a-0f23-4141-9180-b91f468a7f33)


seq 10 | sed -n '2,~4p'
## OUTPUT

![output1_38](https://github.com/user-attachments/assets/ec4c77e5-bb98-4494-8909-90fd54505ec6)


seq 3 | sed '2a hello'
## OUTPUT
![output1_39](https://github.com/user-attachments/assets/42682daa-0245-4a44-a09a-24e7e36550b5)



seq 2 | sed '2i hello'
## OUTPUT
![output1_40](https://github.com/user-attachments/assets/2c3ad6c0-2fa4-40ea-97a6-6cccf5b77a9f)


seq 10 | sed '2,9c hello'
## OUTPUT
![output1_41](https://github.com/user-attachments/assets/82c77379-b538-44bc-b0ee-1dd741883936)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![output1_42](https://github.com/user-attachments/assets/f8134b6a-3c9a-4219-92ce-8fa2e3db438e)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![output1_43](https://github.com/user-attachments/assets/f152d4ed-23b8-4e00-829f-db76962fcd6e)

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
![output1_44](https://github.com/user-attachments/assets/ebfd36f9-344d-4844-92dc-455152d898f0)


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

![output1_45](https://github.com/user-attachments/assets/0d337493-aed4-4865-8f58-14f915e0e735)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![output1_46](https://github.com/user-attachments/assets/a406bf84-e587-4236-bfe9-05e2cbcf79df)

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

![output1_47](https://github.com/user-attachments/assets/2fe27679-d802-4b7f-b802-eb788e76a374)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![output1_48](https://github.com/user-attachments/assets/21a784a4-982d-42ec-b6e1-df8085d2ca69)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![output1_49](https://github.com/user-attachments/assets/dac3252e-3ad4-4b92-b8aa-e6023a7bbb05)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![output1_50](https://github.com/user-attachments/assets/808b4127-83ea-4250-91a5-720a4a8f6146)


tar -xvf backup.tar
## OUTPUT
![output1_51](https://github.com/user-attachments/assets/ec6183df-ee09-49ca-9fcb-41a7b9091fc1)

gzip backup.tar

ls .gz
## OUTPUT
![output1_52](https://github.com/user-attachments/assets/581e9c1b-da91-43a7-b79e-25fb007fe0d7)

gunzip backup.tar.gz
## OUTPUT

 ![output1_53](https://github.com/user-attachments/assets/48041c54-58c8-45e9-9f00-621b236355c9)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![output1_54](https://github.com/user-attachments/assets/703bf7a7-e731-4dfc-9f82-81d541b9c55f)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![output1_55](https://github.com/user-attachments/assets/da6639f9-5b5b-4e1c-9e7f-66fc96523bf2)


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

 ![output1_56](https://github.com/user-attachments/assets/43881ffb-83b0-4006-ac2e-02d622785799)

ls file1
## OUTPUT
![output1_57](https://github.com/user-attachments/assets/164be2a3-d73b-4255-938b-b18dcf14bc09)

echo $?
## OUTPUT 
![output1_58](https://github.com/user-attachments/assets/44c34da9-90b1-4f4e-b2af-63efcaddf1d2)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![output1_59](https://github.com/user-attachments/assets/77660223-eb37-41ac-974e-42c1431015c2)

abcd
 
echo $?
 ## OUTPUT

![output1_60](https://github.com/user-attachments/assets/7d6952ad-d51d-42c4-aa2e-0f242fdfe4c0)

 
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

![output1_61](https://github.com/user-attachments/assets/5740689f-0c23-4250-9d67-670f89f19634)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![output1_62](https://github.com/user-attachments/assets/cc5dd57f-6ffe-4026-affb-931e87b23f5f)


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
 chmod 755 psswdperm.sh

./psswdperm.sh
## OUTPUT
![output1_63](https://github.com/user-attachments/assets/6a5fa1d9-282c-4c97-a659-22eb249309a2)

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
chmod 755 ifnested.sh

./ifnested.sh 
## OUTPUT
![output1_64](https://github.com/user-attachments/assets/d83cd3e5-79ec-4f31-b8b9-7308abbfa619)



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
![output1_65](https://github.com/user-attachments/assets/caa40299-6917-49f2-a29d-32f0960289ff)

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
![output1_66](https://github.com/user-attachments/assets/a6e2e9cb-38e8-481a-af87-85c9ed766912)

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

![output1_67](https://github.com/user-attachments/assets/73136547-8ceb-45a9-92e0-a3f29a34a105)

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
![output1_68](https://github.com/user-attachments/assets/e8623f53-57b2-47a9-862e-bf54bcf7379b)

# using the case command
cat >casecheck.sh 
```bash
case $USER in Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";Rahim)
echo "Special testing account";gganesh)
echo "$USER, Do not forget to log off when you're done";*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
## OUTPUT
![output1_69](https://github.com/user-attachments/assets/b1d4b982-d26c-4c7b-a452-94b3ef329d5f)


cat > whiletest.sh
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

 ![output1_70](https://github.com/user-attachments/assets/358fbf5e-f359-477f-82c8-5914c673e085)

cat > untiltest.sh 
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

$ ./untiltest.sh
 ## OUTPUT
![output1_71](https://github.com/user-attachments/assets/c338792f-7b80-4d62-b02f-fb0872502bc6)

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

$ ./forin1.sh
## OUTPUT
![output1_72](https://github.com/user-attachments/assets/886c35cb-4ae7-4037-86b5-330e0e732e20)

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
![output1_73](https://github.com/user-attachments/assets/96663193-e404-43e0-8ac5-ae96127cce32)

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
![output1_74](https://github.com/user-attachments/assets/d82a5de2-5d8a-4408-8a7d-1e9bdeb2d3a5)

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

![output1_75](https://github.com/user-attachments/assets/43d1dda8-70c4-4ed2-952d-c155e45a6a92)

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
![output1_76](https://github.com/user-attachments/assets/e3904a75-9ac7-4af7-8eeb-fa186ca1cf98)


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

 ![output1_77](https://github.com/user-attachments/assets/5a6ee716-7c66-42aa-af9c-bde294c3eb33)

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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
## OUTPUT
![output1_78](https://github.com/user-attachments/assets/746fd2cf-151b-46a4-8966-c1ea53feac62)

 
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
![output1_79](https://github.com/user-attachments/assets/59b6d8af-36f0-4c37-a58a-d47e3297e19d)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program."
``` 
$ chmod 755 exread1.sh 

$ ./exread1.sh
## OUTPUT
![output1_80](https://github.com/user-attachments/assets/04ecb305-6989-4752-ad94-dc5c79ee6601)


 
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

 ## OUTPUT
![output1_81](https://github.com/user-attachments/assets/3cd984bd-9707-4a60-86f8-3f0ea60ca1b5)


 
 ./funcex.sh 1 2

## OUTPUT

 ![output1_82](https://github.com/user-attachments/assets/0a049d18-9e2a-4d74-8020-533dde917032)

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
![output1_83](https://github.com/user-attachments/assets/83e0b674-ff9e-4c5e-a11e-d35d3d275095)


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
![output1_84](https://github.com/user-attachments/assets/6f260630-249f-4bc0-ad93-70fa592f12ea)


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

![output1_85](https://github.com/user-attachments/assets/6f4819db-954f-4827-90d2-10ab3375638e)

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

![output1_86](https://github.com/user-attachments/assets/238a7815-e728-4d0a-85c9-e6e883188f30)

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
chmod 755 palindrome.sh

./palindrome.sh
## OUTPUT 
![output1_87](https://github.com/user-attachments/assets/a28a7142-77e0-4142-9afb-6b0e4eac70f6)


# RESULT:
The Commands are executed successfully.
