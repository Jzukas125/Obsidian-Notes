These notes are taken on the YARA room on tryhackme
Prerequisites: Basic Linux Familiarity
This room will cover a basic introduction for YARA and familiarize us with its rules and functions.

# Introduction to YARA

Yara can identify information based on both binary and textual patterns, such as hexadecimal and strings contained within a file. Rules in YARA are used to label these patterns such as rules frequently being written to determine if a file is malicious or not, based upon the features or patterns it presents. Stings are a fundamental component of programming languages. Applications use strings to store data such as text. 
For example the code snippet below prints "Hello World" in Python. The text "Hello World" would be stored as a string.
```python
print("Hello World!")
```
We could write a Yara rule to search for "hello world" in every program on our operating system if we would like.

Why does Malware use strings? Malware uses strings to store textual data.

# Introduction to Yara Rules

The language that Yara uses for rules is fairly trivial to pick up, but hard to master. This is because your rule is only as effective as your understanding of the patterns you want to search for.

Using a Yara rule is simple. Every Yara command requires two arguments to be valid, these are:
1) The rule file we create
2) Name of file, directory, or process ID to use the rule for

Every rule must have a name and condition. For example if we wanted to use "myrule.yar" on directory "some directory", we would use the following command: 'yara myrule.yar somedirectory'
Note that .yar is the standard file extension for all Yara rules. We'll make one of the most basic rules below.
1. Make a file named somefile via touch somefile
2. Create a new file and name it "myfirstrule.yar" like below 
```shell
touch somefile
touch myfirstrule.yar
```

3. Open the "myfirstrule.yar" using a text editor such as nano and input the snippet below and save the file 
```shell
rule examplerule {
	condition: true
}
```

The name of the rule in this snippet is examplerule, where we have one condition - in this case, the condition is condition. Simply, the rule we have made checks to see if the file/directory/PID that we specify exists via condition: true. If the file does not exist, we are given the output of examplerule. Let's give this a try on the file "somefile" that we made in step one: yara myfirstrule.yar somefile

If "somefile'" exists, Yara will say examplerule becasue the pattern has been met 
```shell
yara myfirstrule.yar somefile
examplerule somefile
```
If the file does not exist, Yara will output an error such as:
```shell
yara myfirstrule.yar sometextfile
error scanning sometextfile: could not open file
```

# Yara Conditions Continued 

<h2> Meta </h2>
Reserved for descriptive information by the author, can use the desc to summarize what checks are for .

<h3> Strings </h