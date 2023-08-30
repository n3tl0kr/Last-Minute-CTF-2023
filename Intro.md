## Rules

**Value** "5"  
**Clue** "Read the Rules. Under stand the Rules. Follow the Rules.""  
**Hint** ""  
**Flag** "BTC{c6d18f3d857bda2f41e605d6ca81c80c}"  

1. Navigate to the [Last Minute CTF](http://44.201.80.76/) dashboard and then to the **Rules** section. 

2. The flag can be found on this page by expanding certain sections of text.
<img width="1129" alt="Pasted image 20230825182503" src="https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/156bea76-c62c-4f3e-a5b5-ff24ee1fa0a5">

## Writeups

**Value** "5"  
**Clue** "Learn about Challenge Writeups and Challenge Guides."  
**Hint** ""  
**Flag** "BTC{B0nusP01ntsM4keM3H4ppy--}"  

1. Navigate to the [Last Minute CTF](http://44.201.80.76/) dashboard and then to the **Writeups** section. 

2. Reading through the page, there is an *Example Writeup* section that includes instructions for this challenge.
<img width="1131" alt="Pasted image 20230825182947" src="https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/ad5402bc-d334-4b09-a025-544d6498566e">

3. View the sourcecode of the writeups.htm page which includes the flag as directed.  The process to do this may vary depending on the web browser being used.
<img width="1294" alt="Pasted image 20230825183403" src="https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/53ad49fe-9698-4f00-b7a9-71b913bd2843">

## Not for Humans
**Value** "10"  
**Clue** "Having completed your introductory tour of our CTF, we invite you to explore a little more to find two additional flags that have been hidden on our site. The first is hidden in a place not designed for humans..."   
**Hint** ""  
**Flag** "BTC{1fY0uC4nR34dTh1sY0u'r3@N3rd=}"  

So, during a previous challenge, I noted that the robots.txt file in the root of the CTF server contained multiple bologna entries.  

![image](https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/5a68d796-4991-4604-a96a-e62aa4d5a744)

One of these in particular caught my attention amid an ocean of easter eggs. 

![image](https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/a0c57b8a-c650-4c15-897e-1b13c38013f2)

This file mentions another file that is not listed in the robots digest which tells me that there may be other hidden files as well.  However, navigating to the next hop here leads to another riddle so to say. 

![image](https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/0ce03f0d-21c1-46e3-90bb-48d7811817dc)

Now we try to navigate to `../mystery.html` and poof, all of the sudden I'm looking at Chapter 1 of Alice In Wonderland, how cute. 

![image](https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/b01ac1a1-e78b-442d-bc5c-378f8e9494c3)

