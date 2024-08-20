I was looking for a few topics of DFIR which are not used a lot in CTF, and i found EDRs or EVENT DATA RECORDERS.

One popular example would be Black Boxes in a flight or so.

and the thing i think we can proceed in is the data stored in Cars.

i was looking in V2X communication but since making a prototype would be hassle i ditched it.

Then i found about `CAN` i'll let Claude explain it

```
Certainly! I'd be happy to explain how CAN (Controller Area Network) works. CAN is a robust vehicle bus standard designed to allow microcontrollers and devices to communicate with each other within a vehicle without a host computer. Here's an overview of how CAN works:

1. Basic Principle:
   CAN is a multi-master, message-based protocol. This means any node can send a message (called a frame) when the bus is free.

2. Physical Layer:
   - Uses two wires (CAN High and CAN Low)
   - Differential signaling for noise resistance
   - Typical speeds range from 125 kbit/s to 1 Mbit/s

3. Message Format:
   A CAN frame typically includes:
   - Arbitration ID (11 or 29 bits)
   - Data Length Code (DLC)
   - Data field (0-8 bytes)
   - CRC field for error checking
   - Acknowledgment bit

4. Arbitration:
   - When multiple nodes try to transmit simultaneously, a non-destructive bitwise arbitration is used
   - Lower ID numbers have higher priority
   - Nodes automatically back off if they lose arbitration

5. Error Handling:
   - CAN has sophisticated error detection mechanisms
   - Includes CRC checks, bit stuffing, and frame checks
   - Faulty nodes can be automatically shut off from the bus

6. Message Types:
   - Data frames: Carry data from a transmitter to receivers
   - Remote frames: Request transmission of a specific identifier
   - Error frames: Transmitted when a node detects an error
   - Overload frames: Provide an extra delay between data or remote frames

7. Broadcasting:
   - All nodes can see all messages on the bus
   - Nodes decide which messages to process based on the arbitration ID

8. Addressing:
   - CAN doesn't use traditional addressing
   - Instead, each message has an identifier that implies its priority and content

9. Real-time Capabilities:
   - Guaranteed latency times
   - Prioritization of messages

10. Robustness:
    - Resistant to electromagnetic interference
    - Can function even if one of the signal wires is cut or shorted
```

i still am not sure if these can be stored as a different file type or it is just a protocol, if it's later then there is no point but we trust.
