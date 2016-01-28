# Hob0Rules
Password cracking rules for Hashcat based on statistics and industry patterns.

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
