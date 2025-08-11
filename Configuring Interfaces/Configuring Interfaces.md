Routers- shutdown by default - in admin down/down 

Switches- up/up if connected, down/down if not connected



show int status



duplex is auto on Cisco switches



config-inf# speed ?

10

100

auto



\#duplex ?

auto

full

half



changing multiple interfaces:

int range f0/5 - 12

int range f0/5 - 6, f0/9 - 12



desc not in use

shutdown



half duplex:

**CSMA/CD Carrier Sense Multiple Access with Collision Detection**

before sending frames, devices listen to collision domain until they detect other devices are not sending

sends jamming signal for collisions

devices will wait to send frames again



**speed/duplex auto negotiation** 

int advertise to neighboring device, negotiate best speed/duplex settings both capable of

if other device can't auto neg:

speed- switch will try to sense speed and will use slowest supported speed

duplex- if speed is 10/100 will use half duplex, 1000+ full

duplex mismatch = collisions

