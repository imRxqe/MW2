# Next Todo:
* Make a non-host menu base to be able to test sending udp packet from client to host 
* This should apply to joinparty and the ReadBitsCompressed i guess

# Remeber stuff:
* g_scr.h which i added to this repo contains meansOfDeath_t
* client.h contains indexes for throwingknife offhand
* structs.h contains grenadetimes etc

# Ideas:
* Decrypt known sprx files and compare functions, how they looked decompiled vs source
* Compare functions with quake III Source
* Run python server on pc and connect to it from sprx, send data to it, use as service etc.

\# Overview Exploits/CVE

* Known CVEs:

> CVE-2018-10718 --> ExecuteClientMessage/ReadBitsCompressed (Sabotage, Momo5502 writeup) => Just send connectionless udp package

> CVE-2019-20893 --> PartyHost\_HandleJoinPartyRequest (BlastsMods)

> CVE-2018-20817 --> SV\_SteamAuthClient 

> Unknown --> ?



\# Netchan API

* Netchan\_Transmit / Netchan\_SendPacket
* void CL\_Netchan\_Transmit( netchan\_t \*chan, msg\_t\* msg);	//int length, const byte \*data );

location of netchan string: 0x00569fa1



\# JoinParty

* Search for joinparty in the binary, you find some strings atleast



\# Souls RCE v2

Hooked functions:
  HookFunctionStart(0xdb918,PTR\_LAB\_0001d008,PTR\_FUN\_0001cfe0);

&nbsp; HookFunctionStart(0x50f7c4,PTR\_LAB\_0001d010,PTR\_LAB\_0001cfe8);

&nbsp; HookFunctionStart(0xaf978,PTR\_LAB\_0001d018,PTR\_FUN\_0001cff0);

&nbsp; HookFunctionStart(0x50f344,PTR\_LAB\_0001d020,PTR\_FUN\_0001cff8);

&nbsp; HookFunctionStart(0x23a138,PTR\_containsKillswitch\_0001d028,PTR\_5thFuncKillswitchStub\_0001d000);

