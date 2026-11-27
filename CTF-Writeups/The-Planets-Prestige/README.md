**The Planet's Prestige BTLO Challenge CTF investigation Report**

Scenario

CoCanDa, a planet known as 'The Heaven of the Universe' has been having a bad year. A series of riots have taken place across the planet due to the frequent abduction of citizens, known as CoCanDians, by a mysterious force. CoCanDa’s Planetary President arranged a war-room with the best brains and military leaders to work on a solution. After the meeting concluded the President was informed his daughter had disappeared. CoCanDa agents spread across multiple planets were working day and night to locate her. Two days later and there’s no update on the situation, no demand for ransom, not even a single clue regarding the whereabouts of the missing people. On the third day a CoCanDa representative, an Army Major on Earth, received an email.


### Findings

- **Recipient:** Army Major on Earth (`themajor@gmail.com`)
- **Attacker's Host:** `emkei.cz` (`93.99.104.210`)
- **Spoofed Sender Address:** `billjobs@microapple.com`
- **Reply-To Address:** `negeja3921@pashter.com` (differs from the sender address)
- **Email Encoding:** The email contained Base64-encoded content.
- **Malicious Attachment:** An attachment named `PuzzleToCoCanDa.pdf` was discovered to be a ZIP archive containing JPEG, PDF, and XLSX files.
- **Decoded Payload:** Base64-encoded content found inside the XLSX file decoded to reveal the attacker's location: *The Martian Colony, Beside Interplanetary Spaceport*.
- **Metadata Analysis:** Attachment metadata identified the author as **Pestero Negeja**.


**Investigation summary**

The Army Major on earth, received an email from a sender named Bill. This email is related to the whereabout of the President daughter and the missing people. During investigation of the email,  it was discovered that the email sender address was spoofed because the email was sent using a third-party email service, the reply-to was to a different sender and the SPF result returned fail. The attachment disguised as PDF was found to be a zip file containing three files and clues for finding the location of the attacker. The location of the attacker was discovered to be  The Martian Colony, Beside Interplanetary Spaceport while the name of the attacker was identified as Pestero Negeja after checking the metadata of the attachment.     


**Who**
- **Target:** Army Major on Earth (`themajoronearth@gmail.com`)
- **Impersonated Identity:** (`billjobs@microapple.com`)
- **Reply-To:** `negeja3921@pashter.com` 
- **Suspected Attacker:** Pestero Negeja

**What:**
- A suspicious email was sent to Army Major on earth representing CoCanDa.
- The email contained base64 encoded content and zip file disguised as PDF attachment. 
- The attached file contains hidden information related to the abductions.  

**Where:**
- Target Environment: Army Major on Earth
- Attackers domain:emkei.cz
- Suspected attackers location:The Martian Colony, Beside Interplanetary Spaceport
 

**When:**
- Time email was received : 2021-01-25 22:41:18 -800 (PST)

**Why:**
- The suspect motivation was kidnapping and ransom

**How:**
- The attacker used a spoofed email to send to the target.
- The attacker used the domain emkei.cz
- The attacker use base64 encoding to conceal the email content. 
- Zip file disguised as PDF attachment
- Hidden files and spreadsheet content were used to conceal additional information.

**Recommendation**
- Preserve the original phishing email and attachments for investigation.
- Block the identified malicious sender address and associated domains after evidence collection.
- Quarantine or remove similar phishing emails from affected mailboxes.
- Search for other recipients who may have received the same email.

**Tools used**
- Notepad ++
- CyberChef
- Exiftool
- HxD
- Openoffice
