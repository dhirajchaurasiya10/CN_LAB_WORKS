Q) What is the value of each of the header fields ? Explain why the value is what it is .


--> a. Version(4 bits) , value =4. The value 4 indicates that the IP version is 4, i.e., IPv4.

--> b. Header Length (4 bits) , value =5 . Indicates the number of 32-bit words in the header. A value of 5 means the header is 20 bytes long (5 * 4 bytes).

--> c. DSCP (6 bits) ,Value= 0x00 . A value of 0x00 indicates that all 6 bits in the DSCP field are set to 0. This is typically referred to as the Default Forwarding (DF) class. Traffic marked with DSCP 0x00 (DF) does not get any priority over other traffic types and is treated with the lowest priority.

--> d. ECN (2 bits) , This value indicates that the packet is not using ECN. It is not ECN-capable, and any network devices should not set or interpret ECN-related bits for this packet. ECN allows end-to-end notification of network congestion without dropping packets.

--> e. Total Length (2 bytes) , Value =52 , This value indicates that the entire packet, including the header and data is 52 bytes long .

--> f. Identification (2 bytes), Value =0x0000, This value indicates that the entire packet, including the header and data is 52 bytes long.

--> g. Flags (3 bits) , Value=0x2, Don't fragment. The value 0x2 indicates the "Don't Fragment" flag is set, meaning the packet should not be fragmented.

--> h. Fragment Offset( 13 bits) , Value = 0, Indicates where in the datagram this fragment belongs. A value of 0 means the packet is not fragmented.

--> i. TTL (1 byte) , Value=62 , Indicates the packet can pass through 61 routers before being discarded. Operating systems like macOS or GNU/Linux often use a default TTL of 64, meaning the packet has already passed through 3 routers in this case.

--> j. Protocal (1 byte) , Value : TCP(6) , Indicates that the Transmission Control Protocol (TCP) is being used in the data portion of the IP packet.

--> k. Header Checksum (2 bytes) , value : 0x04d6, Used to verify the integrity of the header. If the checksum does not match the calculated value at the receiver, it indicates that some data is lost or corrupted. Here, the checksum status is unverified.

--> l. Source Address (4 bytes) , value: 142.250.194.206 , It indicates the IP address of the sender. The packet is sent from the IP address 192.168.31.73 .

--> m. Destination Address (4 bytes), value: 192.168.31.118, It indicates the IP address of the receiver. The packet is sent to the IP address 192.229.232.200 .
