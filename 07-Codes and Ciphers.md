## All the Base  
**Value** "15"  
**Clue** "Please decode the attached message.  
**Hint** ""  
**Flag** "BTC{An.Imbalance.in.the.Poppability!}"  

For this challenge, a text file with the string 
`FH8+N8AC8E%5C$DAECCECKPC1*5 -DAWERZCQ7AT9E0ECXED-ED4EFZ2` 
was provided with instructions to decode.  Leveraging the dencode.com engine, I was able to see quickly that the string was Base45 encoded.  Decoding the string produced the flag. 

## Last Minute Cypher  
**Value** "10"  
**Clue** "Decode the following file"  
**Hint** ""  
**Flag** "BTC{GeneralMajorWebeloZappBrannigan}"  

This challenge included a text file with a fairly obvious pattern (xxx{}) which initially led me to believe that I was dealing with a mono-alphabetic substitution cypher.  However, upon further inspection, I found that the encryption technique used was actually Vignere.  This was solved using an online decoder tool. 

**Ciphertext**  
`Tf ox tqg naee bmexarsx, xse jxeb bz mlp dgfuvbyl atld ymty fbop a zhgar iy glrvl. Oprwdqltw. UFK{TygicadFmrblPimedhLicjUvlnfbsia}`

**Decoded Text**  
If we hit that bullseye, the rest of the dominoes will fall like a house of cards. Checkmate. BTC{GeneralMajorWebeloZappBrannigan}
