# Hob0Rules
Password cracking rules for Hashcat based on statistics and industry patterns.
The following blog posts on passwords explain the statistical signifigance of these rulesets:

[Statistics Will Crack Your Password](https://www.praetorian.com/blog/statistics-will-crack-your-password-mask-structure)

[Praetorian Password Cracking Rules Released](https://www.praetorian.com/blog/password-rules-released)

Useful wordlists to utilize with these rules can be downloaded from the following locations:

[Rockyou Password Dump](http://downloads.skullsecurity.org/passwords/rockyou.txt.bz2)

[English Wordlist](http://downloads.skullsecurity.org/passwords/english.txt.bz2)

Uncompress these with the unfollowing command 
```
tar -zxjf rockyou.txt.bz2
```
##hob064 
This ruleset contains 64 of the most frequent password patterns used to crack passwords. Need a hash cracked quickly to move on to more testing? Use this list.
```
hashcat –a 0 –m 1000 <NTLMHASHES> wordlists/rockyou.txt -r hob064.rule -o cracked.txt
```

##d3adhob0
This ruleset is much more extensive and utilizes many common password structure ideas seen across every industry. Looking to spend several hours to crack many more hashes? Use this list.
```
hashcat –a 0 –m 1000 <NTLMHASHES> wordlists/english.txt -r d3adhob0.rule -o cracked.txt
```
