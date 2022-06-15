# **Chap 5**
## **Introduction to Ethernet**
* From "Aloha", is a simple architecture and low cost, using easy method to transmit (just send your data to the network), but prone to collision.
    - "Aloha" is from University of Hawaii
* First ethernet network system, 1973 : Metcalfe and Boggs : 2.94Mbps
* In 1980 Sep, DEC(Digital Equipment Corp), Intel and Xerox standardlize 10Mbps speed of ethernet network system called DIX ethernet. (contention-based)
* 1995 : IEEE 802.3u : 100BaseT
    - 100 is 100 Mbps, Base is baseband, T is twisted pair. (Baseband means transmit with original signal(Not modulates), broadband means transmit with carrier(had madulated))
    - Different type of twisted pair will have different efficiency when duel with crosstalk
* Another name of ethernet : IEEE802.3
    - Most commonly used is 100BaseTx

## **Setting up ethernet**
* Mostly used is tree topology
    - Only 1 path between 2 nodes

### **Materials and Equipments**
* UTP(Unshielded Twisted Pair), is the cable for ethernet
* RJ-45 connector, the connector head for cable, used to plug in(connect) computer
* RJ-45 protective case, used to protect RJ-45 connector
    - 568A : Crossover
    - 568B : Straight
* NIC(Network Interface Card), a necessary for connection, have "auto sensing" function to modify the transmission speed
    - "auto sensing" : auto detect suitable speed for both sides, ex: A(10/100) and B(10/100/1000), will transmit with speed 100
* Wire stripper, used to peel the cable 
* Diagonal pliers, used to cut the cable
* Crimping Tool, used to connect the RJ-45 and cable by pressing the contact lugs into the twisted pair cable
* Cable Tester, used to test the completed cable
* Hub or Switched Hub, used to connect multiple devices into an ethernet network

### _Extra_
* In Data Center, "Core Aggregate Accedd" is one of the structure
    - Access layer(Layer 1): Server, storage, etc... will connect to this layer
    - Aggregation layer(Layer 2): Connect from access layer to core layer, ethernet channel is here, faster than access layer
    - Core layer(Layer 3): Fastest layer
    - Multipath structure
* Multipath
    - High fault tolerance: If 1 path broke, still can transmit with another path
    - Load balance: For more efficient
* Ethernet channel
    - Combine multiple cable into 1 cable, to have more bandwidth
* Loop network, have broadcast storm issue
    - STP(spanning tree protocol) can solve this issue, when normal it is not a loop logically but when the main path paralyzed then the become a loop(the spare path connects to it)
* WEP , WPA
    - WEP: Most easy to crack, only need to receive enough packets
    - WPA-PSK: Guess and crack, Brute Force Attack and Dictionary Attack
    - WPA-Enterprise: Very hard to crack, ex: nqu's wifi
* http://tw511.com/a/01/9626.html 
    - need to have a pendrive that support ralink(RTxxxx)


## **Wi-Fi**
* Wifi 4 : 802.11n, 600Mbps
* Wifi 5 : 802.11ac, Gbps++
* Wifi 6 : 802.11ax
* When the device is moving(driving at high way), obstacles(wall,building), etc... will affect transmission
* LOS - Light Of Sight
    - Directly to it(Straight), place at high place(no obstacle, ex:tower)
* 802.11 & 802.15 
    - No need license
    - ISM: 2.4Ghz (Industrial - Science - Medical)
    - UNII: Unlicensed National Information Infrastructure 
* 802.16 
    - Need license and permission
    - High power, long distance

## **Ad Hoc**
* Peer to peer, no need base station
* Use SSID(Service Set ID) to differential different IBSS(Independent Basic Service Set)

## **Infrastructure**
* Need base station
    - Transmit through base station
    - Can control the network
* Repeater Mode
    - Cover more distance but have less efficiency
* Bridge Mode
    - Connect multiple wired network systems
    - To communicate with other LAN
### _Extra_
* Tunnel
    - 1,6,11 independent to each other
    - Weaker signal will have less interrupt