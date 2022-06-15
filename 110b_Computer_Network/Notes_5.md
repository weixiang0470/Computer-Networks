# **Chap 3**
## **Transmission Media**
* Wired and Wireless
    - Wireless in limited space and for mobility causes will have more comprehensiveness and convenience
    - Wired is the most commonly used material to have highest transmission efficiency and make sure receiver can get the original signal from sender
### **Twisted Pair**
* To prevent crosstalk(Electromagnetic Interderence)
* The more twist the less crosstalk, the better transimission efficiency, but the higher cost
    - UTP(Unshielded Twisted Pair), commonly uses
    - STP(Shielded Twisted Pair), higher cost not commonly use
    - Most commonly uses are Categoty V , Enhanced Cat V , and Category VI
### **Coaxial Cable**
* Higher cost than twisted pair but can have larger range of transmission frequency, normally uses in wired television
* Sturcture: `Protective Jacket` ( `Outer Conductor` ( `Insulation` ( `Inner Conductor` )))
    - Inner Conductor: Can have single/multiple core, use as transmission medium
    - Insulation: Plastic insulator, use to cover and isolate the inner conductor
    - Outer Conductor: Metal conductor mesh, uses to prevent influences from external electromagnetic wave signal 
    - Protective Jacket: Plastic cover, use to protect and prevent damp,dirt,etc...
### **Optical Fiber**
* Use at backbone parts of internet, high security((transer data with light), high speed, but high cost
    - Laser longer distance, LED lower cost
* Structure: `Protective Sheath` ( `Cladding` ( `Core` ))
    - Core: High-purity glass fiber, use to transit optical signal
    - Cladding: Low refractive index material, use to provide reflection
    - Protective Sheath: Opaque material, use to protect
* Step-index Multimode Fiber
    - Signal Most bad between this 3 Fiber, shortest distance, lowest cost. 50~100um; 125~140um , around 2km
* Graded-index Multimode Fiber
    - Signal badness is middle between this 3 Fiber, can have longer distance than Step-indie, middle cost.50~100um; 125~140um , around 2km
* Single Mode Fiber
    - Most efficiency, longest distance, highest cost. 5~10um;125um , 100km++
## **Wireless Transmission**
* Ground Wave
    - 150km, 3k~3M Hz, ex: AM radio, nautical communication
* Sky Wave
    - 150~500km, 3M~30M Hz
* Line-of-sight
    - Highest distance, 30M++ Hz, ex: satellite communication... Have to place at the highest place to transmit signal
## **Equipments**
### **Modem**
* For modulation and demodulation, because digital signal is not suitable for transmission so need modulate and transmit, then at receiver side do demodulation to get back the signal.
### **NIC**
* Network Interface Card, use to interface between computer and cable, layer 2 device
### **Repeater**
* Signal will attenuation after distance, repeater use to reorganize the signal, layer 1 device
### **Hub**
* Also call multi-port repeater, use to add network connection node
* Broadcast characteristic and Half-duplex transmission, layer 1 device 
### **Bridge**
* Can make a big LAN into 2 small LAN but they still in the same LAN, can have more bandwidth, and less collision(compare with hub)
* Address learning functionm transfer more effective, layer 2 device
### **Switched hub**
* Also call multi-port bridge, can have additional ports(LANs), each port have private bandwidth, layer 2 device
### **Switch**
* Record MAC address and Full-duplex transmission, layer 2 device
### **Router**
* Having repeater, hub, bridge functions, and additional route routing function
    - Find path to transmit from LAN to another LAN or to Internet. Is gate of LAN networks 
* Static method
    - set manually, no need maintenance cost, only follow the rule was seted, any issues will cause disconnection 
* Dynamic method
    - need maintenance cost: Router will communicate with other router in the specified time, if cannot receive the packet then will find another path to transmit
* Router will do more than routing, like: DHCP, Firewall, VPN, etc.... Layer 3 device
### **Layer 3 Switch**
* Use physical method to find the path for transmission, router use software method.
* Lower cost than router cause only do routing function, layer 3 device
### **Gateway**
* Can connect different networks together, ex: telephone network and internet network, layer 7 device

_**IEEE(Layer 1,Layer 2) ; IETF --> RFC(Layer 3 - Layer 7);**_
