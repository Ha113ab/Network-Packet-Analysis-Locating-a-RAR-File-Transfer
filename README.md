# Network-Packet-Analysis-Locating-a-RAR-File-Transfer
This project involved analyzing a network packet capture (S3-Capture.pcapng) to identify an unauthorized file transfer. The task was to find a specific RAR archive that was believed to have been transferred via FTP.


Project Goal
The objective was to locate a RAR file within the packet capture by identifying its unique "magic bytes," which serve as a file signature. This method was necessary because the file extension might have been altered to bypass a firewall's blacklist filter. Once identified, the correct name of the transferred RAR archive needed to be recorded.

Methodology
Initial Research: Used the Internet to determine the file signature/magic bytes for RAR archives of version 5.0 and above.

Packet Capture Analysis: Opened the S3-Capture.pcapng file in Wireshark.

Search & Discovery: Utilized the "Find" feature in Wireshark to search for the discovered RAR file signature/magic bytes within the packet data. This process revealed the file's transfer.

Outcome
The analysis successfully located the transferred file. The Wireshark packet capture confirmed the transfer of a file named 

Target_Payload2.rar. The packet details showed the command 

STOR Target_Payload2.rar, indicating the file was being stored on the server. This confirmed the name of the correct RAR archive file.
