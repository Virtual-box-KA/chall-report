# Network Forensics

```
You are the forensic investigator tasked with analyzing a packet capture that may contain crucial information regarding Ann's whereabouts after her sudden disappearance. The police chief suspects that Ann might have been in contact with her secret lover, referred to as Mr. X, before she left. Your mission is to decode their communications to determine Ann's movements and recover crucial evidence.

Here are the key pieces of evidence you need to find from the packet capture:

1. Identify Ann’s email address.
2. Determine Ann’s email password. 
3. Find out the email address of Ann’s secret lover, Mr. X.
4. Discover what two items Ann told her secret lover to bring.
5. Ascertain the NAME of the attachment Ann sent to her secret lover.
6. Provide the MD5sum of the attachment Ann sent to her secret lover.
7. Determine in which CITY and COUNTRY the rendez-vous point is located.
8. Find the MD5sum of the image embedded in the document.
```

**Given** - Network Capture file

Steps - I opened the file in networkminer, then started the analysis - 

## Question 1 - Identify Ann’s email address.<br>

From here we can see username - ```sneakyg33k@aol.com```
<br><br><img width="639" height="193" alt="image" src="https://github.com/user-attachments/assets/e1d1af7a-64bb-4e83-b18f-bf1051181526" />

## Question 2 - Determine Ann’s email password.<br>

From here we can see password - ```558r00lz```
<br><br><img width="639" height="193" alt="image" src="https://github.com/user-attachments/assets/e1d1af7a-64bb-4e83-b18f-bf1051181526" />

## Question 3 - Find out the email address of Ann’s secret lover, Mr. X.<br>
Switiching to networking tab given us our answer

Email id of Mr. X - ```mistersecretx@aol.com```
<br><br><img width="652" height="180" alt="image" src="https://github.com/user-attachments/assets/538710dc-5116-4e01-b228-5d1c64530a29" />

## Question 4 - Discover what two items Ann told her secret lover to bring.<br>

Ann told Mister x to bring ```Passport and Bathing Suit```

<br><img width="283" height="254" alt="image" src="https://github.com/user-attachments/assets/70da160d-7413-45eb-8bcd-1d1d0ed96036" />

## Question 5 - Ascertain the NAME of the attachment Ann sent to her secret lover.<br>

Attachment was - ```secretrendezvous.docx```

<img width="292" height="121" alt="image" src="https://github.com/user-attachments/assets/4e54286d-e15b-42f5-a33b-a1f4bd02a783" />

## Question 6 - Provide the MD5sum of the attachment Ann sent to her secret lover.<br>

I then located where the file is being extracted from the mail in my system. Then calculated the md5 hash.

The md5 hash for the file is ```9e423e11db88f01bbff81172839e1923```
<br><br><img width="920" height="41" alt="image" src="https://github.com/user-attachments/assets/882815ad-ddd1-4de4-b57b-6098c010d182" />


## Question 7 - Determine in which CITY and COUNTRY the rendez-vous point is located.<br>

I opened the file to see if i can find any thing, the file had a map which showed a location, with the text _Meet me at the fountain near the rendezvous point. Address below. I’m bringing all the cash._
<br><br> So the location should be ```Playa de Carmen, Mexico```
<br><br> <img width="630" height="175" alt="image" src="https://github.com/user-attachments/assets/92d57b70-cc36-408f-a901-82be8a062aed" />

## Question 8 - Find the MD5sum of the image embedded in the document.<br>

I need to extract the image from the word file, so i used binwalk to do so and got the file.
<br><br>The md5 hash for the embedded image is ```aadeace50997b1ba24b09ac2ef1940b7```
<br><br><img width="1162" height="38" alt="image" src="https://github.com/user-attachments/assets/e87f2566-a6df-4679-af85-892979206795" />

