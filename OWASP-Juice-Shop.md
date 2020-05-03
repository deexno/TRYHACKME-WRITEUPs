# Intro
In the beginning I tried to collect some information, this part is not important for the Writeup (more or less) but I will introduce it here anyway and you are welcome to skip it.

## First I looked at all comments under the products and found the following emails:
* *admin@juice-sh.op
* *jim@juice-sh.op
* *bender@juice-sh.op
* *mc.safesearch@juice-sh.op

## Afterwards I tried to login with the username: ' and the password ' which allowed me to find out how the SQL query is constructed:
--> sql: "SELECT * FROM Users WHERE email = ''' AND password = 'e034fb6b66aacc1d48f445ddfb08da98'"

## And in the robots.txt file I found a subdirectory called: ftp (I will go into this in more detail later)

## I also ran gobuster and found the following subdirectories which might be interesting
* */#/administration
* */#/track-order

<hr>

# TASK 5 
#1 Log in with the administrator's user account using SQL Injection


