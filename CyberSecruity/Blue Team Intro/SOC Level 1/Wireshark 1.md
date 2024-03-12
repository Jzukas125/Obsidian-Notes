 Wireshark: The Basics
Introduction was some basic intro and suggested courses. Answered it by reading the prompt and filling it in. 

        Task 2 Tool Overview
    Wireshark is one of the most potent traffic analyzer tools available. It's used for detecting and troubleshooting network problems, detecting security anomalies, and investigating and learning protocol details, such as response codes and payload data. Wireshark is not an Intrusion Detection System and only allows analysts to discover and investigate the packets in depth while also just reading and not modifying packets. 

GUI 
    Learning the Wireshark GUI is imperative for using it but luckily its all-in-one page, which helps investigate the traffic in multiple ways. 
    The main five sections are as follows, 
        Toolbar - Consists of multiple menus and shortcuts for packet sniffing, including filtering, sorting, summarizing, exporting and merging.
        Display Filter Bar - Main query and filtering section
        Recent Files - List of the recently investigated files, can be recalled by double-clicking 
        Capture Filter and Interfaces - Capture filters and available sniffing points. The network interface is the connection point between a computer and a network and the software connection enables networking hardware.

Loading PCAP Files
    When a file is loaded in the detail of the file are displayed with the according packet details.
    The packet list pane is the summary of each packet and can be clicked on the list to choose a packet further investigation. Once selcted the details will appear in the other panels.
    The packet details pane is the detailed protocol breakdown of the selected packet.
    The packet bytes pane is the hex and decoded ASCII representation of the selected packet, highlighting the packet field depending on the clicked section in the details pane.

Colouring Packets
    Wireshark colors packets in order of different conditions and the protocols to spot anomalies and protocols in captures quickly. Custom color rules can be created to help easily spot more events of interest. Wireshark has two coloring methods, temporary rules that are only available during the session and permanent rules that are saved under the preference file. Coloring rules can be viewed under the view section. 

Traffic Sniffing
    The blue "shark button" can be used to start network sniffing, the red button stops, and the green button restarts the process. The status bar will also provide the current sniffing interface and the number of collected packets. 

Merge PCAP Files
    Wireshark can merge two pcap files into a singular file by using the file menu path and clicking merge. 
View File Details 
    The statistics bar when using the capture file properties can be used to view the details of the file.

Answering The Questions
    
Read the "capture file comments". What is the flag?
I solved these by going to the statistics and used the capture file properties and found the comment in the information.
What is the total number of packets?
What is the SHA256 hash value of the capture file?

    Packet Dissection
Dissection investigates packet details by decoding available protocols and fields. Wireshark supports a lot of protcols for dissection and also allows custom dissection scripts. 
    Packet Details
Clicking on a packet in the packet list pane opens it. Packets consist of 5-7 layers based on the OSI model. Each time a detail is clicked the corresponding part will be highlighted in the packet bytes pane. When the details are clicked the seven distinct layers of the packet can be seen, and they are as follows:  frame/packet, source (MAC, source (IP), protocol, protocol errors, application protocol, and application data. 
    Seven Layers (Detailed)
        The Frame (layer 1)
    It shows what frame is being looked at and the details specifc to the physical layer of the OSI model.
        Source (MAC) (Layer 2)
    Shows the source and the destination MAC address, from the data link layer of the OSI model.
        Source (IP) (Layer 3)
    Shows the source and destination of the IPv4 address, from the network layer of the OSI model.
        Application Protocol (Layer 5)
    Shows the details specifc to the protocol used such as HTTP, FTP, and SMB. From the application layer of the OSI model.

    Answering Questions 
1. I had to find the markup language is used under the HTTP protocol which is under the Hypertext Transfer Protocol which is the eXtensible Markup Language.
2. I was tasked to find the arrival date of the packet which was in the Frame Layer and was 5/13/2004.
3. I was tasked to find the TTL value which is called the time to live in the internet protocol packet details and the answer was 47.
4. I was tasked to find the TCP payload size which was lcated at the bottom of the Transmission Control Protocol and is 424.
5. I was tasked to find the e-tag which was located in the Hypertext Transfer Protocol and is 9a01a-4696-7e354b00.

                  Packet Navigation
    Packet Numers 
Wire shark calculates the nuber of investigatd packets and assigns a unique number for each packet. This makes it easier for packets to be investigated.

    Go to Packet
The go to packet function is a toolbar that allows the user to easily find any packtet from number. 

    Find Packets
Wireshark can find packets by content, by accesseing the edit menu to make a search menu for packets that are of any interest. There are two main points in finding packets, input (Display filter, Hex, String, and Regex) and search field (packet list, packet details, and packet bytes). Searches are case-insensitive, but it can be set to be case senitive by clicking the radio button.  Searching must be done in the corresponding area ie if you look for info available in the packet details pane and conduct the search in the packet lise pane, Wireshark won't find it even if it exists.

    Mark Packets
Mark packets by using the edit menu or right-clicking and marking them. Marked packets are black regardless of their original color.

    Packet comments
You can also add comments by using the edit menu or right clicking and selecting packet comment. Comments allow the user to add more info to a packet that could be helpful in identifying the packet.

    Export Packets
Capture files may sometimes contain thousands of packets within a single file, as wireshark is not an IDS (intrusion detection system), it is sometimes needed to separate specifc packages from the file and investigate more. The file menu can be used to export packets. 

    Export Objects 
Files can be extracted through the wire which allows you to look at them. This can be done through the file menu and only supports DICOM, HTTP, IMF, SMB, and TFTP file types. 

    Time Display Format
The time display format can be changed in the view menu to display a different time format.

    Expert Info
Specifc states of protocols can also be detected to make spotting possible unwanted activities more easy to spot. While it is helpful it must be kept in mind that it is just a suggestion and there is a chance of false positives or false negatives. Expert info is separated into different colors and they are as follows:
Blue is of Chat Severity and has info on the usual workflow.
Cyan is of the Note severity and has notable events lik application error codes.
Yellow is of the Warn severity and has warnings like problem statements.
Red is of error severity and has malformed packets.
Expert Info can be found in the bottom of the analyse tab.

    Answering Questions 
Search the "r4w" string in packet details. What is the name of artist 1?

Go to packet 12 and read the comments. What is the answer?

There is a ".txt" file inside the capture file. Find the file and read it; what is the alien's name?

Look at the expert info section. What is the number of warnings?
