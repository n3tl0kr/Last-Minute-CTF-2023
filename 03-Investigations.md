## Investigation  
**Value** "15"  
**Clue** "Using the provided file, answer the following questions about the incident:
          What was the failed password attempted?  
**Hint** ""  
**Flag** "BTC{BTCpassword1}"  

For this challenge, I was actually very surprised at the speed in which the flag was found.  I simply opened the provided PCAP with Wireshark, a well known protocol analyzer.  Using this tool, I was able to find the FTP session in which the authentication for the service was submitted and failed.  Because FTP is a plaintext protocol, all of this information is shown readable in the traffic capture. 

<img width="856" alt="Pasted image 20230826131137" src="https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/2550b2d5-fbf6-402e-9d95-b0755902a015">

## Investigation 1-b  
**Value** "15"  
**Clue** "Using the provided file, answer the following questions about the incident:   
	What was the correct password?"  
**Hint** ""  
**Flag** "BTC{BTCpassword!}"  

Using the same logic as above, a second authentication attempt to the FTP service was also observed with correct credentials as shown below. 

<img width="1131" alt="Pasted image 20230826131523" src="https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/581d4451-2c91-43ff-8f37-3c544436c40c">

## Investigation 1-c  
**Value** "15"  
**Clue** "Using the provided file, answer the following questions about the incident: What is the md5 hash of the first file transferred?"  
**Hint** ""  
**Flag** "BTC{564e139b32715d622f635d7e881866ad}"  

Along with a packet capture, an OVA was also included as a forensic copy of the affected workstation.  Upon further review of the network traffic, I found that a specific file was downloaded first according to the FTP traffic observed. 

<img width="981" alt="Pasted image 20230826132334" src="https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/a0c4f40f-1364-4f43-8bb9-b3e696d6fb61">

This file `DqKJayFVYAEr2iZ.jpeg` was located within the /Users/frankb/Pictures directory on the workstation and the filehash was collected and submitted as such. 

<img width="912" alt="Pasted image 20230826132140" src="https://github.com/n3tl0kr/Last-Minute-CTF-2023/assets/43141524/7d91db10-dae3-4887-8f7f-41d91dbc5484">

## Investigation 1-d  
**Value** "15"  
**Clue** "Using the provided file, answer the following questions about the incident:
          Where was the second file transferred to? (full path)"  
**Hint** ""  
**Flag** ""  

Unfortunately, this challenge was not solved!

## Root Cause Analysis 
**Value** "25"
**Clue** "bluteamcon. Go find the goods."
**Hint** ""
**Flag** "" 

Unfortunately, this challenge was not solved!
