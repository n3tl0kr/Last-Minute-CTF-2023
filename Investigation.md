## Investigation  
**Value** ""  
**Clue** "Using the provided file, answer the following questions about the incident:
          What was the failed password attempted?  
**Hint** ""  
**Flag** "BTC{BTCpassword1}"  

For this challenge, I was actually very surprised at the speed in which the flag was found.  I simply opened the provided PCAP with Wireshark, a well known protocol analyzer.  Using this tool, I was able to find the FTP session in which the authentication for the service was submitted and failed.  Because FTP is a plaintext protocol, all of this information is shown readable in the traffic capture. 
