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

# Introfuction to Yara R