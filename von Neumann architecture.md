#Computer 
The von Neumann [[architect]]ure—also known as the von Neumann model or Princeton architecture—is a [[computer]] architecture based on a 1945 description by [[John von Neumann]], and by others, in the First Draft of a Report on the EDVAC.[1] The document describes a design architecture for an [[electronic]] [[digital]] computer with these components:

-A processing unit with both an arithmetic logic unit and processor registers
-A control unit that includes an instruction register and a program counter
-Memory that stores data and instructions
-External mass storage
-Input and output mechanisms

The term "von Neumann architecture" has evolved to refer to any stored-program computer in which an instruction fetch and a data operation cannot occur at the same time (since they share a common bus). This is referred to as the von Neumann bottleneck, which often limits the performance of the corresponding system.

The design of a von Neumann architecture machine is simpler than in a Harvard architecture machine—which is also a stored-program system, yet has one dedicated set of address and data buses for reading and writing to memory, and another set of address and data buses to fetch instructions.

A stored-program computer uses the same underlying mechanism to encode both program instructions and data as opposed to designs which use a mechanism such as discrete plugboard wiring or fixed control circuitry for instruction implementation. Stored-program computers were an advancement over the manually reconfigured or fixed function computers of the 1940s, such as the Colossus and the ENIAC. These were programmed by setting switches and inserting patch cables to route data and control signals between various functional units.

The vast majority of modern computers use the same hardware mechanism to encode and store both data and program instructions, but have caches between the CPU and memory, and, for the caches closest to the CPU, have separate caches for instructions and data, so that most instruction and data fetches use separate buses (split cache architecture).


![[Pasted image 20230524210940.png]]