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

At the bottom of this page I find another hyperlink, this time a `myster2.html` page. I have to admin that I'm slightly intrigued at this point. 

![image](https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/25dda6d3-5198-4eb2-98a7-e7f25367ff7d)

Alright, proof of chapter 2!  But wait, theres another chapter at the bottom of the page but this is no hyperlink. 

![image](https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/ce794cc4-1038-4bc0-84b8-31a5d63b85e8)

After inspecting the source of the page, I find a malformed comment containing a reference to another html page. 

![image](https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/059a53fc-c982-4874-bdb6-c78bf56e24b6)

This next chapter looks a little more strange with a long list of reference links.  However, only one of them appear to be functional (`../aliceIV.html). 

![image](https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/bcec669c-c8a3-40d5-acef-bd396503d085)

The next page appears broken as well so taking the clue from the source code, we add a roman numeral to the URL. (`../Chapter(#).html` to `../ChapterVI.html`.  

Moving along, this page contains a link for another `html` page, however the page link is missing a '.' before `html`.  Fixing that takes us to yet another page. `(../mad-tea-party.html)`

![image](https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/78260097-17b2-4e50-8723-6b1c253392a8)

And another trick! Lets check out `view-source.txt`!

<img width="1118" alt="image" src="https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/3917ac42-aa55-4ab9-be33-16e294f8ecc6">

From here, we are faced with another broken hyperlink.  This time, `turtle.html` seems to do the trick.

<img width="1120" alt="image" src="https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/89e6cff4-a2d8-4b34-a5fc-7fb41fd20d2a">


As you can see below, things are really getting wild now.  

<img width="1117" alt="image" src="https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/cc2cd92d-b6dd-4ad2-b118-76d6e3baf5ff">

This appears to be a clue, 2/3 of the next chapter.  "The Lobster" or "Lobster Quadrille" are the first things that come to mind, lets check it out!  `LobsterQuadrille.html` works!  Lets go!

Now looking at the bottom of the Lobster page, we have another crafty little trick.  This type, there appears to be a hyperlink written backwards! `lmth.ChapterXI"=FERH"` should read `HREF="IXretpahC.html"`

<img width="1080" alt="image" src="https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/d756da0a-4d08-4a35-b47f-a6970211f48e">

And now some URL encoded nonsense!  But a quick mouseover shows the actual link. 

<img width="1114" alt="image" src="https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/f969b251-11eb-4a91-99c5-24207b26be51">

