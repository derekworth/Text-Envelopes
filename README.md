![alt text](https://github.com/derekworth/Text-Envelopes/blob/master/lib/e300.png "Envelopes Logo")

# Text-Envelopes

A simple, yet robust way to track all financial activities in your life.

### Overview

Regardless of where your money physically resides, you need to have a plan on how it is allocated in your life.  This simple application is based on the principle that every penny should have a name.  That is, you should tell your money how to behave by tracking and categorizing every financial transaction you make.  Whether it's buying soda from a vending machine or putting a down-payment on a new home, that money has to come from somewhere.  You make your money work for you when you know exactly where it's coming from and intentionally direct it where to go.

This application enforces this behavior by associating every transaction to a single Account (physical location) and a single Envelope (allocation).  That way, you always know, for example, exactly how much you have in your checking account (physical location) and how much you have left to spend on groceries for the month (allocation).

You start with empty Accounts and Envelopes.  You fill them by adding positive transactions.  You deplete them with negative transactions.  Additionally, you can transfer funds between accounts (e.g. ATM withdrawal is a transfer from your 'checking' account to your 'cash' account) or between envelopes (e.g. distributing funds from your 'income' envelope to all your other envelopes during your monthly budgets).  Each transfer will link two transactions (updating one will automatically update the other).

### Getting Started
1) Install the latest version of Java; see https://www.java.com/en/download/
2) Download and extract this repository to your computer (use the "Clone or download" dropdown and click on the "Download ZIP" button)
3) Start the program by double-clicking on the Envelopes.jar.    NOTE: you may need to update your system PATH variable to run java applications; see https://www.java.com/en/download/help/path.xml
3) Once program is running, log in as admin; default password is "password"
4) From here, change your username from "admin" to something else (like your first name) and update your password to something you won't forget
5) Add other users who will share financial responsibilities in your household (e.g. spouse)
6) Add transactions and transfers to keep your finances up-to-date

### Remote Access (via iPhone App)
First, you will need to enable port forwarding from your home router to the computer running the Envelopes server.
1) Login to your router
2) Navigate to your router's __port forwarding__ section, also frequently called __virtual server__
3) Create the port forwarding entry that points traffic to the computer running your Envelopes server (to private IP address over __port 8456__)

Next, you will need to install and configure the App

4) Install the Envelopes.ipa file (i.e. the remote client) ![alt text](https://github.com/derekworth/Text-Envelopes/blob/master/lib/e40.png "Envelopes Logo") using the directions posted here: https://docs.monaca.io/en/products_guide/monaca_ide/deploy/non_market_deploy/
5) From the computer running the Envelopes server, open a browser and navigate to https://www.whatismyip.com/ to identify your public IPv4 address--this will be the IP address you enter in the App
6) In the App, enter your username, password, and IP address (make sure you click the __Done__ button to save for each field)
7) Test your connection by sending __help__ from the App... and that's it, you are connected! See below for usages.

NOTE: You may need to adjust firewall rules within your network to allow Envelopes network traffic.


USAGES:
(optional), [1 or more], \<replace\>

--add new transaction(s)--\
(date) \<acc\> [\<env\> \<amt\> (desc), ...]

--add new transfer--\
\<from acc\> \<to acc\> \<amt\>\
\<from env\> \<to env\> \<amt\>

--add new account/category/envelope/user--\
new acc/cat/env \<name\>\
new env \<name\> (cat)\
new user \<name\> \<password\>

--view amounts/transactions--\
accounts/categories/envelopes/users\
\<acc/cat/env\>\
history (\<acc\>/\<env\>) (\<qty\>/\<date\> \<date\>)

--modify--\
\<from\> \<to\> \<amt\> (desc)\
rename acc/cat/env/user \<old\> \<new\>\
remove acc/cat/env/user \<name\>\
change password \<pw\>\
\<env\> \<cat\>

For example, if you wanted to create a new category named 'big purchases', send the message "new category big-purchases" (or "new cat big-purchases" for short), and this application will respond with a message saying your new category was created.

If you wish to add a transaction that reflect you spending cash on a video game, you would use the "\<acct\> \<env\> \<amt\> (desc)" command and it would look something like "cash entertainment -39.99 Space Invader video game from GameSpot".

Try sending the word "categories" or "cat" for short and see what it returns.

If you have any questions about this application, recommendations for improvement, or just want to share your experience with it, I'd love to hear from you, derek84worth@gmail.com.  I hope you enjoy using this application!

Last Updated: 2020-12-29
