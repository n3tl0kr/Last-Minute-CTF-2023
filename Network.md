## They See Me Rolling...  
**Value** "15"  
**Clue** "Please monitor the following log server for updates on flags."  
**Hint** ""  
**Flag** "BTC{A novel about Яussian Gulags.}"  

For this challenge, we are asked to listen to a port on a remote server.  
`> nc 54.163.140.212 33333`
In order to complete this challenge, I did connect to this remote service and piped all of the output to both an external log file and to the terminal.  After several minutes of garbage output, the actual flag was represented as "packet # 1260". 

## System Flag Interface
**Value** "20"  
**Clue** "The Last Minute Team has setup a new System Flag Interface. You may access the interface at the following location:
`ncat 54.163.140.212 20202"`  
**Hint** ""  
**Flag** "BTC{No-*s-4-naughty-boys!}"  

This challenge forces you to interact with a flag generator application reminiscent of the Jurassic Park computer system.  

1. Connect to the socket with netcat
2. Interacting with the system and providing the wrong input results in "You didn't say the magic word" 
3. The `HELP` command displays several commands but no other input is allowed. 
4. Found that appending `please` to the beginning of any command will successfully execute. 

## Flag Server v2
**Value** "30"  
**Clue** "We have upgraded the Last Minute Flag Server to version 2. Please grab one of the new flags from the new Last Minute Flag server: disabled"  
**Hint** ""  
**Flag** "" 

Unfortunately, this challenge was not completed!
