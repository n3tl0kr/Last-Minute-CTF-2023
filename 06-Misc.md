## Hidden  
**Value** "10"  
**Clue** "Please recover the redacted flag from this file."  
**Hint** ""  
**Flag** "BTC{What_kind_of_PictureS?}"  

In order to solve this challenge, a PDF document was downloaded from the challenge site.  This documented seemed to drone on and on about a football match.  Knowing the format of the flag, I simply ran a free text search in the pdf for the string "BTC{" which presented the text underneath of an overlay color block.  

<img width="912" alt="Pasted image 20230826123957" src="https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/72c9c54d-225f-42d4-bc00-41ca74395a54">

## Did Someone Find My Blue Team Con Key?
**Value** "10"   
**Clue** "If you find my key, I hope you know what to do with it."  
**Hint** ""  
**Flag** "BTC{SSH_AND_NO_ROOT_FILES_YET}"  

This challenge actually relies on another challenge in the [Forensics](05-Forensics.md) category. With the file provided (`file.fs`) from the **Finders Keepers** challenge:

1. On a Linux system, create a folder 
  `mkdir -p /mnt/test`
2. Mount the .fs file as an EXT3 partition
  `sudo mount -t loop file.fs /mnt/test`
3. Within the newly mounted partition, we find a file containing an SSH private key.

<img width="965" alt="image" src="https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/ed127f44-f84f-4f2e-8c0e-85ee7810945b">

4. With this key captured, we can actually connect to the server mentioned in the file name using standard SSH.  First, we will copy the key out and modify the name for ease of use and then use the useraccount and IP address combination first observed in that file name. 

```
┌──(kali㉿kali)-[/mnt/test]
└─$ cp blueteamcon@159.203.84.152 ~/Desktop/ssh.key
                                                                                                                                                                
┌──(kali㉿kali)-[/mnt/test]
└─$ cd ~/Desktop                                   
                                                                                                                                                                
┌──(kali㉿kali)-[~/Desktop]
└─$ ls
Blueteamcon  file.fs  spiral.txt  ssh.key  Theres_more
                                                                                                                                                                
┌──(kali㉿kali)-[~/Desktop]
└─$ ssh -i ssh.key blueteamcon@159.203.84.152
```
5. Run "cat .flag" and the flag will output to the screen
   
![image](https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/605fab4a-7cf9-4080-8f72-4b2b3a6c7395)

6. The final flag is BTC{SSH_AND_NO_ROOT_FILES_YET}

## De...Code  
**Value** "10"  
**Clue** ""  
**Hint** ""  
**Flag** "BTC{QRCODESBYTOM}"  

This challenge provided a text file called `readme.txt` which contained a series of bash color codes. When read in a terminal with cat, it produces a QR code which is actually a flag.

<img width="440" alt="Pasted image 20230826163555" src="https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/547f32a7-e289-4069-be84-5e0aa85ac979">

## Talkative
**Value** ""
**Clue** ""
**Hint** ""
**Flag** ""

## Searching  
**Value** ""  
**Clue** "To assist with building challenges, we created a service to generate flags for us. Unfortunately it isn't quite working as expected. Retreive the flag from the tool output."  
**Hint** ""  
**Flag** "BTC{68b40d89dffab559e8f5d273028a0472}"  

For this challenge, we are provided with a very large text file.  In order to quickly parse this text file, I simply grepped the text file for the string `BTC{` which revealed the flag as shown. 
```
❯ head BTC-1M.txt
uSt<D5pOZOjNd3eS8INW2RGQ6yr5TW8jORepgIZyMn41nfqQ92jGinVSTwClqNbtUHk6phsRnBLZdBIwb1Fi}
nnN(vLCCAmIm43BHPAyf1y8KgrwdSlCgCTfWb0BCUkF8EaSvEwlFAuGpZzuvYC6xDuxXR0Sv6n6v3nvw9eRlHC)
hEL<D0XbPM2jLKOSExnDVutAbzwrtpbbbmrmLEQcGS2CQLmba1r1i7RjEmyE1aoW1isw
lkm[sYnNvwtnweFrMS13flPnlE2TG6HxNlbj8mDqTACYxTgwZYdjhGhURVTR3UbHQ2wlYSvy29JLdbuH5FXxMlpDscsmhPOZWD]
uHj(j8ydrZeS7FwQ9QFCcof88TydCQ7enVivdyqJiL8t90R>
FEf<zriuReVL7OW076YVkRUmVyVJ1SYpzLVM6Hyj3TmbQH3rLCgFvEGx0UQQIPdUfxZBZnC3s07ORz5
hXCpinch.studio1THULIUM]
HBT<FHFTdxf4d7HXdh3SA91W0hUlLcY6XT2VX>
zcH(JHynSJOh0diFq77xJgMXsuJYvLjnUDZ8oWrvt4BlBiSDK0TnKbKSCWcdmXHvJzXEpEXS)
Xjg 7yRkH1zcesI
❯ grep BTC{  BTC-1M.txt
BTC{68b40d89dffab559e8f5d273028a0472}
```

## Black Boxes  
**Value** "10"  
**Clue** "Please recover the message hidden in the following files."  
**Hint** ""  
**Flag** "Flagequalsiiiiiiiiiieightsevenend (submitted as BTC{iiiiiiiiiieightsevenend})"  

In this challenge, I was provided with four different text files but there appeared to be nothing obvious about any of them.  After analysis was exhausted, I began to work with other challenges until receiving a notification from the challenge administrators stating that an issue had been fixed.  Upon reviewing the new files, I found that certain characters were blacked out in in the file `num1.txt`.    The files were compared directly and all of the obfuscated characters were collected to complete the flag.   

<img width="682" alt="Pasted image 20230826183925" src="https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/bd636454-2971-409c-9eb0-e4f41bb3e4aa">

## Feedback
**Value** ""  
**Clue** "Please click on the following link and respond with feedback on the CTF. We would very much like to know what you enjoyed as well as your favorite challenge(s).
          https://forms.gle/4tC623VP7ZSNTMJf9
          We're giving this a good amount of points as we're very interested in the responses."  
**Hint** ""  
**Flag** "BTC{Thanks.for-the_feedback!}"  

This challenge is self explanatory and the flag is provided once the survey is completed!

<img width="756" alt="image" src="https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/a5fdc427-0cfc-4492-81c7-15ba7dcaad3b">

