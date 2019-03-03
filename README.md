# Ghost

Ghost is a prototype packet radio protocol utilizing conventional radioteletype mode technology. The use of multi-layer tone generation theoretically makes this data transmit scheme four times as fast as other convetional options. Ghost is designed for use through amateur radio, which means transmissions are not encrypted.

## Multi-Layer Tone Generation (MLTG)

The fundemental principle of multi-layer tone generation lies in the use of CTCSS tones. CTCSS tones, or privacy tones, use low-frequency tones to open the squelch of a radio. The use of subaudible tones allows only desired traffic to be heard, and also does not inhibit regular FM voice use. 

Instead of using CTCSS tones in this conventional sense, we can instead use both subaudible tones and conventional tones simultaneously:

![Standard Frame Design](https://github.com/DoctorPepe/Ghost/master/MLTG_Diagram.jpg)

### Layer 1
Layer 1 is the subaudible level. This includes a header and footer, which is a single designated CTCSS tone to signify the beginning and end of each frame, as well as the senders callsign. The frame portion of layer 1 includes checksums to give a method of identifying interference or packet loss, as well as some extra room for further data. This extra room can be used to send various supplamentary data, such as GPS or gridsquare location, weather data, or signal loss to name a few. Additionally, layer 1 can be used in combination with layers 2 and 3 to increase simultaneous data transmission to decrease the time it takes to transmit a frame.

### Layer 2/3
Layers 2 and 3 consist of your standard radioteletype high and low signals which make up the signal data. Think RTTY for PSK31. In additiona to the callsign being transmitted in the header, it is also sent here. The callsign here is sent as a redudency, and creates an additionall check to ensure callsign accuracy. 

While the initial goal of ghost is to create an even more robust digital text mode, the hope is that ghost could one day be multi-mode, including sending data, images, or the maybe multiple at once. 
