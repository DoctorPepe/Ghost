# Ghost

Ghost is a prototype packet radio protocol utilizing conventional radioteletype mode technology. The use of multi-layer tone generation theorhetically makes this data transmit scheme four times as fast as other convetional options. Ghost is designed for use through amateur radio, which means transmissions are not encrypted.

## Multi-Layer Tone Generation (MLTG)

The fundemental principle of multi-layer tone generation lies in the use of CTCSS tones. CTCSS tones, or privacy tones, use low-frequency tones to open the squelch of a radio. The use of subaudible tones allows only desired traffic to be heard, and also does not inhibit regular FM voice use. 

Instead of using CTCSS tones in this conventional sense, we can instead use both subaudible tones and conventional tones simultaneously:

![Standard Frame Design]()

### Layer 1
Layer 1 is the subaudible level. This includes a header and footer, which is a single designated CTCSS tone to signify the beginning and end of each frame. 
