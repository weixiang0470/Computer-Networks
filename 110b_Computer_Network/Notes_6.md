# **Chap 4**
## **International organization and standard**
* IEEE: The Institute of Electrical and Electronic Engineers
* ANSI: American National Standards Institute
* ITU: International Telecommunications Union
* CCITT(1865~1993): Consultative Committee on International Telephone and Telegraph
* ITU-T(1993~): ITU-Telecommunications Standardization Sector
* EIA/TIA: Electronic Industries Association / Telecommunication Industry Association
* ISO: International Organization for Standardization
* IAB: Internet Architecture Board
    - IETF: Internet Engineering Task Force
    - IRTF: Internet Research Task Force
* AT&T: American Telephone & Telegraphy Company

## **OSI Reference Model**
* Encapsulation
    - Add header(Trailer only for data link layer), do before send, from Layer7 -> Layer1
* Decapsulation
    - Take out Header/trailer, do when receive, from Layer1 -> Layer7
* [Details in all layer](Notes_3.md)


### **MTU/MSS**
* Maximum Transmission Unit
    - 1500 bytes
* Maximum Segment Size
    - 1500 - 40(TCP and IP) = 1460 bytes (IP 20 , TCP 20)
* Frame
    - 64~1518 bytes : ethernet(6+6+2) + payload(48~1500) + FCS(4)
* Packet
    - 48~1500 bytes : IP(20) + TCP(20) + payload(48~1460)
* If have serious interference then need to decrease MTU

## **Extra**
* Proprietary
    - Exclusive technology/product/protocol
* Base Station
    - Can be layer 2 or layer 3 device through setting
    - Bridge mode(layer 2): Ethernet(wired nodes) and Wireless nodes in one LAN, have better network sharing
    - Router mode(layer 3): Ethernet and Wireless nodes is in different LAN, is more secure

* _Layer 2 device for some special purpose will also have ip address, like management or maintenance_
* _OSI Reference model by ISO , TCP/IP by IAB_