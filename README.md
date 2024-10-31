# Project: Wireshark Basics Exploration

## Objective
The goal of this project is to explore basic functionality within Wireshark by analyzing a `.pcapng` file. I answer specific questions by investigating packet details, identifying flags, calculating hashes, and locating embedded files. This serves as an introduction to network analysis techniques in Wireshark.

## Skills Learned
- Navigating and filtering packets in Wireshark
- Extracting information from packet captures
- Calculating hash values (SHA256, MD5) from packet data
- Identifying strings and metadata within captured network traffic
- Using expert info and comments sections to troubleshoot and locate data

## Tools Used
- **Wireshark**: For packet analysis and filtering
- **Hashing Utility**: For SHA256 and MD5 hash calculation (within Wireshark)
- **Linux OS**: Ubuntu-based system for file handling and navigation

## Steps

### 1. Capture File Comment Identification
- **Task**: Read the "capture file comment" to find the flag.
- **Solution**: Located the flag within the comment section, which revealed "TryHackMe_Wireshark_Demo."

   ![Capture File Comment](https://github.com/user-attachments/assets/2d069cf5-586e-409b-b992-20ff2cddf1f3)


### 2. Counting Total Packets
- **Task**: Determine the total number of packets in the capture file.
- **Solution**: Identified a total of `58620` packets in the packet capture summary.

   ![image](https://github.com/user-attachments/assets/78bfd2a7-edee-4ac0-a494-fc257eb1380a)


### 3. Calculating SHA256 Hash of Capture File
- **Task**: Find the SHA256 hash of the entire capture file.
- **Solution**: The SHA256 hash value for the file was calculated as `f446de335565fb0b0ee5e5a3266703c7f8b2f3dfa4d7efaececb2da5641a6deb`.

   ![SHA256 Hash Calculation](image3.png)

### 4. Searching for Specific Strings in Packet Details
- **Task**: Search for the string "r4w" to uncover the name of "artist 1".
- **Solution**: Found the name "r4w8173" within the packet details by searching the specified string.

   ![Artist 1 Search](image4.png)

### 5. Extracting and Hashing Image Data
- **Task**: Go to packet number 39765, extract the JPEG data, and find the MD5 hash of the image.
- **Solution**: Extracted the JPEG and calculated its MD5 hash, resulting in `911cd574a42865a956ccde2d04495ebf`.

   ![JPEG Extraction and MD5 Hash](image5.png)

### 6. Finding Text Data Embedded in Capture
- **Task**: Search for a `.txt` file within the capture file and read its contents to find an "alien's name."
- **Solution**: Located the `.txt` file, revealing the name "PACKETMASTER."

   ![Text File Search](image6.png)

### 7. Using Expert Info for Error Warnings
- **Task**: Check the "Expert Info" section for the number of warnings.
- **Solution**: Identified `1636` warnings in the expert info section, related to malformed HTTP packets.

   ![Expert Info Warnings](image7.png)

### 8. Applying a Display Filter
- **Task**: Use a filter to view only HTTP packets.
- **Solution**: Applied an HTTP filter, displaying a narrowed list of packets relevant to HTTP traffic.

   ![HTTP Filter](image8.png)

### 9. Determining the Number of Displayed Packets
- **Task**: Check the count of packets displayed after applying the HTTP filter.
- **Solution**: After filtering, `1089` packets remained visible in the capture.

   ![Displayed Packet Count](image9.png)

### 10. Identifying Total Number of Artists
- **Task**: Locate the total number of artists by examining packet data.
- **Solution**: Found three artists referenced in the packet capture.

   ![Total Artists](image10.png)

### 11. Finding the Second Artist's Name
- **Task**: Identify the name of the second artist from the packet data.
- **Solution**: The second artist’s name was identified as "Blad3".

   ![Second Artist Name](image11.png)

---

## Conclusion
This Wireshark exercise provided valuable insights into network traffic analysis, demonstrating how packet data can reveal hidden information, such as embedded files, comments, and protocol-specific details. Through these practical tasks, I solidified foundational skills in packet filtering, data extraction, and Wireshark's hashing and expert information functionalities.

