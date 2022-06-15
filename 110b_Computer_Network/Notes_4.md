# **Chap 2**
## **Transmission type**
### **Simplex**
* Only one direction(1 way) transmission, ex: broadcast, television, radio, etc...
### **Half-duplex**
* Two direction(both way) transmission, but only 1 direction at the same time, ex: walkie talkie
### **Full-duplex**
* Two direction transmission and can 2 direction at the same time, ex: phone call

## **Signal**
* Magnitude
    - ex: volume of sound
    - If magnitude is bigger , signal can transmit longer distance
* Frequency
    - ex: 10Hz
    - c(light speed) = f * wavelength , if f is smaller and wavelength is longer, then area covered is bigger
* Phase
    - Phase, ex: difference of delta(t)
* `S(t) = m(t) * cos(2 * pi * f(t) + delta(t))`
* 1024QAM: 1 signal can bring 10 bits. 256QAM: 1 signal can bring 8 bits. 
    - 2^10 = 1024 , 2^8 = 256 || 1024QAM is 1.25 times faster than 256QAM , 10/8= 1.25

## **Modulation**
### **Analog modulation**
* AM
    -Amplitude Modulation, modulate the magnitude of signal, easy to interfere 
* FM
    -Frequency Modulation, modulate the frequency of signal, more resistance to interference 
* PM
    - Phase Modulation, modulate the phase of signal

### **Digital modulation**
* ASK
* FSK
* PSK

_Digitize usually do before transmission, can do something on signal, like: encrypt, make some effect on sound, etc..._

## **Progression of Analog to Digital Signal**
### **Sampling**
* On X-axis, sampling the x-axis of signal in an interval time
* The more sample, more accuracy, but need more time and storage
* Nyquist theorem: `Fs >= 2 * Fm` frequency of sampling have to more than 2 times of maximum frequency of signal
### **Quantization**
* On Y-axis, quantify the amplitude value of sample
* The more bits used, the more similar to original signal, but need more storage and time. 
    - 256(2^8) means use 8 bits/sample , 65536 (2^16) means use 16 bits/sample
### **Encoding**
* For more effective transmission and synchronization of digital signal
* NRZ-L
    - 1 : +V 
    - 0 : -V
    - Low cost, only using +V and -V only, ex: RS-232(early generation cable).
* NRZ-I
    - 1 : Invert the V 
    - 0 : maintain the V
    - Differential encoding, ex: FDDI(early optical fiber)
* Manchester 
    - 1 : +V to -V 
    - 0 : -V to +V
    - self-clocking, faster, less error and no need synchronization, early generation Ethernet(10mb/s)
* Differential Manchester
    - 1 : Invert |(+V to -V) to (-V to +V)| or |(-V to +V) to (+V to -V)|
    - 0 : Maintain (+V to -V) or (-V to +V)
    - Token-ring, self-clocking
* MLT-3
    - Step: +V --> 0 --> -V --> 0 --> +V
    - 1 : Move 1 step
    - 0 : Maintain
    - 100BaseTx ethernet
        - (100 : Base : Tx) ==> (Speed is 100Mbps : Modulation statuts(Base is not, broad is  have) : Material or Distance)
* 4B/5B 
    - 4 bit transfer to 5 bit, to prevent continuously of '0' signal to make the transmission progress faster
    - 100BaseFx
    - 8B/10B, 8B6T
### **Analog process**
* By Modem, 
    - modem : modulation and demodulation

## **Multiplexing**
### **FDM**
* Frequency Division Multiplexing
* Divide tunnel into smaller tunnel to different users
    - Using different frequency of carrier to modulate different signals and use the same channel to send all the signal.
    - They won't affect each others is because they're using different range of frequency
### **TDM**
* Time Division Multiplexing
* Divide time-axis of tunnel into slots(time slots), seperate to different users, the user can use all resource when is his time
### **CDM**
* Code Division Multiplexing
* Use different encoding style so they won't affect each other
    - Using the same frequency but won't affect each other cause they're using different coding
    - See others signal as noise

## **Telephony**
### **Circuit Switching**
* The line will 100% be yours
    - During communication others node cannot communicate with both sender or receiver.
    - ex: Even you're not using but still need to pay
### **Packet Switching**
* Divide data(to deliver) into smaller packets and add(mark) the control command(destination address) on it to deliver packets to the right user.
* When destination station receive all packet and it will recombined all the packet into original data.
* Can be used by many users, effectively increase usage, but if too many users will occure some errors(packet lost)
### **Message Switching**
* Similar to packet switching but using the method "Store and Forward" on every intermediate switching node
    - When receive, store the message(combine all the small packets into message) and then send message in packets form(divide message into smaller packet and send)
![EX_of_Message_switching](Images/Note4.1.png)
* Example of sending email from A to B
    - Mark mail address on the message, then send
    - A will divide message into packets and send to mail2 first
    - mail2 will store(combine packets into message) and forward to mail1(if availale) in packets form
    - mail1 will store and forward to B
