# LoRaWAN Device Address Space

Although LoRaWAN devices have a 64 bit unique identifier (DevEUI), the communication is done with a dynamic 32 bit device address (DevAddr) of which 7 bits are fixed for The Things Network, leaving 25 bits that can be assigned to individual devices, a procedure called **Activation**.

## Over-the-Air Activation (OTAA)

Over-the-Air Activation (OTAA) is the preferred and most secure way to connect with The Things Network. Devices perform a join-procedure with the network, during which a DevAddr is assigned and security keys are negotiated with the device.

## Activation by Personalization (ABP)

In some rare cases you might need to hardcode the DevAddr as well as the security keys in the device. This means activating a device by personalization (ABP). This strategy might seem simpler, because you skip the join procedure, but it also has some nasty downsides.

> TODO: Explain the downsides (frame counters, replay attack protection, ...).