UNIX Assignments: Day 1

Concept:   Basic commands in UNIX, 

Objective: At the end of the assignment, participants will be able to:
•	Execute Basic Unix commands
Problems: 

Section 1:

1.	List all the files and sub directories of the directory /bin.

ls –l /usr/bin

2.	List all the files including hidden files in your current directory.

ls -l -a

3.	List all the files starting with letter ‘r’ in your current 

directory.

ls r*

4.	List all the files having three characters in their names, from your 

current directory.

ls | grep '^...$'

5.	List all the files with extension .doc in your current directory.

ls | grep '.doc$'

6.	List all the files having the first letter of their name within the 

range ‘l’ to‘s’, from
 your current directory.

ls | grep '^[l-s]'

7.	Create a file text1 and read its input from keyboard.

grep "" > text1

8.	Copy the contents of file text1 to another file text2.

mv text1 text2

9.	Append the contents of file text2 to file text1.

cat text1 >> text2

10.	Count the number of files in the current directory.

ls | wc -l

11.	Display the output of command ls –l to a file and on the output 

screen.

ls -l | tee text1

12.	From file text1 print all lines starting from 10th line.

head --lines=10 text1

13.	Find the number of users currently logged on to the system.

cat /etc/passwd | wc -l

14.	Delete all the files with their names starting with “tmp”.

rm -v tmp*

15.	List only the directories in your current directory

ls -d */
ls -l | grep "^d"

------------------------


1.	Count the total number of words in file text1.

2.	Display the system date in following format: Today is Friday, 17 May 

96

echo "Today is $(date)"

3.	Display the following text message on the monitor screen. Deposited 

$100 to you account

echo "Deposited \$100 to your account"


4.	Display the following message on the monitor. The long listing of my 

home dir …………   is …………  (Hint: Use ls – l and pwd commands)

echo "The long listing of my home dir $HOME is $(pwd)"

5.	Display the name and count of the directories in the current 

directory.

echo -e "$(ls -d */)\nTotal number of Directories: $(ls -d *. | wc -w)"


6.	Assign a value “Black” to var1 and then display the following 

message on the terminal using this variable. Black belt is associated with 

karate



7.	Create the file employee.txt having colon (: ) separated fields. 
The fields of the record are: enumber, ename, eposition, esal, edoj, edept. 
And now answer the following:



a.	List all the employees along with a row number



b.	Sort the file as per the names

cut -d ':' -f 2 emp.txt | sort 

c.	List top three salaried employees

cut -d ':' -f 4 emp.txt : sort : tail -n 3

d.	Remove duplicate records from the file



e.	List dept. no along with no. of employees working in each dept.
f.	Sort the file in descending order of salary


