<img width="1584" height="192" alt="image" src="https://github.com/user-attachments/assets/f3027ac7-4b77-4e8b-b877-36fc39aaface" />

# 🔍 LAB - Disk Analysis & Autopsy
Room Link: https://tryhackme.com/room/autopsy2ze0

# Introduction:
Disk forensics is the process of extracting forensic information for storage mediums like HDD, USB devices , firmware etc.
In order to forensically analyze a disk, you will need to create a forensic image of the drive.
A forensic image is an exact digital copy of a physical drive and the data contained within it.

Autopsy:
Autopsy is a free open-source digital forensics tool that can be used to perform forensic analysis on disk images.
Autopsy can be used to extract useful information and artifacts from a disk image like:

------
**Platform:** TryHackMe  
**Category:** Disk Forensics  
**Difficulty:** Medium 
**Tool Used:** Autopsy 

---

<img width="602" height="396" alt="image" src="https://github.com/user-attachments/assets/8389488f-89e9-4c34-b7ae-0ee1bcaae3dd" />

Create a new case by clicking it , after that you need to provide two information

1. Provide Case information
2. Provide optional information like the case number , mail ,number ,etc.

<img width="611" height="456" alt="image" src="https://github.com/user-attachments/assets/da1ea62e-3f59-4514-97d4-18ee0ff74f9e" />

   
1. Select Host
There you can select the option Generate new host name based on data source name or you can also specify a new host name.

<img width="472" height="436" alt="image" src="https://github.com/user-attachments/assets/6fa16aad-aecc-4d7c-a813-aa648b19e04f" />

2. Select Data source type
Based on the type of data we are giving we had to choose form the below ,
in our case we have to choose Disk Image.
And in case we are using an external USB then we can choose Local Disk.

<img width="650" height="202" alt="image" src="https://github.com/user-attachments/assets/fb4caf57-12e5-40ed-a713-d75633f3f656" />

3.Select Data source
Choose the disk image from where you have saved them.


<img width="296" height="358" alt="image" src="https://github.com/user-attachments/assets/3e512cc3-b20e-4e31-ad25-968f17c0535f" />

4. Configure Ingest
Ingests are very important as they allow you to perform various functionalities, and process your disk image
They provide:

----
Once your data source has been processed, we will able to see the navigation tree where all the extracted data will be there. We will be able to see the data sources , File views , Data artifacts , Analysis results , etc.

Now, under the data sources choose NTFS that is where Windows is installed, so that’s the default drive.

We can see the listing window , there in columns ‘S’ denotes the scores which tells us the whether an item is notable or interesting , ‘C’ denotes comments where you can essentially add comments and ‘O’ denotes the number of occurrence of files or folders.

Press enter or click to view image in full size

<img width="1100" height="491" alt="image" src="https://github.com/user-attachments/assets/6e877855-0364-4b57-be5b-de8df773d9e3" />

And at the bottom we will have the ability to view the data in the form of Hex, Text , File Metadata ,Data Artifacts , etc.

<img width="778" height="238" alt="image" src="https://github.com/user-attachments/assets/e9b91fc8-aadf-459a-b837-77d65fa0b2f8" />

Everything is set now . i leave the rest to you . your task is to do manual analysis of the artifcats discovered by autopsy and Find the answers . see ya !!!

<img width="736" height="585" alt="image" src="https://github.com/user-attachments/assets/46fa0ec9-219e-4e0c-b75f-e9a3647f0697" />



## Conclusion
In conclusion, the use of Autopsy for disk analysis proves to be an invaluable asset in the realm of digital forensics.
As technology continues to evolve, tools like Autopsy remain essential in the fight against cybercrime, ensuring that justice is served and digital evidence is meticulously examined to uphold the integrity of investigations.

---


