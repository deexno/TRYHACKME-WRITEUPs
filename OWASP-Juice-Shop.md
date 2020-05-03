# Intro
In the beginning I tried to collect some information, this part is not important for the Writeup (more or less) but I will introduce it here anyway and you are welcome to skip it.

<details><summary>Show Intro</summary>

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
</details>

# TASK 4

<details><summary>TASK 4</summary>

## #1 Log in with the administrator's user account using SQL Injection

At this task we try to log in as the administrator without knowing his password or his Email-address 

1. First we read the SQL statement which we have discovered
(sql: "SELECT * FROM Users WHERE email = ''' AND password = 'e034fb6b66aacc1d48f445ddfb08da98'")

2. By using the SQL statement we can see that we can skip the verification of the password with:

' OR 1=1 --

If we now login with the following credentials we will see that we are logged in as the administrator

Email: ' OR 1=1 --
Password: '

<img height="400" src="img/login.png"><br>

<img height="250" src="img/admin.png">

</details>



