# kermit
# Setting up various versions of kermit
I recently (February 2024) rediscoverd the [Kermit Project](https://kermitproject.org), after being a serious user in th 1980'-90's.

Initially I wanted to be able to use kermit on my recently purchased AgonLight2. The CP/M version was included with the version of CP/M made available with the AgonLight2. But is was unable to configure the serial port used.
The new ZINC (Zinc is not CP/M) wrapper does appear to allow this to be configured. But I havent managed to get it working yet.

I also got my BBC Master working again with the [PiTubeDerect](https://github.com/mbernardi1961/PiTubeDoc) and wanted to be able to install kermit on the various processors (so far without sucess). The following ought to be available: 
<li>BBC Kermit [1.46] MOS
<li>MS-DOS Kermit [3.16] DR-DOSPlus
<li>Kermit 80 [4.11] Z80 CP/M
<li>C-Kermit [4C(057)] PANOS

So I wanted to get something working and decided to test compile the new (C-Kermit Beta 10)[https://www.kermitproject.org/ck10devbuilds.html].
As Frank da Cruz says on the C-Kermit 10.0 Beta-Test Builds 2021-24 page; I provided a large percentage of the x86_64 Linux, BSD &amp; Solaris builds in VirtualBox and most the of the ARM builds using a Raspberry Pi 4.

It was particularly interesting building under the BSD and Solaris flavours, as I hadn't used either of these systems before.

Thre are a few systems that SHOULD compile C-Kermit, but hasn't been built for decades! These include the following: Coherent 4.2, Haiku 64, Minix 3.3, OpenStep 4.2, Plan9, I haven't managed to get any of these working yet.
