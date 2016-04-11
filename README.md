# Hob0Rules
Password cracking rules for Hashcat based on statistics and industry patterns.
The following blog posts on passwords explain the statistical signifigance of these rulesets:

[Statistics Will Crack Your Password](https://www.praetorian.com/blog/statistics-will-crack-your-password-mask-structure)

[Praetorian Password Cracking Rules Released](https://www.praetorian.com/blog/hob064-statistics-based-password-cracking-rules-hashcat-d3adhob0)

Useful wordlists to utilize with these rules have been included in the wordlists directory 

Uncompress these with the unfollowing command 
```
gunzip rockyou.txt.gz
```
##hob064 
This ruleset contains 64 of the most frequent password patterns used to crack passwords. Need a hash cracked quickly to move on to more testing? Use this list.
```
hashcat -a 0 -m 1000 <NTLMHASHES> wordlists/rockyou.txt -r hob064.rule -o cracked.txt
```

##d3adhob0
This ruleset is much more extensive and utilizes many common password structure ideas seen across every industry. Looking to spend several hours to crack many more hashes? Use this list.
```
hashcat -a 0 -m 1000 <NTLMHASHES> wordlists/english.txt -r d3adhob0.rule -o cracked.txt
```
