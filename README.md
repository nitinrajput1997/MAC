# MAC

These are the functions of Mac :-

1. Logical-channel multiplexing
2. Hybrid-ARQ retransmission
3. Scheduling
4. Multiplexing/Demultiplexing for carrier aggregation 

### Multiplexing Logical Channel

MAC layer provides the services to the RLC in the form of logical channels.

MAC layer uses services from PHY layer in the form of transport channel.

**Logical Channel:** It defined by the "types of information" it carries and its generally classified as control chaannel (used for the transmission and configuration information necessary for operating in oue system and as a traffic channel (used for the user data).   

**Transport Channel:** It is defined by "how and with what characteristic information" is transmitted over the radio interface. This includes paging, broadcast or shared channel.

Logical Channel have:-<br />
a) Broadcast Control Channel (BCCH)<br />
b) Paging Control Channel (PCCH)<br />
c) Common Control Channel (CCCH)<br />
d) Dedicated Control Channel (DCCH)<br />
e) Dedicated Traffic Control Channel (DTCH)<br />

Tansport Channel have:-<br />
a) Broadcast Channel (BCH)<br />
b) Paging Channel (PCH)<br />
c) Downlink Shared Channel (DL-SCH)<br />
d) Uplink Shared Channel (UL-SCH)<br />
e) Random Access Channel (RACH)<br />

**Carrier Aggregation**

In this, the data are distributed over multiple cells not just at one cell.

**HARQ**
The main mechanism responsible for retransmission in MAC layer is HARQ.

It is hybrid such as, it checks error message through channeling and retransmission of message if error occurs. 

NOTE:<br />
Error Correecction are done on = PHY layer<br />
Retransmission are done on = MAC layer<br />

In this , one block is transmitted and wait for the "No Negative Acknowlegement (No NAK)" and then transmit another block otherwise retransmit same block until it get feedback as No NAK.

If there is large transport block , it was then divided into small CODE BLOCS during the channel coding process in the Physical Layer.

Suppose during the transmit , the tranport block become erroneous. Now we no need to retransmit whole Transport block instead we need to find out which code block is erroneous . So for that we grouped the code bloxk which is known as CBG(Code Block Group).

**Scheduling**
Suppose there are three different user connected to base station. Now they have different services and priority to allocate data.

Now the Scheduler comes into the game, it takes frequency resources and for each time instant lets say onee slot for a given time instant of a scheduling interval. It schedules 'where and how much data' the different users can use and when this is successfull in the next and subsequent time slot , the scheduler keeps updating for each slot, what is the best allocation of resources between different users. This is the function of scheduler.

Now, officially Scheduler is the part of MAC-Layer in NR. It is better to accept scheduler as a sepearte entity because it interacts with different layers in order to carry out its functions and also controls its different layers in oreder to carry out its functions.
