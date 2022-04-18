# CVE-2022-27254
PoC for vulnerability in Honda's Remote Keyless System(CVE-2022-27254)


# Disclaimer:
*For educational purposes only.*
Kindly note that the discoverers for this vulnerability are [Ayyappan Rajesh](https://www.linkedin.com/in/ayyappan-rajesh/), a student at UMass Dartmouth 
 and [HackingIntoYourHeart](https://github.com/HackingIntoYourHeart/). 


**Others mentioned in this repository are credited for the support that they have provided but have played no active role in any   research conducted related to this finding. 
If looking to publish these findings elsewhere, please refrain from associating this with any other persons, companies or institutions without any explicit approval.**
 
 ## Summary:
 
This is a proof of concept for [CVE-2022-27254](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-27254), wherein the remote keyless system on various Honda vehicles send the same, unencrypted RF signal for each door-open, door-close, boot-open and remote start(if applicable). This allows for an attacker to eavesdrop on the request and conduct a replay attack.

## POC videos:
[Remote Start](https://user-images.githubusercontent.com/5160055/159138537-2904b448-af1c-4a89-af08-b53a4d77a277.mp4)

[Door Unlock](https://user-images.githubusercontent.com/5160055/159138551-e9ab24fa-a05c-4fc8-ad1c-f1dcda698bcc.mp4)

[Door Lock](https://user-images.githubusercontent.com/5160055/159138581-eb844936-9999-4234-a5c0-fa7412df193b.mp4)



## Vehicles Affected:

• 2016-2020 Honda Civic(LX, EX, EX-L, Touring, Si, Type R)

## Important Notes:
 
     •Key fob FCC ID: KR5V2X

     •Key fob frequency: 433.215MHz

     •Key fob modulation: FSK


## Tools used: 
           
           •FCCID.io
           •HackRF One
           •Gqrx
           •GNURadio



## Prevention:
  - Manufacturers:
    1. Manufacturers must implement Rolling Codes, otherwise known as hopping code. It is a security technology commonly used to provide a fresh code for each authentication of a remote keyless entry (RKE) or passive keyless entry (PKE) system.


  - Consumers:
    1. Utilize a Faraday Pouch for the key fob.
    1. Use the PKE as opposed to the RKE, this would make it significantly harder for an attacker to clone/read the signal due to the proximity they would need to be at to do so.
 
⚠️ The precautions mentioned above ARE NOT foolproof ⚠️

If you believe that you are a victim of this attack, the only current mitigation is to reset your key fob at the dealership.


## Credits:
•[Ayyappan Rajesh(nonamecoder)](https://www.linkedin.com/in/ayyappan-rajesh/) 

•[HackingIntoYourHeart](https://github.com/HackingIntoYourHeart/) 

## Special thanks to:
• My professor :[Prof. Hong Liu](https://www.umassd.edu/directory/hliu/) 

• My mentor:[Sam Curry](https://www.linkedin.com/in/currysam) 

•My professor :[Prof. Ruolin Zhou](https://www.umassd.edu/directory/rzhou1/) 


## Reference :

•https://attack.mitre.org/techniques/T1040/

## Tanks to My bro
   
  • Mr Ayappan



## MDOS

         _   _   _____
        | \ | | |___ /
        |  \| |   |_ \
        | |\  |  ___) |
        |_| \_| |____/
	       surya N3
